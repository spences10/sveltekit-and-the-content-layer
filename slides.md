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

# SvelteKit and the Content Layer<hl>.</hl>

## <hl>Scott Spence</hl>

Svelte London Meetup <hl>-</hl> Dec 2021

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

# Scott Spence<hl>.</hl>

- Developer Advocate <hl>@</hl>GraphCMS
- Svelte LDN meetup organiser
- <span>Svelte Sirens
  <img class='sirens-logo' src='/assets/svelte-sirens-logo.png'/></span>
- Workshop <hl>"</hl>Building with Svelte and
  GraphQL<hl>"</hl>
  - Jamstack Conf
  - GraphQL Galaxy
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

# Histroy Lesson<hl>.</hl>

<!--
So with a talk like this,

I’m going to need to bring up the past, to justify the present, to the future

First, a bit of history lesson
-->

---

<dots />

# The past<hl>.</hl>

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

Traditional CMS<hl>.</hl>

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

# The present<hl>.</hl>

<!--
That bring us to the present

So let’s talk about the present and where we are now
-->

---

<dots />

# Terminology<hl>.</hl>

<!--
But first

Let’s talk terminology
-->

---

<dots />

# Buzzwords<hl>.</hl>

<!--
About buzzwords
-->

---

<dots />

# Hype<hl>.</hl>

<!--
And hype

Don’t worry I’m not going to be talking about web 3

But while I’m talking about naming things
-->

---

<dots/>

# Tangent time<hl>!</hl>

---

<div v-click-hide><dots /></div>

<div grid="~ cols-2 gap-2" m="-t-2" class='place-items-center'>

# Serverless<hl>.</hl>

<v-clicks>

- Not making calls to specific servers
- Making calls to an API
- API abstracts away the server
- Guaranteeing uptime and reliability + scalability + all that jazz

</v-clicks>

</div>

<style>
  li {
    line-height: 1em !important;
    padding-bottom: 1.5rem;
  }
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

<div v-click-hide><dots /></div>

<div grid="~ cols-2 gap-2" m="-t-2" class='place-items-center'>

# Headless<hl>.</hl>

<v-clicks>

- Not making calls to specific servers
- Making calls to an API
- API abstracts away the server
- Guaranteeing uptime and reliability + scalability + all that jazz

</v-clicks>

</div>

<style>
  li {
    line-height: 1em !important;
    padding-bottom: 1.5rem;
  }
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
Slight tangent here, I’m sure the majority of you have heard the term serverless...

Serverless because you’re not making call to specific servers, you’re making calls to APIs

You’re making call to specific APIs

These abstract away the servers from you whilst guaranteeing uptime and reliability + scalability, etc
-->

---

<dots />

# Headless <hl> = </hl> Serverless<hl>?</hl>

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

# The Present<hl>.</hl>

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

Headless CMS<hl>.</hl>

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

# The Future<hl>.</hl>

<!--
Let's talk about where we're going

Briefly
-->

---

<div v-click-hide><dots /></div>

<div grid="~ cols-2 gap-2" m="-t-2" class='place-items-center'>

# GraphQL<hl>.</hl>

<v-clicks>

- Simple to understand
- You get what you ask for
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

# Svelte<hl>.</hl>

<!--
Ok, so let's talk about Svelte and it's position here
-->

---

<dots rgColor="#f5487fff" />

# SvelteKit<hl>.</hl>

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

<dots />

# SvelteKit and GraphQL<hl>.</hl>

---

<dots />

# Client Side<hl>.</hl>

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

# URQL<hl>.</hl>

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

```js {all|1,6|2|3-5|8-10|all}
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
    query AllPosts {
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

# src<hl>/</hl>routes<hl>/</hl>index<hl>.</hl>svelte

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
    query AllPosts {
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

```js {1-13}
<script>
  import { gql, operationStore, query } from '@urql/svelte'
  const postsQuery = gql`
    query AllPosts {
      posts {
        title
        slug
      }
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
    query AllPosts {
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

# Houdini<hl>.</hl>

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
layout: two-cols-code
---

`bash`

```bash
npx houdini generate
```

::right::

`src/environment.js`

<div class="right">

```js {all|8|20|all}
import { Environment } from '$houdini'
const GRAPHQL_API = import.meta.env.VITE_GRAPHQL_API

