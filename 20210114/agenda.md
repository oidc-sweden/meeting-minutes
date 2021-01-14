# Agenda & mötesanteckningar 2021-01-14

https://sunet.zoom.us/my/fresia


* Intro & recap från senaste gången
* Signature extension
* Pilotimplementationer (både client och OP)
* Ta fram en gemensam roadmap


## Närvarande

* Leif Johansson
* Martin Lindström
* Stefan Santesson
* Fresia Pérez
* Dragoljub Nešić
* Petter Dahl
* Jesper Skagerberg
* Stefan Halén
* Roger Fagerud

## Anteckningar

* Martin gick igenom anteckningarna från förra mötet.

* Martin presenterade det utkast kring [Signature Extensions](https://github.com/oidc-sweden/specifications/blob/main/oidc-signature-extension.md) som har påbörjats. Det ser ut som att vi kan implementera stöd för underskrift med relativt små ingrepp (ett nytt request object).

    - Dragoljub hade förslag på att ett "signature request" också ska kunna innehålla krav på signaturformat etc. Leif hade invändningar mot att man kan öppna upp för olika typer av attacker om klienten dynamiskt ska kunna styra vilken typ av signatur som skapas.
    
    - Vi kommer förmodligen att behöva göra ev. konfiguration av signaturformat etc. som en del då klienten registerar sig hos OP:n. Ev. kan vi också ha vissa flaggar som är dynamiska.
    
    - Martin nämnde några ytterligare saker som behöver hanteras kring "signature requests", bl.a. kravet på att inte tillåta SSO vid signering och möjligheten att skicka över kända attribut (t.ex. personnummer).
    
* Vid diskussioner angående pilotimplementationer av klienter och OP:er kom gruppen fram till:

   - Freja och BankID sätter upp varsin OP (som använder test-credentials).
   
   - Sunet kan sätta upp en proxy mot Sweden Connect (alt. eduID).
   
   - Martin tar fram en klientapplikation motsvarande den vi har för SAML. Se https://test.swedenconnect.se (prod), https://qa.test.swedenconnect.se (QA) och https://eid.idsec.se/testmyeid/ (sandbox). Denna app bygger på Spring Frameworks bibliotek för OAuth2 och OIDC.
   
   - Internetstiftelsen tittar på om de kan ta fram en klient.
   
   - På sikt bör vi inventera vilka hyllprodukter/lösningar vi kan använda under tester.
   
   - Som en följd av pilotimplementationer kan det bli så att vi berör UX-frågor m.a.p. bl.a. terminologi.
   
   - För att piloterna ska kunna starta bör vi ha någorlunda färdiga utkast för protokoll-specifikationera, dock behöver frågan ang. klientregistrering inte lösas utan kan hanteras manuellt under pilotdriften.
   
* Leif diskuterade OIDC federation som ett alternativ registreringsprocesser som inte skalar lika väl. Gruppen ser inte detta som akut, men vi bör enas om vilken väg vi vill gå. 

   - Leif gör en presentation tills näst-nästa möte. Vi kan också passa på att fråga Roland under webinariet.
   
* Martin föreslog följande roadmap (utan invändningar):

**2021-Q1:** Protokollspecifikationer är i implementeringfärdiga lägen (deploymentprofil, attributspecifikation och signature extension). Under denna period kan vi också börja förbereda för pilotimplementationer.

**2021-Q2:** Pilotimplementationer och interoperabilitetstester. Målet med dessa pilot-POC:ar är att validera att våra specifikationer "håller måttet" samt ge input till kommande steg såsom specikationer för registrering, "discovery", och deployment i skarp drift etc.

**2021-Q3 och framåt:** Deploymentfrågor - hur ska detta realiseras i drift? Fastställande av specifikationer. Federation och registrering.


## Nästa möte

* 2021-01-29, 14:00-15:30 (https://sunet.zoom.us/my/fresia)

