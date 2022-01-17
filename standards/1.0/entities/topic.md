# Topic

A topic is just a topic for discussion. It can be a question, poll, piece of news, etc.

# Standard

```json
{
  "title": {
    "type": "string",
    "description": "Title of topic"
  },
  "content": {
    "type": "string",
    "description": "Content of topic"
  }
}
```

The `title` and `content` fields are mandatory. Implementers can add extra fields to help their businesses, for example,
languages, category, etc.

# Examples

```json
{
  "title": "This is the title",
  "content": "This is the content",
  "language": "en"
}
```

The `language` is an extra field to help get topic language.

The corresponding IPFS CID is:

```
bafybeigvbkfmhdgnqko4ev35wfecx7exiyg35gcr7rh45ywlpw2v62itye
```
