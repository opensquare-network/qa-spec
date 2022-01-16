# Message

A message is content appended or content of an answer to a topic. It’s used when:

- a topic author misses some content or has new ideas for a topic.
- a user gives an answer to a topic.

# Standard

```json
{
  "topic": {
    "type": "string",
    "description": "IPFS CID of a topic entity"
  },
  "content": {
    "type": "string",
    "description": "An message to a topic"
  }
}
```

# Examples

```json
{
  "topic": "bafybeigvbkfmhdgnqko4ev35wfecx7exiyg35gcr7rh45ywlpw2v62itye",
  "content": "This is an message to a topic"
}
```

The corresponding IPFS CID is:

```bafybeif73b2esnqk47ghr44whqdbk526uufzysh5sfvhdugksqgr2bd4si```
