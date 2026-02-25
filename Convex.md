## Functions

Functions are the ways to create APIs that are accessible by the frontend. The different kind of functions are: Queries, Mutations, and Actions
- Queries:  Reads data from your Convex database and are automatically cached. They fetch data from the database, check authentication or perform other business logic, and return data back to the client application
- Mutations: writes data to the database and runs as a transaction
- Actions: used for external API calls like OpenAI, Stripe, Twilio. Do not have database access


HTTP Actions are used to create HTTP APIs as functions
```
import { httpRouter } from "convex/server";
import { httpAction } from "./_generated/server";

const http = httpRouter();

http.route({
  path: "/",
  method: "GET",
  handler: httpAction(async (ctx, request) => {
    return new Response(`Hello from ${request.url}`);
  }),
});
export default http;
```

## Schemas

Use v from convex/values to define schemas in schema.ts