# Agenda & mötesanteckningar 20201210

https://sunet.zoom.us/my/fresia


* Intro & recap från senaste gången
* Samordningsnummer
* Vectors-of-trust
* Seminarium


## Närvarande

* Leif Johansson
* Martin Lindström
* Stefan Santesson
* Fresia Pérez
* Dragoljub Nešić
* Petter Dahl
* Jesper Skagerberg
* Stefan Halén

## Anteckningar

* Martin gick igenom anteckningarna från förra mötet.

* Fresia sonderade intresse för webbinarium med Roland Hedberg. 

    - Martins tillägg: Kika på Rolands sida på [GitHub](https://github.com/rohe). Flera intressanta repositorys, bl.a. [oidctest](https://github.com/rohe/oidctest) och [openid_course](https://github.com/rohe/openid_course).

* Diskussioner angående samordningsnummer, och dilemmat med att vissa är "starkare" än andra men att de ändå inte kommer upp i LoA 3. Det är oklart hur vi ska kunna använda samordningsnummer utan att använda kompletterande attribut som beskriver dess ursprung och "styrka".

* Leif presenterade vectors-of-trust (https://tools.ietf.org/html/rfc8485).

* Martin visade att vi har ett påbörjat utkast till vår tolkning av vectors-of-trust, https://github.com/oidc-sweden/specifications/blob/main/swedish-oidc-vector-of-trust.md.

* Diskussioner om vectors-of-trust och riskhantering. Jesper framförde att vi inte får "överspeca" detta. Då kommer vi aldrig i mål.

* Korta diskussioner om attribut och vikten av att kunna leverera också "authentication information" attribut. Dessa attribut ska kunna användas till bl.a. riskhantering. Martin förslog att dessa levereras via scopes och inte som default. 

* Martin bad alla ta en titt på iGov-profilen, [International Government Assurance Profile (iGov) for OpenID Connect 1.0](https://openid.net/specs/openid-igov-openid-connect-1_0.html). Det är förmodligen den profil som bäst matchar det vi vill göra i Sverige.

* Jesper önskar att vi tittar på best practices kring användning av OIDC i appar. Hur hanterar man webbläsaren och kommunikation mellan front- och backend bl.a.

## Beslut 

* Vi beslutade att försöka få till flera sittningar med Roland där första fokus är att få en introduktion.

* Gruppen avvaktar utredning kring samordningsnummer (https://www.statenspersonadressregister.se/root/om-spar/aktuellt/nyheter-2020/2020-10-23-information---forandringar-gallande-samordningsnummer-fran-2021-01-01.html).

* Gruppen kikar på utkastet till vectors-of-trust och ger feedback (via [Issues](https://github.com/oidc-sweden/specifications/issues) i GitHub).

* Martin lägger upp ett icke-normativt dokument, cookbook/examples, där vi kan illustrera det vi diskuterar på ett enkelt sätt.

* Nästa möte - 2021-01-14, 12:30-14:00 (https://sunet.zoom.us/my/fresia)

