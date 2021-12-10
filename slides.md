---
theme: ./theme
class: text-left
highlighter: prism
title: SvelteKit and the Content Layer
fonts:
  sans: Inter
  serif: Inter
  mono: Fira Code
lineNumbers: true
---

<dots />

<div class='max-w-screen-sm'>

# SvelteKit and the Content Layer<highlight>.</highlight>

## <highlight>Scott Spence</highlight>

Svelte London Meetup <highlight>-</highlight> Dec 2021

</div>

<style>
  h2, p {
    font-weight: bold;
    font-size: 1rem;
  }
</style>

<!--
Hi my name is Scott, I’m a developer advocate at GraphCMS

GraphCMS is a headless API content management system and, we really pride ourselves on delivering structured content at scale

We’re one of the first, if not the first headless GraphQL based CMS’

We're completely GraphQL native to this day, we’re all in on GraphQL and that’s all we provide to access content

This will be a brief history of content on the web, where we are now and where we’re going

But it's mainly about Svelte and SvelteKit
-->

---

<div grid="~ cols-2 gap-2" m="-t-2" class='place-items-center'>

<div>

# Scott Spence<highlight>.</highlight>

- Developer Advocate <highlight>@</highlight>GraphCMS
- Svelte LDN meetup organiser
- <span>Svelte Sirens
  <img class='sirens-logo' src='/assets/svelte-sirens-logo.png'/></span>
- Jamstack Conf workshop <highlight>"</highlight>Building with
  Svelte<highlight>"</highlight>
- Jamstack Explorers
- Cat dad 😻

</div>

<img class='scott-profile-pic' src='/assets/scott-profile-pic.png' alt='Scott Profile Pic' />

</div>

<style>
  ul {
    font-size: 1rem !important;
  }
  .scott-profile-pic {
    width: 60%;
  }
  .sirens-logo {
    margin-left: 0.2rem;
    display: inline-block;
    width: 6%;
  }
</style>

<!--
My name is Scott, I'm a developer advocate for GraphCMS

I'm a massive Jamstack enthusiast

I'm helping out with organising the Svelte LDN meetup, next one is Dec 13th if you're interested

Currently helping out with the Svelte Sirens project GraphCMS integration with Brittany Postma

I've recently held a workshop at Jamstack Conf, "Building with Svelte and GraphQL"

There's also a Jamstack explorers mission you can check out

I'm a cat dad
-->

---

<dots />

# Histroy Lesson<highlight>.</highlight>

<!--
So with a talk like this,

I’m going to need to bring up the past, to justify the present, to the future

First, a bit of history lesson
-->

---

<dots />

# The past<highlight>.</highlight>

<!--
Let's take a look at how things used to be

This is the not so distant past, and for some their current reality
-->

---

<dots />

<in-the-beginning />

<!--
Initially.

Using FTP to upload files to live instances.

There then became a requirement for authoring content without the need for a developer.
-->

---

<dots />

<how-it-started />

<!--
The Content Management System is born

It all started with the need to edit content online in a managed way without the need for developer intervention.
-->

---

<div v-click-hide><dots /></div>

<div grid="~ cols-2 gap-2" m="-t-2" class='place-items-center'>

Traditional CMS<highlight>.</highlight>

<v-clicks>

- Website based
- “Theme” based
- Server rendered
- Tightly coupled
- You pay for everything
- Often slow

</v-clicks>

</div>

<style>
  p {
    font-size: 3.25rem;
    font-weight: bold;
    text-align: left;
  }
  .slidev-vclick-target {
    transition: opacity 400ms ease;
  }
</style>

<!--
Taking a quick look at what a CMS was back in the day

Primarily website based, there wasn’t much of a need to have any on a mobile device

These sites were heavily theme based, you could make your own and alter them to your liking

You’d pay for everything, you were hosting this yourself, there wasn’t really CDNs back then and server space was expensive

A lot of the things which made it slow were those round trips to the database back to the page
-->

---

<dots rgColor="#dee2ed" rgBgColor="#ffffff" />

<og-cms-solutions />

<style>
  div {
    background-color: #fff;
  }
