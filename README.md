# OpenSquare QA Specification and Standards

This repository hosts standards for creating and interacting with questions and answers in the OpenSquare collaboration
platform.

There are three types of standards: _entities_, identifiers and _interactions_. Entities are definitions for how a paid
question should be declared and how answers should be given and declared, so that tools can recognize them as valid.
Identifiers are definitions to help user recognize what and how many tokens are promised to be awarded. Interactions are
interactions between the off-chain world and the OpenSquare Paid QA protocol, between topics and answers.

## Interactions

The standards currently cover the following basic interactions:

- [NEW](./standards/1.0/interactions/new.md) creates a new paid topic with a promise to award at least some amount of
  tokens.
- [APPEND](./standards/1.0/interactions/append.md) allows a topic author to append content to an existed topic.
- [SUPPORT](./standards/1.0/interactions/support.md) allows anyone to grant extra fund to an existed topic.
- [ANSWER](./standards/1.0/interactions/answer.md) submits an answer to a blockchain. The submitted answer is signed by
  the author.
- [FUND](./standards/1.0/interactions/fund.md) funds an answer or a topic immediately.
- [RESOLVE](./standards/1.0/interactions/resolve.md) allows a topic author or supporter to resolve a topic.

## Entities

Entities are a group of stuffs for QA collaboration, while they are usually related to the QA content.

- [topic](./standards/1.0/entities/topic.md) is a topic to be discussed, or a question the author expect an answer.
- [message](./standards/1.0/entities/message.md) is a piece of content a topic author want to append to the topic.
- [answer](./standards/1.0/entities/answer.md) is an answer signed with the author. It can be submitted to a blockchain
  by anyone.

## Identifiers

Identifiers help recognize the promised awarded token and amount.
