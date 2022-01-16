# ANSWER

The ANSWER interaction allows anyone to submit an answer to a blockchain. The interaction caller don't have to be the
real answer.

# Standard

The format of a ANSWER interaction is `0x{bytes(osn:q:1:AS:{answer_ipfs_cid})}`.

There are 5 items in this interaction:

- `osn`: it just means OpenSquare Network.
- `q`: it means qa collaboration.
- `1`: it means the qa spec version.
- `AS`: it's the abbreviation of ANSWER, directive to submit an answer to a blockchain.
- `answer_ipfs_cid`: IPFS CID of an [answer](../entities/answer.md) entity.

# Examples

```
osn:q:1:AS:bafybeibknoqig3k472ke56llloupmlf7g6u6xwxntje4pm2a37npb343n4
```

It will be submitted as:

```
6f736e3a713a313a41533a62616679626569626b6e6f716967336b3437326b6535366c6c6c6f75706d6c6637673675367877786e746a6534706d326133376e70623334336e34
```

# Notes

Why separate the answer submitter and answer author?

- Answer authors don’t have to pay gas fees to answer a topic.
- Answers don't even have to be submitted to a blockchain.
- Dapps implementers can submit a batch of answers in a batch transaction.
