# Agenda & meeting notes 2022-05-31

https://sunet.zoom.us/my/fresia


* Re-cap
* Introduction for new participants
* What has happened since last?
* Where should we publish our specifications?
* Things left to do
* What we shouldn’t do
* CIBA – Include or not?
* Plans for Sweden Connect

See [Re-booting OIDC Sweden](Re-booting_OIDC_Sweden_20220531.pdf).


## Participants

* Martin Lindström
* Leif Johansson
* Stefan Santesson
* Fresia Pérez
* Petter Dahl
* Erik Lupander
* Stefan Halén
* Aras Kazemi
* Magnus Hoflin
* Anders Malmros
* Jerker Hagman
* Olle Nyman
* Abdul Ghafoor

## Notes

We started the meeting with a presentation round to welcome the new members from Rise and Skatteverket.

Martin informed what has happened since last time we meet. DIGG has decided to introduce OpenID Connect
to the Sweden Connect-federation, and base the new specifications on our group's work.

Then followed discussions about where to publish our work. Leif reported about the way of things in
Kantara, and meant that the main reason for us to lay under an organisation such as Kantara was to
protect our from intellectual property issues.

We want to publish our work as soon as possible, and to initate, and complete a process with Kantara, or
any other organisation, may take years. Therefore, the group decided to publish our work at www.oidc.se 
(via GitHub pages). At least initially.

We also dicussed whether Internetstiftelsen would be a good place to host our specs at.

Martin presented a listing of "things that are left to do" before we reach final specifications.
Nobody objected when he suggested that we leave "Vectors of trust" out. However, one thing that we want to
look into, and possibly introduce, is CIBA - OpenID Connect Client-Initiated Backchannel Authentication
Flow". This flow greatly resembles that flow of using the BankID and Freja-API:s.

> Action point: Erik goes through this spec and notes what is missing from a BankID point-of-view.

Next, Martin presented a listing of items belonging to the category "things we shouldn't do within the group".
One thing that we should leave to others (Sweden Connect) is to try to profile the use of OIDC in federations.
We also agreed that we shouldn't let the eIDAS 2-work (wallet) interfere.

> More action points: Martin will initiate the OIDC Sweden Connect work and move some of the specifics 
from our specs there. Most importantly, eIDAS-sector specific attributes and signing spec writings that
concerns the federated signing model will be moved.

## Next meeting

Not decided yet, but we aim for a slot during week 25 (20/6-23/6). Invitation will be sent soon.

 

