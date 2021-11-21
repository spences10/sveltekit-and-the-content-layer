---
theme: default
class: text-left
highlighter: prism
title: SvelteKit and the Content Layer
fonts:
  sans: 'Inter'
  serif: 'Inter'
  mono: 'Fira Code'
---

<div class='max-w-screen-sm'>

# SvelteKit and the Content Layer

## Scott Spence

MMT Meetup Nov 2021

</div>

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

<!--
So with a talk like this,

I’m going to need to bring up the past
-->

---
layout: cover
---

# The past<span class='text-[#F5487FFF]'>.</span>

<!--
As with any kind of talk like this, we’ll need to bring up the past to justify the present/or future
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

<!--

-->

---
layout: cover
---

# Terminology<span class='text-[#F5487FFF]'>.</span>

<!--

-->

---
layout: cover
---

# Buzzwords<span class='text-[#F5487FFF]'>.</span>

<!--

-->

---
layout: cover
---

# Hype<span class='text-[#F5487FFF]'>.</span>

<!--

-->

---
layout: cover
---

# Headless<span class='text-[#F5487FFF]'>.</span>

<!--

-->

---
layout: cover
---

# Headless = Serverless<span class='text-[#F5487FFF]'>.</span>

<!--

-->

---
layout: cover
class: text-center
---

# 🤷

<!--

-->

---
layout: cover
---

# The Present<span class='text-[#F5487FFF]'>.</span>

<!--

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
This brings us to headless...

So what is a headless CMS

Give developers a lot of flexibility to implement what why like
-->

---
layout: cover
---

# The Future<span class='text-[#F5487FFF]'>.</span>

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

---
layout: cover
---

# SvelteKit<span class='text-[#F5487FFF]'>.</span>

---
layout: cover
---

# URQL<span class='text-[#F5487FFF]'>.</span>