</style>

<!--
Some of the tools from back then included the likes of Drupal, Wordpress and Adobe Experience manager

These are now what’s referred to as the monolith

As someone who is relatively new to web development these technologies were still present in my daily workflow at the agencies I worked at

Let’s not dwell on those though!

Although I do acknowledge these tools are still used across a lot of the web now!
-->

---

<dots />

# The present<highlight>.</highlight>

<!--
That bring us to the present

So let’s talk about the present and where we are now
-->

---

<dots />

# Terminology<highlight>.</highlight>

<!--
But first

Let’s talk terminology
-->

---

<dots />

# Buzzwords<highlight>.</highlight>

<!--
About buzzwords
-->

---

<dots />

# Hype<highlight>.</highlight>

<!--
And hype

Don’t worry I’m not going to be talking about web 3

But while I’m talking about naming things
-->

---

<dots />

# Headless<highlight>.</highlight>

<!--
Slight tangent here, I’m sure the majority of you have heard the term serverless...

Serverless because you’re not making call to specific servers, you’re making calls to APIs

You’re making call to specific APIs

These abstract away the servers from you whilst guaranteeing uptime and reliability + scalability, etc
-->

---

<div v-click-hide><dots /></div>

<div grid="~ cols-2 gap-2" m="-t-2" class='place-items-center'>

# Serverless<highlight>.</highlight>

<v-clicks>

- No calls to servers
- Calling an API
- Abstracts away the server
- Guaranteeing uptime and reliability

</v-clicks>

</div>

<style>
  p {
    font-size: 3.25rem;
    font-weight: bold;
    text-align: left;
  }
  .slidev-vclick-target {
    transition: opacity 400ms ease;
  }
</style>

---

<dots />

# Headless <highlight> = </highlight> Serverless<highlight>.</highlight>

<!--
So, in the terms of headless no server === serverless right?
-->

---
class: text-center
---

🤷

<style>
  p {
    font-size: 6rem;
  }
</style>

<!--
Anyway moving on
-->

---

<dots />

# The Present<highlight>.</highlight>

<!--
Back to the present!

So, let’s talk about JavaScript and how much it has really matured over the recent years

It’s now like a runtime for the web in the browser

And we, as developers can do a lot more in the browser
-->

---

<how-its-going />

<!--
Headless is decoupled from the monolith.

This means as a developer all you need to worry about on the client is how to present the data

This is where content is outgrowing the internet

Destinations for content are growing every day.

Destinations like, Websites, Apps, In-store displays, cars, fridges, etc.

The headless CMS solved the problem of omni-channel content distribution

Where a developer can request the data on any client
-->

---

<div v-click-hide><dots /></div>

<div grid="~ cols-2 gap-2" m="-t-2" class='place-items-center'>

Headless CMS<highlight>.</highlight>

<v-clicks>

- Frontend agnostic
- Mostly CRUD
- Decoupled
- Developer flexibility
- CI/CD with Git

</v-clicks>

</div>

<style>
  p {
    font-size: 3.25rem;
    font-weight: bold;
    text-align: left;
  }
  .slidev-vclick-target {
    transition: opacity 400ms ease;
  }
</style>

<!--
So, headless...

So what is a headless CMS

Gives developers a lot of flexibility to implement what why like
-->

---

<dots />

# The Future<highlight>.</highlight>

<!--
Let's talk about where we're going

Briefly
-->

---

<div v-click-hide><dots /></div>

<div grid="~ cols-2 gap-2" m="-t-2" class='place-items-center'>

# GraphQL<highlight>.</highlight>

<v-clicks>

- Simple to understand
- You get what you see
- Client or Server Side

</v-clicks>

</div>

<style>
  p {
    font-size: 3.25rem;
    font-weight: bold;
    text-align: left;
  }
  .slidev-vclick-target {
    transition: opacity 400ms ease;
  }
</style>

<!--
GraphQL simple to understand

You get what you see and what you request

Can be used on the client or server side
-->

---