export default new Environment(async function ({
  text,
  variables = {},
}) {
  const result = await this.fetch(GRAPHQL_API, {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
    },
    body: JSON.stringify({
      query: text,
      variables,
    }),
  })

  // parse the result as json
  return await result.json()
})
```

</div>

<style>
  .right pre * span {
    font-size: 0.8rem;
    line-height: 1;
  }
  span {
    font-size: 1rem;
    line-height: normal;
  }
</style>

---

## `src/routes/__layout.svelte`

<br>

```js {all|2-3|5|8-10|all}
<script context="module">
  import { setEnvironment } from '$houdini'
  import env from '../environment'

  setEnvironment(env)
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

---

# src<hl>/</hl>routes<hl>/</hl>index<hl>.</hl>svelte

<style>
  h1 {
    padding: 0 1rem;
    text-align: center;
    font-family: "Victor Mono";
    background-color: #1d3a52;
    border-radius: 0.25em;
}
</style>

---
layout: two-cols-code
---

```js {1-12}
<script>
  import { graphql, query } from '$houdini'
  const { data } = query(graphql`
    query AllPosts {
      posts {
        title
        slug
      }
    }
  `)
  const { posts } = $data
</script>

<ul>
  {#each posts as post}
    <li>
      <a
        sveltekit:prefetch
        href={`/posts/${post.slug}`}
      >
        {post.title}
      </a>
    </li>
  {/each}
</ul>
```

::right::

<v-clicks>

<div class="right">

```js {1-12}
<script>
  import { graphql, query } from '$houdini'
  const { data } = query(graphql`
    query AllPosts {
      posts {
        title
        slug
      }
    }
  `)
  const { posts } = $data
</script>
```

</div>

</v-clicks>

<style>
  span {
    font-size: 0.65rem;
    line-height: 1;
  }
  .right pre * span {
    font-size: 0.8rem;
    line-height: normal;
  }
</style>

<!--

-->

---
layout: two-cols-code
---

```js {14-25}
<script>
  import { graphql, query } from '$houdini'
  const { data } = query(graphql`
    query AllPosts {
      posts {
        title
        slug
      }
    }
  `)
  const { posts } = $data
</script>

<ul>
  {#each posts as post}
    <li>
      <a
        sveltekit:prefetch
        href={`/posts/${post.slug}`}
      >
        {post.title}
      </a>
    </li>
  {/each}
</ul>
```

::right::

<div class="right">

```js {1-12}
<ul>
  {#each posts as post}
    <li>
      <a
        sveltekit:prefetch
        href={`/posts/${post.slug}`}
      >
        {post.title}
      </a>
    </li>
  {/each}
</ul>
```

</div>

<style>
  .right pre * span {
    font-size: 0.8rem;
    line-height: normal;
  }
  span {
    font-size: 0.65rem;
    line-height: 1;
  }
</style>

<!--

-->

---

<dots />

# But<hl>.</hl>

<!--
But!
-->

---
preload: false
---

<dots />

# Butt<hl>.</hl>

<butt />

<!--
And it's a big butt!
-->

--- 

<dots />

# Leaking Credentials<hl>.</hl>

<!--
So that's great n' all but what about sensitive information?

I'm talking about authentication tokens, etc

Before I get into that, did I tell you that Svelte has file-based routing?

Let's take a quick look at Svelte routing
-->

---
preload: false
---

<video autoplay>
  <source src="/assets/bearer-token-in-sveltekit.mp4" type="video/mp4">
</video>

---

<dots />

# SvelteKit routes<hl>.</hl>

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

# SvelteKit endpoints<hl>.</hl>

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

