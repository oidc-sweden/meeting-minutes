# Agenda & mötesanteckningar 2021-01-29

https://sunet.zoom.us/my/fresia


* Intro & recap från senaste gången
* Öppna diskussioner ...


## Närvarande

* Leif Johansson
* Martin Lindström
* Stefan Santesson
* Fresia Pérez
* Petter Dahl
* Jesper Skagerberg
* Erik Lupander
* Stefan Halén

## Anteckningar

* Martin gick igenom anteckningarna från förra mötet.

* Leif pratade om att sätta upp SATOSA-instanser för OIDC framför Sweden Connect:s IdP:er. 

* Martin tog upp frågan om ett växande intresse/behov för attributtjänster. Med SAML är detta svårt att få till på ett bra sätt, men det kan vara en god idé att boosta vårt arbete genom att göra en presentation som visar hur OAuth2 och OpenID Connect är en bättre platform att stå på vad gäller en mer dynamisk hantering av attribut.

* Diskussioner angående utmaningar med trust (dvs. tillit till certifikat) och hur detta ska hanteras ut mot förlitande parter. Det är önskvärt att vi tittar på någon form av automatiseringslösning som medger en enklare hantering av certifikatbyte. För BankID är detta inget jätteproblem i dagsläget eftersom de kan byta certifikat för sin TLS-endpoint relativt enkelt då root-certifikatet sällan ändras. För SAML, or OIDC, är tilliten ofta direkt till ett visst certifikat (nyckel) - detta noterat som en "utmaning".

* Erik har tagit fram en demo/poc där en demoapp använder sig av OIDC för att autentisera en användare mot BankID. Mycket återstår, men bollen är i rullning.

* Diskussioner ang. användare av ACR (authentication context class reference) vs. VoT (Vectors-of-trust). Vi har ett arbete kvar för VoT, och iGov rekommenderar att man stödjer båda, dock inte i samma meddelande. För "enklare" klienter är VoT förmodligen inget som efterfrågas, men större myndigheter och liknande kan vara intresserade. Som iGov föreslår det så avgör klienten huruvida acr eller vot ska användas i responsen.

* Enkelhet. Jesper har ett krav (förhoppning) att det vi kommer fram till inte gör det "för komplext" för små förlitande parter att ansluta. Vi bör ha detta som en ledstjärna under framtagandet av våra specifikationer. Speciellt utmanande kan det vara med krav på signerade JWT:s. För närvarande används en bakkanal som skyddas med mutual-TLS i BankID-fallet.

* Inför webinariet med Roland den 11/2 bestämde vi att vi skulle sammanställa ett antal frågor. 

* Martins frågor till Roland:

**Komplexa datatyper som claims**:

Vi definierar en egen attributprofil för användande inom Sverige. Bland annat behöver vi representera personnummer, hsa-id etc som claims. För eIDAS ID har vi definierat ett claim, `http://claims.oidc.se/eidasPersonId`, enligt:


```
"http://claims.oidc.se/eidasId" : {
  "prid" : "DE:8976543432",
  "persistence": "A",
  "eidasPersonIdentifier" : "DE/SE/0008976543432"
},
...
```

Är detta en dum idé, och bör vi istället ha tre separata claims för resp. värde? De olika värdena hör ihop och levereras alltid tillsammans, men det kan ju innebära interop-problem om vi introducerar claims som inte är enkla strängvärden.

**iGov:**

Vi planerar att utgår från iGov:s OIDC profil (https://openid.bitbucket.io/iGov/openid-igov-profile-id1.html). Finns det någon annan profil som vi också bör titta på?

**Request Objects:**

Bland annat för att kunna hantera "begäran om underskrift" planerar vi att definiera ett *Request Object* som innehåller data som ska skrivas under, underskriftsmeddelande, m.m. Hur ser stödet ut i bibliotek och programvaror för att kunna hantera Request Objects? Är det att be om problem?

## Nästa möte

* 2021-02-11, 08:30-12:30, Webinar med Roland Hedberg

