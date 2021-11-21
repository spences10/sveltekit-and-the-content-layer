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

<div class='max-w-screen-sm'>

# SvelteKit and the Content Layer

## <span class='text-[#F5487FFF]'>Scott Spence</span>

MMT Meetup - <span class='text-[#F5487FFF]'>Nov 2021</span>

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

GraphCMS is a headless API content management system

We really pride ourselves on delivering structured content at scale

We’re one of the first, if not the first headless GraphQL based CMS’

Completely GraphQL native to this day, we’re all in on GraphQL and that’s all we provide

This will be a brief history of content on the web, where we are now and where we’re going
-->

---
layout: cover
---

# Histroy Lesson<span class='text-[#F5487FFF]'>.</span>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
So with a talk like this,

I’m going to need to bring up the past

So time for a bit of history
-->

---
layout: cover
---

# The past<span class='text-[#F5487FFF]'>.</span>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
Let's take a look at how things used to be
-->

---

<div>
<img class='how-it-started' src='/assets/how-it-started-graphic.png' alt='filezilla logo' />
</div>

<style>
  div {
    display: flex;
    justify-content: center;
  }
  .how-it-started {
    position: absolute;
    left: 50px;
    top: 110px;
    width: 60%;
  }
</style>

<!--
How it started.

Using FTP to upload files to live instances.

There then became a requirement for authoring content without the need for a developer.
-->
---

<div>
<img class='filezilla' src='/assets/filezilla.png' alt='filezilla logo' />
<img class='old-website' src='/assets/old-website.png' alt='filezilla logo' />
</div>

<style>
  div {
    display: flex;
    justify-content: center;
  }
  .filezilla {
    position: absolute;
    left: 220px;
    top: 100px;
    width: 35%;
    z-index: 1;
  }
  .old-website {
    position: absolute;
    left: 450px;
    top: 150px;
    width: 35%;
    z-index: -1;
  }
</style>

<!--
How it started.

Using FTP to upload files to live instances.

There then became a requirement for authoring content without the need for a developer.
-->

---
layout: cover
---

<div grid="~ cols-2 gap-2" m="-t-2" class='place-items-center'>

Traditional CMS<span class='text-[#F5487FFF]'>.</span>

- Website based
- “Theme” based
- Server rendered
- Tightly coupled
- You pay for everything
- Often slow


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
    color: #F5487FFF; 
  }
</style>


<!-- 
So let’s take a quick look at what a CMS was back in the day

Primarily website based, there wasn’t the need to have any content piped to a mobile device

These sites were heavily theme based, you could make your own and alter them to your liking

You’d pay for everything, you were hosting this yourself, there wasn’t really CDNs back then and server space was expensive

A lot of the things which made it slow were those round trips to the page from the database
-->

---
layout: cover
---

# The present<span class='text-[#F5487FFF]'>.</span>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
Ok, so let’s talk about the present and where we are now
-->

---
layout: cover
---

# Terminology<span class='text-[#F5487FFF]'>.</span>

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

# Buzzwords<span class='text-[#F5487FFF]'>.</span>

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

# Hype<span class='text-[#F5487FFF]'>.</span>

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

# Headless<span class='text-[#F5487FFF]'>.</span>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
Slight tangent here, I’m sure the majority of you have heard the term serverless...

Serverless because you’re not making call to specific servers, you’re making calls to APIs 

You’re making call to specific APIs that abstracts away the servers from you whisht guaranteeing uptime and reliability + scalability, etc
-->

---
layout: cover
---

# Headless = Serverless<span class='text-[#F5487FFF]'>.</span>

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

# The Present<span class='text-[#F5487FFF]'>.</span>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
So, let’s talk about JavaScript and how much it has really matured over the years

It’s now like a runtime for the web in the browser

And we, as developers can do a lot more in the browser
-->

---
layout: cover
---

<div grid="~ cols-2 gap-2" m="-t-2" class='place-items-center'>

Headless CMS<span class='text-[#F5487FFF]'>.</span>

- Frontend agnostic
- Mostly CRUD
- Decoupled
- Developer flexibility
- CI/CD with Git

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
    color: #F5487FFF; 
  }
</style>

<!--
So, headless...

So what is a headless CMS

Give developers a lot of flexibility to implement what why like
-->

---
layout: cover
---

# The Future<span class='text-[#F5487FFF]'>.</span>

<style>
  h1 {
    font-weight: bold;
  }
</style>

---
layout: cover
---

<div grid="~ cols-2 gap-2" m="-t-2" class='place-items-center'>

GraphQL<span class='text-[#F5487FFF]'>.</span>

- Simple to understand 
- You get what you see
- Client or Server Side

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
    color: #F5487FFF; 
  }
</style>


<!-- 

-->

---
layout: cover
---

```graphql
query {
  products {
    name
    description {
      richtext # from GraphCMS
    }
    inventory {
      inStock # from 3rd party API
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

---
layout: cover
---

# Svelte<span class='text-[#F5487FFF]'>.</span>

<style>
  h1 {
    font-weight: bold;
  }
</style>

---
layout: cover
---

# SvelteKit<span class='text-[#F5487FFF]'>.</span>

<style>
  h1 {
    font-weight: bold;
  }
</style>

---
layout: cover
---

# URQL<span class='text-[#F5487FFF]'>.</span>

<style>
  h1 {
    font-weight: bold;
  }
</style>

<!--
URQL can be initialised in a __layout.svelte component then be available throughout the project
-->

---
layout: cover
---

## `__layout.svelte`

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
URQL can be initialised in a __layout.svelte component then be available throughout the project
-->

---
layout: cover
---

## `index.svelte`

<br>

```js {all|2|3-7|8|9|all}
<script>
  import { gql, operationStore, query } from '@urql/svelte'
  const postsQuery = gql`
    query Posts {
      # posts query
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
You can then write your queries in to the URQL operation store to create a subscription to the data
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
After the script tag in the body of the page

I can add this to see what the data looks like from URQL
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
This is where this fetching property comes in handy
-->

---
layout: cover
---

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
</style>

<!--
URQL has the fetching state built into it so you can check before rendering
-->

---
layout: cover
---

# Leaking Credentials<span class='text-[#F5487FFF]'>.</span>

<style>
  h1 {
    font-weight: bold;
  }
</style>

---
layout: cover
---

# SvelteKit routes<span class='text-[#F5487FFF]'>.</span>

<style>
  h1 {
    font-weight: bold;
  }
</style>