```graphql {all|2,11|3-7|8-11|all}
query {
  products {
    # from GraphCMS
    name
    description {
      richtext
    }
    # from 3rd party API
    inventory {
      inStock
    }
    # rest of query
  }
}
```

<style>
  span {
    font-size: 1.25rem;
    line-height: 1.5;
  }
  h2 {
    margin-top: -25px;
  }
</style>

<!--
Here's a GraphQL query, and an example of how content federation will work in GraphCMS

content federation is a fancy term for bringing together data from various sources

anyway I'm here to talk about Svelte and how that fits in here
-->

---

<dots rgColor="#f5487fff" />

# Svelte<highlight>.</highlight>

<!--
Ok, so let's talk about Svelte and it's position here
-->

---

<dots rgColor="#f5487fff" />

# SvelteKit<highlight>.</highlight>

<!--
When I say Svelte what I'm actually referring to is SvelteKit

SvelteKit will eventually be the way all new projects are made with Svelte

Still in public beta

here's how to get started with Svelte
-->

---

```bash
npm init svelte@next new-svelte-project
```

<style>
  span {
    font-size: 2rem;
    line-height: 1.5;
  }
</style>

<!--
Once SvelteKit goes v1 this will change to
-->

---

```bash
npm init svelte new-svelte-project
```

<style>
  span {
    font-size: 2rem;
    line-height: 1.5;
  }
</style>

<!--
This

The @next will go away

This will be the way to start a new Svelte project

I'm sure everyone is familiar with Svelte here, here's the layout of a typical Svelte file
-->

---

## `src/routes/index.svelte`

<br>

```js {all|1,3|2|5|7-11|all}
<script>
  let name = 'world';
</script>

<h1>Hello {name}!</h1>

<style>
  h1 {
    font-size: 3rem;
  }
</style>
```

<style>
  span {
    font-size: 1.25rem;
    line-height: 1.5;
  }
  h2 {
    margin-top: -25px;
  }
</style>

<!--
Superset of html
-->

---

## `src/routes/index.svelte`

<br>

```js
<script context="module">
  export const load = async ({ fetch }) => {
    return {
      props: incomingProps,
    }
  }
</script>

<script>
  export let incomingProps
</script>

<h1>{incomingProps.title}</h1>
```

<style>
  span {
    font-size: 1.25rem;
    line-height: 1.5;
  }
  h2 {
    margin-top: -25px;
  }
</style>

<!--
This is a a way to get data from an API endpoint to return to the page
-->

---

<dots />

# SvelteKit and GraphQL<highlight>.</highlight>

---

<dots />

# Client Side<highlight>.</highlight>

---

<dots rgColor="#dee2ed" rgBgColor="#ffffff" />

<graphql-clients />

<style>
  div {
    background-color: #fff;
  }
</style>

---

<dots />

# URQL<highlight>.</highlight>

<img
  class="urql"
  src="/assets/urql-logo.svg"
  alt="urql logo"
/>

<style>
.urql {
  position: absolute;
  left: 510px;
  top: 170px;
  width: 20%;
}
</style>

<!--
So, let's take a look at how we'd go about using GraphQL with a Svelte project

We can start by taking a look at a client site GraphQL library like URQL

URQL

Or Universal React Query Library is a great GraphQL client with Svelte bindings

An URQL client can be initialised anywhere in the Svelte project

a __layout.svelte component is a good place to have the client as it will be available throughout the project

Kind of like how you would do a content provider in React but with a lot less boilerplate
-->

---

## `src/routes/__layout.svelte`

<br>

```js {all|1,6|2|3-5|8,10|9|all}
<script>
  import { initClient } from '@urql/svelte'
  initClient({
    url: import.meta.env.VITE_GRAPHQL_URL,
  })
</script>

<main>
  <slot />
</main>
```

<style>
  span {
    font-size: 1.25rem;
    line-height: 1.5;
  }
</style>

<!--
The __layout.svelte file can be used for persisted components like a navbar and footer

This is also where global styles can be added

You can think of a slot much like you would wrap React children in a react component

I'm not going to be making comparisons between React and Svelte
-->

---

## Svelte debug 👀

<br>