```js {all|1|2|3|5-7|6|all}
import { GraphQLClient } from 'graphql-request'
const GRAPHQL_ENDPOINT = import.meta.env.VITE_GRAPHQL_API
const SECRET_TOKEN = import.meta.env.VITE_SECRET_TOKEN

export const client = new GraphQLClient(GRAPHQL_ENDPOINT, {
  headers: { Authorization: `Bearer ${SECRET_TOKEN}` },
})
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

# src<hl>/</hl>routes<hl>/</hl>posts<hl>/</hl>index<hl>.</hl>json<hl>.</hl>js

<style>
  h1 {
    padding: 0 1rem;
    font-size: 3rem !important;
    text-align: center;
    font-family: "Victor Mono";
    background-color: #1d3a52;
    border-radius: 0.25em;
}
</style>


---
layout: two-cols-code
---

```js {20-25}
import { client } from '$lib/graphql-client'
import { gql } from 'graphql-request'

export const get = async (req, res) => {
  try {
    const query = gql`
      query AllPosts {
        posts {
          title
          slug
          date
          excerpt
          tags
          coverImage {
            url
          }
        }
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

::right::

<div class="right">

```js
const { posts } = await client.request(query)

return {
  status: 200,
  body: { posts },
}
```

</div>

<style>
  pre {
    zoom: 59.9%;
  }
  span {
    font-size: 1rem;
    display: inline-block !important;
    line-height: 1.35;
  }
  .right pre * span {
    font-size: 1.5rem;
    line-height: 1.5;
  }
  div {
    margin-top: -15px;
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

# src<hl>/</hl>routes<hl>/</hl>index<hl>.</hl>svelte

<style>
  h1 {
    padding: 0 1rem;
    text-align: center;
    font-family: "Victor Mono";
    background-color: #1d3a52;
    border-radius: 0.25em;
}
</style>

---
layout: two-cols-code
---

```js {1-11}
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

<script>
  export let posts
</script>

<ul>
  {#each posts as post}
    <li>
      <a
        sveltekit:prefetch
        href={`/posts/${post.slug}`}
      >
        {post.title}
      </a>
    </li>
  {/each}
</ul>
```

::right::

<v-clicks>

<div class="right">

```js {1-11}
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

</div>

</v-clicks>

<style>
  .right pre * span {
    font-size: 1.1rem;
    line-height: normal;
  }
  span {
    font-size: 0.65rem;
    line-height: 1;
  }
  div {
    margin-top: -15px;
  }
</style>

---
layout: two-cols-code
---

```js {13-28}
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

<script>
  export let posts
</script>

<ul>
  {#each posts as post}
    <li>
      <a
        sveltekit:prefetch
        href={`/posts/${post.slug}`}
      >
        {post.title}
      </a>
    </li>
  {/each}
</ul>
```

::right::

<div class="right">

```js {all|1-3|5-16}
<script>
  export let posts
</script>

<ul>
  {#each posts as post}
    <li>
      <a
        sveltekit:prefetch
        href={`/posts/${post.slug}`}
      >
        {post.title}
      </a>
    </li>
  {/each}
</ul>
```

</div>

<style>
  span {
    font-size: 0.65rem;
    line-height: 1.5;
  }
  .right pre * span {
    font-size: 1.1rem;
    line-height: normal;
  }
  div {
    margin-top: -15px;
  }
</style>

<!--
Context module means it runs before the page loads

The props from the load function are passed to the page with export let

Then you can work with it much the same as with the URQL example

Take note of the prefetch here, this will call the load function of the route
-->

---
preload: false
---

<video autoplay>
  <source src="/assets/bearer-token-in-sveltekit-with-endpoints.mp4" type="video/mp4">
</video>

---

# Bearer token<hl>.</hl>

<!--
What about the credentials?
-->

---

# src<hl>/</hl>routes<hl>/</hl>posts<hl>/</hl>add-post<hl>.</hl>json<hl>.</hl>js

<style>
  h1 {
    padding: 0 1rem;
    text-align: center;
    font-family: "Victor Mono";
    font-size: 2.85rem !important;
    background-color: #1d3a52;
    border-radius: 0.25em;
}
</style>

---
layout: two-cols-code
---

```js {all}
import { client } from '$lib/graphql-client'
import { gql } from 'graphql-request'

export const post = async req => {
  const { title, markdownContent } = req.body
  try {
    const query = gql`
      mutation AddPost(
        $title: String!
        $markdownContent: String!
      ) {
        createPost(
          data: {
            title: $title
            markdownContent: $markdownContent
          }
        ) {
          id
        }
      }
    `
    const variables = {
      title,
      markdownContent,
    }

    const id = await client.request(query, variables)

    return {
      status: 200,
      body: id,
    }
  } catch (error) {
    return {
      status: 500,
      body: { error: error.message },
    }
  }
}
```

::right::

<div class="right">

</div>

<style>
  pre {
    zoom: 59.9%;
  }
  span {
    font-size: 1rem;
    display: inline-block !important;
    line-height: 1.35;
  }
  .right pre * span {
    font-size: 1.5rem;
    line-height: 1.5;
  }
  div {
    margin-top: -15px;
  }
</style>

---
layout: two-cols-code
---

```js {5,7-27}
import { client } from '$lib/graphql-client'
import { gql } from 'graphql-request'

export const post = async req => {
  const { title, markdownContent } = req.body
  try {
    const query = gql`
      mutation AddPost(
        $title: String!
        $markdownContent: String!
      ) {
        createPost(
          data: {
            title: $title
            markdownContent: $markdownContent
          }
        ) {
          id
        }
      }
    `
    const variables = {
      title,
      markdownContent,
    }

    const id = await client.request(query, variables)

    return {
      status: 200,
      body: id,
    }
  } catch (error) {
    return {
      status: 500,
      body: { error: error.message },
    }
  }
}
```

::right::

<div class="right">

```js {all|2-14|16-19|21}
const query = gql`
  mutation AddPost(
    $title: String!
    $markdownContent: String!
  ) {
    createPost(
      data: {
        title: $title
        markdownContent: $markdownContent
      }
    ) {
      id
    }
  }
`
const variables = {
  title,
  markdownContent,
}

const id = await client.request(query, variables)
```

</div>

<style>
  pre {
    zoom: 59.9%;
  }
  span {
    font-size: 1rem;
    display: inline-block !important;
    line-height: 1.35;
  }
  .right pre * span {
    font-size: 1.5rem;
    line-height: 1.5;
  }
  div {
    margin-top: -15px;
  }
</style>

<!--
This should all be in a try catch, but I want to get all the code on the screen

That's it.
-->

---

<dots />

# Closing Comments<hl>.</hl>

---

<div grid="~ cols-2" m="-t-2" class='place-items-center'>

# Closing Comments<hl>.</hl>

<v-clicks>

- Great client side tools to use
- Secure credentials on server
- Don't feel bad about using server side to secure dem creds

</v-clicks>

</div>

<style>
  p {
    font-size: 3.25rem;
    font-weight: bold;
    text-align: left;
  }
  li {
    line-height: 1em !important;
    margin-left: 0.1em !important;
    padding-bottom: 1.5rem;
  }
  .slidev-vclick-target {
    transition: opacity 400ms ease;
  }
</style>

---

<div grid="~ cols-2 gap-2" m="-t-2" class='place-items-center'>

# SvelteKit<hl>.</hl>

🏆

</div>

<style>
  p {
    font-size: 6rem;
  }
</style>

---

<dots />

# <hl color="#253889ff">graphcms.com/blog</hl>

# <hl color="#253889ff">graphcms.com/docs</hl>

---

<dots />

# <hl>@</hl>spences10 <hl color="#253889ff"><mdi-github /> <mdi-twitter-circle /></hl>

# scottspence<hl>.</hl>com <hl color="#253889ff"><mdi-web /></hl>

---

<dots />

# <hl color="#253889ff">sveltekit-and-the-content-layer.vercel.app</hl>

<style>
  h1 {
    font-size: 3.5rem !important;
  }
</style>

---

<dots />

# Thank you<hl>.</hl>
