# FUND

The FUND interaction allows a user to immediately fund an answer or a topic.

# Standard

The FUND interaction is a batch call of a system remark together with a token/asset transfer.

- the first message, A is `0x{bytes(osn:q:1:F:{ipfs_cid})}`.
- the second transaction is a token/asset transfer.

The format of FUND is thus 1 of following types:

- `utility.batch(system.remark(A), balances.transfer({target}, {any_amount_of_token}))`
- `utility.batch(system.remark(A), balances.transferKeepAlive({target}, {any_amount_of_token}))`
- `utility.batch(system.remark(A), assets.transfer({asset_id}, {target}, {any_amount_of_token}))`

Notes:

- `ipfs_cid` is the IPFS CID of an answer or a topic.
- `asset_id` locates the asset on statemine/statemint.
- `target` is the fund target address, and it should be same with the address field in the answer entity identified by
  the IPFS CID.
- `any_amount_of_token` is just any amount of token/asset.

# Examples:

A user which is either the topic author or not funds 1 DOT to an answer.

The fund message is

```
osn:q:1:F:bafybeibknoqig3k472ke56llloupmlf7g6u6xwxntje4pm2a37npb343n4
```

while `bafybeibknoqig3k472ke56llloupmlf7g6u6xwxntje4pm2a37npb343n4` is the IPFS CID of the
following [answer](../entities/answer.md) entity.

```json
{
  "answer": {
    "topic": "bafybeigvbkfmhdgnqko4ev35wfecx7exiyg35gcr7rh45ywlpw2v62itye",
    "content": "This is an answer"
  },
  "address": "HHyxCP1oWuZqdk9gneHx6RuEqXFs1SGpL51e3LS4aUoiriN",
  "signature": "0x0c54e9750cbafbf76d666151b2ec1a61035b8b1234e105dbb381aa5c564a753d16a1fbdd6ade7e89d4c09391d7ea3aedf4932fcf439025c828c397e5900d2080"
}
```

In bytes, the fund message is:

```
0x6f736e3a713a313a463a62616679626569626b6e6f716967336b3437326b6535366c6c6c6f75706d6c6637673675367877786e746a6534706d326133376e70623334336e34
```

To complete the fund, we submit a utility.batch call comprised of two transactions:

```js
utility.batch([
  system.remark(
    0x6f736e3a713a313a463a62616679626569626b6e6f716967336b3437326b6535366c6c6c6f75706d6c6637673675367877786e746a6534706d326133376e70623334336e34
  ),
  tx.balances.transfer(HHyxCP1oWuZqdk9gneHx6RuEqXFs1SGpL51e3LS4aUoiriN, 10000000000),
]);
```
