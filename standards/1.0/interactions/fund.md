# FUND

The FUND interaction claims that the caller promises to fund a topic with some amount of token. It’s used when a user
finds a topic created by others interesting or useful to himself/herself. If the caller is the creator, it means the
creator will fund more to the topic.

# Standard

The format of a NEW interaction is `0x{bytes(osn:q:1:F:{token_identifier}:{token_amount}:{topic_ipfs_cid})}`. It means
the extrinsic caller promises to fund a existed topic with some amount of token.

There are 7 items in this interaction.

- osn: it just means OpenSquare Network.
- q: it means qa collaboration.
- 1: it means the qa spec version.
- F: it's the abbreviation of FUND, directive to fund a existed topic.
- token_identifier: it identifies a token, described in [token identifier](../entities/token-identifier.md) entity.
- token_amount: how many tokens to fund this topic, described at [token amount](../entities/token-amount.md) entity.
- topic_ipfs_cid: ipfs CID of a [topic](../entities/topic.md) entity.

# Examples

```
osn:q:1:F:N:1:bafybeigvbkfmhdgnqko4ev35wfecx7exiyg35gcr7rh45ywlpw2v62itye
```

It will be submitted as:

```
6f736e3a713a313a463a4e3a313a626166796265696776626b666d6864676e716b6f346576333577666563783765786979673335676372377268343579776c70773276363269747965
```

If submitted to Kusama, it will mean the caller promises to fund at least 1 KSM to the answers which solve the existed
topic described with the following topic.

```json
{
  "title": "This is the title",
  "content": "This is the content",
  "language": "en"
}
```