```js
<pre>{JSON.stringify($posts, null, 2)}</pre>
```

<style>
  span {
    font-size: 1.25rem;
    line-height: 1.5;
  }
</style>

<!--
One of my favourite ways to visualise data coming into a svelte component

After the script tag in the body of the page

I can add this to see what the data looks like from URQL

The $ on posts there is subscribing to any changes in the data from the URQL operation store

That gives some output like this
-->

---

## `src/routes/index.svelte`

<br>

```js {all|12|all}
<script>
  import { gql, operationStore, query } from '@urql/svelte'
  const postsQuery = gql`
    query Posts {
      # posts GraphQL query here
    }
  `
  const posts = operationStore(postsQuery)
  query(posts)
</script>

<pre>{JSON.stringify($posts, null, 2)}</pre>
```

<style>
  span {
    font-size: 1.25rem;
    line-height: 1.5;
  }
</style>

<!--
You can then write your queries into the URQL operation store to create a subscription to the data
-->

---

## URQL output on `localhost:3000/`

<br>

```json {all|3|all}
{
  "stale": false,
  "fetching": false,
  "data": {
    "posts": [
      {
        // posts data
      }
    ]
  }
}
```

<style>
  span {
    font-size: 1.25rem;
    line-height: 1.5;
  }
</style>

<!--
Here we get some additional properties in the URQL data response

This is where this fetching property comes in handy
-->

---

<!-- # `src/routes/index.svelte` -->

# src<highlight>/</highlight>routes<highlight>/</highlight>index<highlight>.</highlight>svelte

<style>
  h1 {
    /* display: inline-block; */
    padding: 0 1rem;
    text-align: center;
    font-family: "Victor Mono";
    background-color: #1d3a52;
    border-radius: 0.25em;
    /* font-weight: 300; */
}
</style>

---
layout: two-cols-code
---

```js {1-10}
<script>
  import { gql, operationStore, query } from '@urql/svelte'
  const postsQuery = gql`
    query Posts {
      # posts GraphQL query here
    }
  `
  const posts = operationStore(postsQuery)
  query(posts)
</script>

{#if $posts.fetching}
  <p>Loading...</p>
{:else if $posts.error}
  <p>Error! {$posts.error.message}</p>
{:else}
  <ul>
    {#each $posts.data.posts as post}
      <li>
        <a href={`/posts/${post.slug}`}>
          {post.title}
        </a>
      </li>
    {/each}
  </ul>
{/if}
```

::right::

<v-clicks>

<div class="right">

```js {1-10}
<script>
  import { gql, operationStore, query } from '@urql/svelte'
  const postsQuery = gql`
    query Posts {
      # posts GraphQL query here
    }
  `
  const posts = operationStore(postsQuery)
  query(posts)
</script>
```

</div>

</v-clicks>

<style>
  .right pre * span {
    font-size: 0.9rem;
    line-height: 1.5;
  }
  span {
    font-size: 0.5rem;
    line-height: normal;
  }
</style>

<!--
You can then write your queries into the URQL operation store to create a subscription to the data

Here we can use some of the Svelte expressions to work through the URQL response

URQL has the fetching state built into it so you can check before rendering
-->

---
layout: two-cols-code
---

```js {12-26}
<script>
  import { gql, operationStore, query } from '@urql/svelte'
  const postsQuery = gql`
    query Posts {
      # posts GraphQL query here
    }
  `
  const posts = operationStore(postsQuery)
  query(posts)
</script>

{#if $posts.fetching}
  <p>Loading...</p>
{:else if $posts.error}
  <p>Error! {$posts.error.message}</p>
{:else}
  <ul>
    {#each $posts.data.posts as post}
      <li>
        <a href={`/posts/${post.slug}`}>
          {post.title}
        </a>
      </li>
    {/each}
  </ul>
{/if}
```

::right::

<div class="right">

```js {all|1,15|2|3-4|5|6-14|all}
{#if $posts.fetching}
  <p>Loading...</p>
{:else if $posts.error}
  <p>Error! {$posts.error.message}</p>
{:else}
  <ul>
    {#each $posts.data.posts as post}
      <li>
        <a href={`/posts/${post.slug}`}>
          {post.title}
        </a>
      </li>
    {/each}
  </ul>
{/if}
```

