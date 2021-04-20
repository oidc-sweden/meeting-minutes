# Agenda & mötesanteckningar 2021-04-09

https://sunet.zoom.us/my/fresia


* Intro & recap från senaste gången
* Diskussioner - inkomna frågeställningar - Se [Issues](https://github.com/oidc-sweden/specifications/issues)
* Första version av profil (huvuddokumentet för den svenska profilen)
* Tester


## Närvarande

* Leif Johansson
* Martin Lindström
* Stefan Santesson
* Fresia Pérez
* Dragoljub Nešić
* Petter Dahl
* Jesper Skagerberg
* Erik Lupander
* Stefan Halén
* Roger Fagerud
* Per Mützell
* Anders Malmros

## Anteckningar

Martin gick igenom [huvudspecen](https://github.com/oidc-sweden/specifications/blob/main/swedish-oidc-profile.md) som påbörjats:

- Vissa attribut som anges i [Attribute Specification for the Swedish OpenID Connect Profile](https://github.com/oidc-sweden/specifications/blob/main/swedish-oidc-attribute-specification.md) ska stödjas för att vara compliant.

- Kring säkerhetskrav och begära signerade request för klientautentisering så bör vi inte hårt kräva signerade request till token-endpoint, utan också kunna hantera andra lösningar (password + mutual TLS). Andra profiler (t.ex. Sweden Connect eller Inera) kan stärka detta krav i egna profiler. Det kan till månt och mycket lämnas över till IdP:n (OP) att avgöra.

- Det ska vara mandatory för IdP:er att hantera signerade JWT:er.

- För signering ska `prompt` sättas till `login`, dvs, ingen SSO.

Vi bör ha ett annat namn för delegatedSign. Brokered signing är ett förslag.

Syftet med de kommande testerna är helt och hållet för interoperabilitet samt att "testa" våra specifikationer.


## Nästa möte

* 2021-04-23
 

