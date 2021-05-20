# Agenda & mötesanteckningar 2021-04-23

https://sunet.zoom.us/my/fresia


* Intro & recap från senaste gången
* Första version av profil (huvuddokumentet för den svenska profilen)
* Diskussioner - inkomna frågeställningar - Se [Issues](https://github.com/oidc-sweden/specifications/issues)
* Tester - Dags att starta
* Hitta intressenter för klientimplementationer
* Use-cases
* Marknadsföra arbetet utåt?


## Närvarande

* Martin Lindström
* Leif Johansson
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

- Martin gick igenom huvuddokumentet för den svenska profilen:

  - Kommentarer kring autentisering av klienten. Vi bör tillåta även clientSecret, och de tillämpningar som vill ha högre säkerhet kan skärpa detta krav.
  
  - Birthdate och age bör inte vara "mandatory". Alla IdP:er har inte tillgång till denna information.
  
  - Erik hävdar (korrekt) att enligt OIDC core så ska UserInfo användas för att leverera info enligt `user_info` claim. Vi måste utreda hur claims ska levereras. Att leverera i token endpoint är egentligen att föredra.
  
- Diskussioner om hur vi ska få vårt arbete att "lyfta". Specifikt måste vi få in organisationer som är intresserade av att ta fram klienter. F.n. har vi ingen uppenbar kandidat.

## Nästa möte

* 2021-05-21
 

