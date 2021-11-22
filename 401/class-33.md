
## GraphQL @connection section:

#### Definition

        directive @connection(keyName: String, fields: [String!]) on FIELD_DEFINITION


#### Has one (One-to-One)

        type Project @model {
        id: ID!
        name: String
        team: Team @connection
        }

        type Team @model {
        id: ID!
        name: String!
        }


#### Has many (uni-directional One-to-Many)

        type Post @model {
        id: ID!
        title: String!
        comments: [Comment] @connection(keyName: "byPost", fields: ["id"])
        }

        type Comment @model
        @key(name: "byPost", fields: ["postID", "content"]) {
        id: ID!
        postID: ID!
        content: String!
        }


#### Belongs to (bi-directional One-to-Many)

        type Post @model {
        id: ID!
        title: String!
        comments: [Comment] @connection(keyName: "byPost", fields: ["id"])
        }

        type Comment @model
        @key(name: "byPost", fields: ["postID", "content"]) {
        id: ID!
        postID: ID!
        content: String!
        post: Post @connection(fields: ["postID"])
        }


#### Many-to-many connections

        type Post @model {
        id: ID!
        title: String!
        editors: [PostEditor] @connection(keyName: "byPost", fields: ["id"])
        }

        type PostEditor
        @model(queries: null)
        @key(name: "byPost", fields: ["postID", "editorID"])
        @key(name: "byEditor", fields: ["editorID", "postID"]) {
        id: ID!
        postID: ID!
        editorID: ID!
        post: Post! @connection(fields: ["postID"])
        editor: User! @connection(fields: ["editorID"])
        }

        type User @model {
        id: ID!
        username: String!
        posts: [PostEditor] @connection(keyName: "byEditor", fields: ["id"])
        }



**resources:** 

*[https://docs.amplify.aws/cli/graphql-transformer/connection/#connection](https://docs.amplify.aws/cli/graphql-transformer/connection/#connection)*

