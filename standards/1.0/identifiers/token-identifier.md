# Token identifier

There are 2 kinds of token identifiers.

1. N. It means the chain native token. For example, KSM for kusama/statemine, DOT for polkadot/statemint.
2. A U32 number. It identifies the asset on statemine/statemint. This is used with blockchain context, for example 8 at
   height 500,000 means the RMRK token. For 8 at height 10,000, it's invalid because RMRK does not exist at that height.

Examples:

- 'N' on kusama means the KSM token.
- 'N' on polkadot means the DOT token.
- 8 on statemine at height 500,000 means the RMRK token.
