# Decentralized Identities and eIDAS 
by Oliver Terbu

## Introduction
One of the main objectives of the eIDAS regulation is to foster the EU Digital Single Market. Electronic signatures and identifications should be recognized across borders to enable member states to work more closely together, lower friction, and establish new markets. eIDAS sets requirements for the mutual-recognition of electronic signatures (eSignatures/eSeals) and electronic identification (eID) to participate in this ecosystem. 

## Leverage the existing eIDAS Network

Because of its strictly regulated nature, eIDAS eSignatures and eIDs are highly trustworthy. One important problem that decentralized identity systems need to solve is how the user gets onboarded. This typically involves mitigating problems like sybil attacks, or identity theft in general. eIDAS could help to derive trusted identities to solve these issues. eIDAS provides unified interfaces for eIDs and eSignatures. By leveraging eIDAS, only one transformation process has to be implemented instead of several per member state. eIDAS is currently limited to EU member states only. Transforming or importing eIDAS eIDs and eSignatures to decentralized identity systems would allow the eIDAS network to scale globally.

eIDAS Trust Service Providers (TSP) are issuing so called Qualified Electronic Signatures (QES) which have the same legal implications as handwritten signatures. By definition, a QES is under the sole control of the user. Introducing a new type of trust service for TSPs that issue a Qualified Decentralized Identifier (QDID), a decentralized identity system could provide stronger authentication as well. The public key would correspond to a private key stored in a remote secure element and a smartphone app could be used to authorize the transaction. 
**TOPIC:** Implications for the DID specification (DIF) and Verifiable Claims data model (W3C) need to be investigated.

TSPs are trusted because they are included in a dedicated Trust Service List (TSL) published and signed by the European Commission (EC). The EC ensures that they comply with the eIDAS regulatory framework. A similar approach is used by boarder control agencies to trust foreign passports. In this case, ICAO maintains a dedicated public key directory. Trust lists allow to trust one issuer instead of multiple. Although one aspect of decentralized identity systems is to reduce the need to trust central authorities, they could still benefit from implementing specifications for trust lists. The EC could publish a trust list for DIDs of all eIDAS TSPs which could easily be imported by verifiers in order to verify a presented DID belongs to a TSP. The concept of trust lists is not limited to TSPs only but is open to be adopted by anyone who wants to play that role.
**TOPIC:** Investigate if there is the need for a specification (e.g. in DIF or/and W3C) to define trust lists, or a similar approach.

The eIDAS interoperability framework defines a unified way for all EU member states to exchange eIDs. The Interfaces are currently limited to a dedicated SAML profile with respective requests and assertions. eIDAS introduces requirements for a high level of assurance (LoA) similar to NIST SP 800-63. The LoA is determined by how the user was identified during provisioning (e.g. national ID card) and how the user authenticated (e.g. hardware security). The SAML assertions communicate the LoA which was used during the transaction.
**TOPIC:** It needs to be investigated if new specifications (e.g. in DIF or/and W3C) could help to leverage eIDAS eIDs or national eIDs in general - e.g. make room for an authentication context class reference (similar to OpenID Connect).