</div>

<style>
  .right pre * span {
    font-size: 0.9rem;
    line-height: 1.5;
  }
  span {
    font-size: 0.5rem;
    line-height: normal;
  }
</style>

<!--
Here we can use some of the Svelte expressions to work through the URQL response

URQL has the fetching state built into it so you can check before rendering
-->

---

<dots />

# Houdini<highlight>.</highlight>

<img class="houdini" src="/assets/houdini.png" alt="houdini logo" />

<style>
.houdini {
  position: absolute;
  left: 400px;
  top: 190.7px;
  width: 36.2%;
}
</style>

---

<dots />

# But<highlight>.</highlight>

<!--
But!
-->

---
preload: false
---

<dots />

# Butt<highlight>.</highlight>

<butt />

<!--
And it's a big butt!
-->

---

<dots />

# Leaking Credentials<highlight>.</highlight>

<!--
So that's great n' all but what about sensitive information?

I'm talking about authentication tokens, etc

Before I get into that, did I tell you that Svelte has file-based routing?

Let's take a quick look at Svelte routing
-->

---

<dots />

# SvelteKit routes<highlight>.</highlight>

<!--
SvelteKit uses a file-based routing system much like NextJS

These routes can also be turned into endpoints

Let's take a quick look at a project file structure using file-based routing
-->

---

```text {all|7|6|4|5|all}
new-svelte-project/
├─ src/
│ ├─ routes/
│ │ └─ posts/
│ │   └─ [slug].svelte
│ ├─ __layout.svelte
│ └─ index.svelte
... rest of project files
```

<style>
  span {
    font-size: 2rem;
    line-height: 1.5;
  }
</style>

---

<dots />

# SvelteKit endpoints<highlight>.</highlight>

<!--
Let's take a look at how SvelteKit can be used to create endpoints
-->

---

```text {all|6|all}
new-svelte-project/
├─ src/
│ ├─ routes/
│ │ └─ posts/
│ │   ├─ [slug].svelte
│ │   └─ index.json.js
│ ├─ __layout.svelte
│ └─ index.svelte
... rest of project files
```

<style>
  span {
    font-size: 2rem;
    line-height: 1.5;
  }
</style>

<!--
This is how you can define an endpoint in SvelteKit

The dot json dot js notation is a bit funky but let's just roll with it for now

We'll also pop a GraphQL client in a lib folder here
-->

---

```text {all|3-4|all}
new-svelte-project/
├─ src/
│ ├─ lib/
│ │ └─ graphql-client.js
│ ├─ routes/
│ │ └─ posts/
│ │   ├─ [slug].svelte
│ │   └─ index.json.js
│ ├─ __layout.svelte
│ └─ index.svelte
```

<style>
  span {
    font-size: 2rem;
    line-height: 1.5;
  }
  div {
    margin-top: -10px;
  }
</style>

<!--
So, in here we have a lib folder where we're defining a GraphQL client

Looks a little something like this
-->

---

## `src/lib/graphql-client.js`

<br>

```js {all|1|2|4|all}
import { GraphQLClient } from 'graphql-request'
const GRAPHQL_ENDPOINT = import.meta.env.VITE_GRAPHQL_API

export const client = new GraphQLClient(GRAPHQL_ENDPOINT)
```

<style>
  span {
    font-size: 1rem;
    line-height: 1.25;
  }
</style>

<!--

-->

---

## `src/routes/posts/index.json.js`

<br>

```js {all|1-2|4,23|5,17,22|6-10|11|13-16|all}
import { client } from '$lib/graphql-client'
import { gql } from 'graphql-request'

export const get = async (req, res) => {
  try {
    const query = gql`
      query Posts {
        # posts GraphQL query here 
      }
    `
    const { posts } = await client.request(query)

    return {
      status: 200,
      body: { posts },
    }
  } catch (error) {
    return {
      status: 500,
      body: { error: error.message },
    }
  }
}
```

