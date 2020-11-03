# Meetings minutes for the Swedish OpenID Connect Working Group


## 2020-11-03

**Participants:**

- Leif Johansson, SUNET
- Fresia Pérez Arriagada, SUNET
- Martin Lindström, IDsec Solutions
- Stefan Santesson, IDsec Solutions
- Petter Dahl, BankID
- Jesper Skagerberg, BankID
- Carl Hössner, BankID
- Dragoljub Nešić, Freja eID
- Milica Jelić, Freja eID
- Stefan Halén, Internetstiftelsen

This was the first meeting of the working group where Martin Lindström provided a [presentation](20201103/20201103-OIDC-Sweden.pdf) intended as a base for the goals and purposes of the group.

The meeting participants agreed that the current composition of the group is ideal for the initial work. Later on we may invite more collaborators.

Areas in which we need to do work comprises of:

- An attribute specification where common Swedish attributes, such as "personnummer" and HSA-ID, are defined. This specification also needs to define a set of named attribute claim sets.

- A main (deployment) profile where fundamentals are defined. This will probably be a very brief document that may build upon the [iGov](https://openid.bitbucket.io/iGov/openid-igov-profile-id1.html) OpenID Connect profile.

- OpenID Connect extension(s) for handling the use case of signing; both "direct" (as used by BankID and Freja) and "federated" as used within the Sweden Connect federation.

- The use of OpenID Connect within federations. What are the commons requirements for registration and metadata?

- A specification where we define values for vectors-of-trust [RFC8485](https://tools.ietf.org/html/rfc8485).

- Investigate the use cases for OIDC and mobile platforms.

The group agreed that the first two items (attribute specification and main profile) are the most important to focus on initially.

Freja eID has started an OIDC pilot but without support for "personnummer" attributes and only for authentication (not signing).

Stefan Santesson mentioned that we should look at use cases where for example a SAML proxy uses OIDC to authenticate users. 

Jesper Skagerberg wanted us to look at existing OIDC clients when developing the specifications.

---

Fresia Pérez Arriagada agreed to be the group's coordinator.

**Next meeting:** 2020-11-24, 13:00

