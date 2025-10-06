# CollaboWrite ✍️

A real-time collaborative blog post editor built with GraphQL, React, React Markdown, & AWS AppSync.

Google Docs for markdown!


### Base schema

Here's the base schema:

```graphql
type Post @model {
  id: ID!
  clientId: ID!
  markdown: String!
  title: String!
  createdAt: String
}
```

We have a `Post` type that has a few properties. The most important property is the markdown. This is where we are keeping up with the state of the post.

We also have a `clientId` to properly handle GraphQL subscriptions on the client.
