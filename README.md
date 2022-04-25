# BloXmove Dev : Claims / Credential Exchange

BloXmove generally uses a 1-step process when requesting an action, e.g. when requesting a rental.

```javascript
export class RentalRequest implements IRentalRequest {

  constructor(vehicleDID: string,
              consumerDID: string,
              packageId: number,
              timestamp?: number,
              consumerSignature?: string,
              verifiablePresentation?: IVerifiablePresentation | string) {
    this.vehicleDID = vehicleDID;
    this.consumerDID = consumerDID;
    this.packageId = packageId;
    this.timestamp = timestamp;
    this.consumerSignature = consumerSignature;
    this.verifiablePresentation = verifiablePresentation;
  }
}
```

This allow the request to be processed immediately as the requesting participant is required to provide sufficient information for the service participant to verify her authorization.

## Alternative Flows for a Claims / Credential Exchange
### Decentralized Identity Foundation

The DIF lists several approaches for requesting and presenting credentials: https://github.com/decentralized-identity/papers/blob/master/Credential%20Exchange%20Message%20Formats%20Survey.md

The presentation exchange is described here: https://identity.foundation/presentation-exchange/ with a library in typescript: https://github.com/Sphereon-Opensource/pe-js A further sample is by the DIF https://github.com/decentralized-identity/presentation-exchange/tree/master/sample-implementation

The DIF further proposes a mechanism to describe the requested information from a validating participant to a wallet: https://identity.foundation/credential-manifest/ Their description of the exchange protocol has not advanced beyond draft status: WACI PeX (Wallet And Credential Interactions Presentation Exchange) https://identity.foundation/working-groups/claims-credentials.html#:~:text=open%20source%20implementations.-,AreWeWaciYet%3F,-Repo.

### Sphereon
https://github.com/Sphereon-Opensource/pe-js

### Hyperledger Aries
Aries has developed a series of standards (current: https://github.com/hyperledger/aries-rfcs/blob/eace815c3e8598d4a8dd7881d8c731fdb2bcc0aa/features/0037-present-proof/README.md proposed: https://github.com/hyperledger/aries-rfcs/blob/eace815c3e8598d4a8dd7881d8c731fdb2bcc0aa/features/0454-present-proof-v2/README.md superseded: https://hackmd.io/@QNKW9ANJRy6t81D7IfgiZQ/HkklVzww4?type=view that describe a flow where both parties can initiate the credential exchange. However, even if the requesting participant is initiating the exchange, the exact scope of information requested is defined by the validating participant:

<img src="https://github.com/gaganpreets529mingltech/21/blob/main/4493836318.png">

Hyperledger Aries & BBS+ Signatures

#### W3C
The https://w3c-ccg.github.io/credential-handler-api/ (draft) defines capabilities that enable third-party Web applications to handle credential requests and storage (ie. how to build Wallets for Websites).

#### uPort
uPort defines the Selective disclosure flow https://github.com/uport-project/specs/blob/develop/flows/selectivedisclosure.md for an app requesting credentials from the uPort wallet.

#### Jolocom
https://jolocom-lib.readthedocs.io/en/latest/interactionFlows.html is also defining a validator-initiated request flow for credentials:

```javascript
// An instance of an identityWallet is required at this point
const credentialRequest = await identityWallet.create.interactionTokens.request.share({
  callbackURL: 'https://example.com/authentication/',
  credentialRequirements: [{
    type: ['Credential', 'ProofOfEmailCredential'],
    constraints: []
  }],
}, password)
```
