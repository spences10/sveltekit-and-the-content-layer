---
theme: default
class: text-left
highlighter: prism
title: SvelteKit and the Content Layer
fonts:
  sans: 'Inter'
  serif: 'Inter'
  mono: 'Fira Code'
lineNumbers: true
---

<dots />

<div class='max-w-screen-sm'>

# SvelteKit and the Content Layer<highlight>.</highlight>

## <highlight>Scott Spence</highlight>

MMT Meetup <highlight>-</highlight> Nov 2021

</div>

<style>
  h1 {
    font-weight: bold;
    margin-bottom: 4rem;
  }
  h2, p {
    font-weight: bold;
    font-size: 1rem;
  }
  p {
    margin-top: 0;
  }
</style>

<!--
Hi my name is Scott, I’m a developer advocate at GraphCMS

GraphCMS is a headless API content management system and, we really pride ourselves on delivering structured content at scale

We’re one of the first, if not the first headless GraphQL based CMS’

We're completely GraphQL native to this day, we’re all in on GraphQL and that’s all we provide to access content

This will be a brief history of content on the web, where we are now and where we’re going
-->

---
layout: cover
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
  h1 {
    font-weight: bold;
  }
  .scott-profile-pic {
    width: 60%;
  }
  .sirens-logo {
    margin-left: 0.2rem;
    display: inline-block;
    width: 6%;
  }
  ul {
    list-style: disc !important;
  }
  ::marker { 
    color: #f5487fff; 
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
layout: cover
---

<dots />

# Histroy Lesson<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
So with a talk like this,

I’m going to need to bring up the past, to justify the present, to the future

First, a bit of history lesson
-->

---
layout: cover
---

<dots />

# The past<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
Let's take a look at how things used to be

This is the not so distant past, and for some their current reality
-->

---

<dots />

<div>
<img class='filezilla' src='/assets/filezilla.png' alt='filezilla logo' />
<img class='old-website' src='/assets/old-website.png' alt='old website graphic' />
</div>

<style>
  .filezilla {
    position: absolute;
    left: 220px;
    top: 107px;
    width: 30%;
    z-index: 1;
  }
  .old-website {
    position: absolute;
    left: 450px;
    top: 150px;
    width: 30%;
    z-index: -1;
  }
</style>

<!--
Initially.

Using FTP to upload files to live instances.

There then became a requirement for authoring content without the need for a developer.
-->

---

<dots />

<div>
<img class='how-it-started' src='/assets/how-it-started-graphic.png' alt='cms graphic' />
</div>

<style>
  .how-it-started {
    position: absolute;
    left: 50px;
    top: 110px;
    width: 60%;
  }
</style>

<!--
The Content Management System is born

It all started with the need to edit content online in a managed way without the need for developer intervention.
-->

---
layout: cover
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
  ul {
    list-style: disc !important;
    font-size: 2rem;
  }
  ::marker { 
    color: #f5487fff; 
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

<v-clicks>
  <img class='drupal' src='/assets/drupal.png' alt='drupal logo' />
  <img class='wordpress' src='/assets/wordpress.png' alt='wordpress logo' />
  <img class='aem' src='/assets/adobe-experience-manager.png' alt='adobe experience manager logo' />
</v-clicks>

<style>
  div {
    background-color: #fff;
  }
  .drupal {
    position: absolute;
    left: 130px;
    top: 100px;
    width: 20%;
  }
  .wordpress {
    position: absolute;
    left: 540px;
    top: 60px;
    width: 20%;
  }
  .aem {
    position: absolute;
    left: 380px;
    top: 300px;
    width: 20%;
  }
  .slidev-vclick-target {
    transition: opacity 400ms ease;
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
layout: cover
---

<dots />

# The present<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
That bring us to the present

So let’s talk about the present and where we are now
-->

---
layout: cover
---

<dots />

# Terminology<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
But first

Let’s talk terminology
-->

---
layout: cover
---

<dots />

# Buzzwords<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
About buzzwords
-->

---
layout: cover
---

<dots />

# Hype<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
And hype

Don’t worry I’m not going to be talking about web 3

But while I’m talking about naming things
-->

---
layout: cover
---

<dots />

# Headless<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
Slight tangent here, I’m sure the majority of you have heard the term serverless...

Serverless because you’re not making call to specific servers, you’re making calls to APIs

You’re making call to specific APIs

These abstract away the servers from you whilst guaranteeing uptime and reliability + scalability, etc
-->

---
layout: cover
---

<dots />

# Headless = Serverless<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
So, in the terms of headless no server === serverless right?
-->

---
layout: cover
class: text-center
---

# 🤷

<!--
Anyway moving on
-->

---
layout: cover
---

<dots />

# The Present<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
Back to the present!

So, let’s talk about JavaScript and how much it has really matured over the recent years

It’s now like a runtime for the web in the browser

And we, as developers can do a lot more in the browser
-->

---

<div>
<img class='how-its-going' src='/assets/headless-cms-graphic.png' alt='headless cms graphic' />
</div>

<style>
  .how-its-going {
    position: absolute;
    left: 40px;
    top: 120px;
    width: 70%;
  }
</style>

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
layout: cover
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
  ul {
    list-style: disc !important;
    font-size: 2rem;
  }
  ::marker { 
    color: #f5487fff; 
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
layout: cover
---

<dots />

# The Future<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
Let's talk about where we're going

Briefly
-->

---
layout: cover
---

<div v-click-hide><dots /></div>

<div grid="~ cols-2 gap-2" m="-t-2" class='place-items-center'>

GraphQL<highlight>.</highlight>

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
  ul {
    list-style: disc !important;
    font-size: 2rem;
  }
  ::marker { 
    color: #f5487fff; 
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
layout: cover
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
  @import '/prism-night-owl.css';
  span {
    font-size: 1.25rem;
    line-height: 1.5;
  }
</style>

<!--
Here's a GraphQL query, and an example of how content federation will work in GraphCMS

content federation is a fancy term for bringing together data from various sources

anyway I'm here to talk about Svelte and how that fits in here
-->

---
layout: cover
---

<dots rgColor="#f5487fff" />

# Svelte<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
Ok, so let's talk about Svelte and it's position here
-->

---
layout: cover
---

<dots rgColor="#f5487fff" />

# SvelteKit<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
When I say Svelte what I'm actually referring to is SvelteKit

SvelteKit will eventually be the way all new projects are made with Svelte

Still in public beta

here's how to get started with Svelte
-->

---
layout: cover
---

```bash
npm init svelte@next new-svelte-project
```

<style>
  @import '/prism-night-owl.css';
  span {
    font-size: 2rem;
    line-height: 1.5;
  }
</style>

<!--
Once SvelteKit goes v1 this will change to
-->

---
layout: cover
---

```bash
npm init svelte new-svelte-project
```

<style>
  @import '/prism-night-owl.css';
  span {
    font-size: 2rem;
    line-height: 1.5;
  }
</style>

<!--
This

The @next will go away

This will be the way to start a new Svelte project

So, let's take a look at how we'd go about using GraphQL with a Svelte project

We can start by taking a look at a client site GraphQL library like URQL
-->

---
layout: cover
---

<dots />

# URQL<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
URQL

Or Universal React Query Library is a great GraphQL client with Svelte bindings

An URQL client can be initialised anywhere in the Svelte project

a __layout.svelte component is a good place to have the client as it will be available throughout the project

Kind of like how you would do a content provider in React but with a lot less boilerplate
-->

---
layout: cover
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
  @import '/prism-night-owl.css';
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
layout: cover
---

## `src/routes/index.svelte`

<br>

```js {all|2|3-7|8|9|all}
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

<style>
  @import '/prism-night-owl.css';
  span {
    font-size: 1.25rem;
    line-height: 1.5;
  }
</style>

<!--
You can then write your queries into the URQL operation store to create a subscription to the data
-->

---
layout: cover
---

## Svelte debug 👀

<br>

```js
<pre>{JSON.stringify($posts, null, 2)}</pre>
```

<style>
  @import '/prism-night-owl.css';
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
layout: cover
---

## URQL output

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
  @import '/prism-night-owl.css';
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
layout: cover
---

## `src/routes/index.svelte`

<br>

```js {all|1,15|2|3|4|5|6,14|7-13|all}
{#if $posts.fetching}
  <p>Loading...</p>
{:else if $posts.error}
  <p>Error! {$posts.error.message}</p>
{:else}
  <ul>
    {#each $posts.data.posts as post}
      <li>
        <a href={`/posts/${post.slug}`}>
          <Post {post} copy={false} />
        </a>
      </li>
    {/each}
  </ul>
{/if}
```

<style>
  @import '/prism-night-owl.css';
  span {
    font-size: 1.25rem;
    line-height: 1.5;
  }
  h2 {
    margin-top: -25px;
  }
</style>

<!--
Here we can use some of the Svelte expressions to work through the URQL response

URQL has the fetching state built into it so you can check before rendering
-->

---
layout: cover
---

<dots />

# Leaking Credentials<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
So that's great n' all but what about sensitive information?

I'm talking about authentication tokens, etc

Before I get into that, did I tell you that Svelte has file-based routing?

Let's take a quick look at Svelte routing
-->

---
layout: cover
---

<dots />

# SvelteKit routes<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
SvelteKit uses a file-based routing system much like NextJS

These routes can also be turned into endpoints

Let's take a quick look at a project file structure using file-based routing
-->

---
layout: cover
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
  @import '/prism-night-owl.css';
  span {
    font-size: 2rem;
    line-height: 1.5;
  }
</style>

---
layout: cover
---

<dots />

# SvelteKit endpoints<highlight>.</highlight>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
Let's take a look at how SvelteKit can be used to create endpoints
-->

---
layout: cover
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
  @import '/prism-night-owl.css';
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
layout: cover
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
  @import '/prism-night-owl.css';
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
layout: cover
---

## `src/lib/graphql-client.js`

<br>

```js {all|1|2|4|all}
import { GraphQLClient } from 'graphql-request'
const GRAPHQL_ENDPOINT = import.meta.env.VITE_GRAPHQL_API

export const client = new GraphQLClient(GRAPHQL_ENDPOINT)
```

<style>
  @import '/prism-night-owl.css';
  span {
    font-size: 1rem;
    line-height: 1.25;
  }
</style>

<!--

-->

---
layout: cover
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
  @import '/prism-night-owl.css';
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
layout: cover
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
  @import '/prism-night-owl.css';
  span {
    font-size: 1.25rem;
    line-height: 1.5;
  }
</style>

<!--
Context module means it runs before the page loads
-->

---
layout: cover
---

## `src/index.svelte`

<br>

```js {all|2|all}
<script>
  export let posts
</script>
```

<style>
  @import '/prism-night-owl.css';
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
layout: cover
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
  @import '/prism-night-owl.css';
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
layout: cover
---

# Bearer token<highlight>.</highlight>

<!--
What about the credentials?
-->

---
layout: cover
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
  @import '/prism-night-owl.css';
  span {
    font-size: 0.8rem;
    line-height: 1.25;
  }
</style>

---
layout: cover
---

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
  @import '/prism-night-owl.css';
  span {
    font-size: 0.8rem;
    line-height: 1.25;
  }
</style>

<!--
This should all be in a try catch, but I want to get all the code on the screen
-->

---
layout: cover
---

<dots />

# <highlight color="#253889ff">graphcms.com/blog</highlight>

# <highlight color="#253889ff">graphcms.com/docs</highlight>

---
layout: cover
---

<dots />

# <highlight>@</highlight>spences10 <highlight color="#253889ff"><mdi-github /> <mdi-twitter-circle /></highlight>

# scottspence<highlight>.</highlight>com <highlight color="#253889ff"><mdi-web /></highlight>

---
layout: cover
---

<dots />

# Thank you<highlight>.</highlight>
