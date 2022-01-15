# APPEND

The APPEND interaction appends content to a topic. It’s used when a topic author misses some content or has new ideas
for a topic. Only a topic author can do this interaction, and can only do it to the topics created by the author.

# Standard

The format of a APPEND interaction is `0x{bytes(osn:q:1:A:{topic_ipfs_cid}:{addition_ipfs_cid})}`. It means the topic
author append an addition to an existed topic created by himself/herself.

## Items

There are 6 items in this interaction.

- osn: it just means OpenSquare Network.
- q: it means qa collaboration.
- 1: it means the qa spec version.
- A: it's the abbreviation of APPEND, directive to append an addition to a existed topic.
- topic_ipfs_cid: ipfs CID of the [topic](../entities/topic.md) to be appended.
- addition_ipfs_cid: IPFS CID of the topic [addition](../entities/addition.md).

# Examples

```
osn:q:1:A:bafybeigvbkfmhdgnqko4ev35wfecx7exiyg35gcr7rh45ywlpw2v62itye:bafybeidzruwvbbhhohll7mif5rbuupkfoeeltjf6bi3meristpx7milt2a
```

It will be submitted as:

```
6f736e3a713a313a413a626166796265696776626b666d6864676e716b6f346576333577666563783765786979673335676372377268343579776c707732763632697479653a62616679626569647a72757776626268686f686c6c376d69663572627575706b666f65656c746a66366269336d65726973747078376d696c743261
```

It means add an addition to topic(bafybeigvbkfmhdgnqko4ev35wfecx7exiyg35gcr7rh45ywlpw2v62itye), and the addition is
described with the following entity.

```json
{
  "topic": "bafybeigvbkfmhdgnqko4ev35wfecx7exiyg35gcr7rh45ywlpw2v62itye",
  "content": "This is an addition of a topic"
}
```
