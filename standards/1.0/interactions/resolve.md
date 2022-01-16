# RESOLVE

The RESOLVE interaction allows a topic author/supporter to resolve a topic created. The prerequisite is that the
author/supporter has call the [NEW](./new.md)/[SUPPORT](./support.md) interaction to this topic before.

# Standard

The format of a RESOLVE interaction is `0x{bytes(osn:q:1:R:{topic_ipfs_cid})}`. It means the extrinsic caller resolves a
topic created/supported by himself/herself. The caller should be one of the corresponding NEW/SUPPORT interactions
callers.

There are 5 items in this interaction:

- `osn`: it just means OpenSquare Network.
- `q`: it means qa collaboration.
- `1`: it means the qa spec version.
- `R`: it's the abbreviation of RESOLVE, directive to resolve an existed topic.
- `topic_ipfs_cid`: IPFS CID of a [topic](../entities/topic.md) entity.

# Examples

```
osn:q:1:R:bafybeigvbkfmhdgnqko4ev35wfecx7exiyg35gcr7rh45ywlpw2v62itye
```

It will be submitted as:

```
0x6f736e3a713a313a523a626166796265696776626b666d6864676e716b6f346576333577666563783765786979673335676372377268343579776c70773276363269747965
```

# Notes

- An author/supporter can resolve a topic at any time even he/she didn't fund all the promised amount of token. It
  depends on the dapps implementers to decide how to handle it, for example:
    - a dapp may reduce the author/supporter credit score because of the promise break.
    - a dapp will do nothing, just show the author/support history behavior records and leave the decisions to the end
      users to decide whether to collaborate with the author/supporter.
- A topic will be resolved when the author and call supporters resolve it. Supports won't be accepted after a topic is
  resolved.
