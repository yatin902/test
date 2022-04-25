# BloXmove Dev : Use of BBS+ signatures
Should it be used in the bloxmove system ?

To derive certain fields of a VC, VCs must be signed with the signature type: BbsBlsSignature2020

- Accordingly to the Spherity API, this type is not supported as of now to issues this kind of VCs
- Also i could not find a way to issue VCs based on this signature type with the plain ethereum stack which is used currently in the bloxmove system
- If there would be a way to use ethereum keys to issue this type of signature, the asset lib needs a whole refactoring and we need a library then (e.g. →https://github.com/mattrglobal/jsonld-signatures-bbs )
- Also documentation of this signatures are often still in draft mode (e.g. https://w3c-ccg.github.io/ldp-bbs2020/#the-bbs-signature-proof-suite-2020 )
- And this one was published in August this year → https://mattrglobal.github.io/bbs-signatures-spec/

Conclusion:
I am not sure what the current benefits are, if we use this type of signatures in this early state.
There could be more problems than benefits.