<style>
  span {
    font-size: 0.95rem;
    line-height: 1.25;
  }
  h2 {
    margin-top: -25px;
  }
</style>

<!--
So with endpoints you can create REST methods

get, put, del etc

del because delete is a reserved word in JavaScript

This endpoint can then be accessed from the client via a browser fetch call

Let's take a look at how that works
-->

---

## `src/index.svelte`

<br>

```js {all|1,11|2,10|3|4-9|all}
<script context="module">
  export const load = async ({ fetch }) => {
    const res = await fetch('/posts.json')
    if (res.ok) {
      const posts = await res.json()
      return {
        props: posts,
      }
    }
  }
</script>
```

<style>
  span {
    font-size: 1.25rem;
    line-height: 1.5;
  }
</style>

<!--
Context module means it runs before the page loads
-->

---

## `src/index.svelte`

<br>

```js {all|2|all}
<script>
  export let posts
</script>
```

<style>
  span {
    font-size: 1.25rem;
    line-height: 1.5;
  }
</style>

<!--
The props from the load function are passed to the page with export let

Then you can work with it much the same as with the URQL example
-->

---

## `src/index.svelte`

<br>

```js {all|2,11|4-9|7|all}
<ul>
  {#each posts as post}
    <li>
      <h2>{post.title}</h2>
      <p>{post.excerpt}</p>
      <a
        sveltekit:prefetch
        href={`/posts/${post.slug}`}>Read the Post</a
      >
    </li>
  {/each}
</ul>
```

<style>
  span {
    font-size: 1.25rem;
    line-height: 1.5;
  }
  h2 {
    margin-top: -25px;
  }
</style>

<!--
Take note of the prefetch here, this will call the load function of the route
-->

---

# Bearer token<highlight>.</highlight>

<!--
What about the credentials?
-->

---

## `src/lib/graphql-client.js`

<br>

```js {all|2-3,5|7-9|all}
import { GraphQLClient } from 'graphql-request'
const GRAPHQL_ENDPOINT = import.meta.env.VITE_GRAPHQL_API
const POST_TOKEN = import.meta.env.VITE_POST_TOKEN

export const client = new GraphQLClient(GRAPHQL_ENDPOINT)

export const postClient = new GraphQLClient(GRAPHQL_ENDPOINT, {
  headers: { Authorization: `Bearer ${POST_TOKEN}` },
})
```

<style>
  span {
    font-size: 0.8rem;
    line-height: 1.25;
  }
</style>

---

## `src/routes/posts/add-post.js`

<br>

```js {all|1|4|5|6-13|14-16|18|22|all}
import { postClient } from '$lib/graphql-client'
import { gql } from 'graphql-request'

export const post = async req => {
  const { title, content, etc } = req.body
  const query = gql`
    mutation AddPost(
      # posts GraphQL mutation here
      ) {
        id
      }
    }
  `
  const variables = {
    // variables
  }

  const id = await postClient.request(query, variables)

  return {
    status: 200,
    body: id,
  }
}
```

<style>
  span {
    font-size: 0.8rem;
    line-height: 1.25;
  }
  h2 {
    margin-top: -25px;
  }
</style>

<!--
This should all be in a try catch, but I want to get all the code on the screen

That's it.
-->

---

# Closing Comments<highlight>.</highlight>

---

<div grid="~ cols-2 gap-2" m="-t-2" class='place-items-center'>

# SvelteKit<highlight>.</highlight>

🏆

</div>

<style>
  p {
    font-size: 6rem;
  }
</style>

---

<dots />

# <highlight color="#253889ff">graphcms.com/blog</highlight>

# <highlight color="#253889ff">graphcms.com/docs</highlight>

---

<dots />

# <highlight>@</highlight>spences10 <highlight color="#253889ff"><mdi-github /> <mdi-twitter-circle /></highlight>

# scottspence<highlight>.</highlight>com <highlight color="#253889ff"><mdi-web /></highlight>

---

<dots />

# <highlight color="#253889ff">sveltekit-and-the-content-layer.vercel.app</highlight>

---

<dots />

# Thank you<highlight>.</highlight>
