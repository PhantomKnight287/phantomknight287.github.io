---
title: I created A Freelance Platform
description: My story about how I build a freelance platform.
pubDate: 11 Sep 2022
layout: ../../layouts/BlogPost.astro
---

I created A Freelance Platform called [LendMySkill.](https://lendmyskill.com) You can view all the source code powering this monolith [here.](https://github.com/phantomknight287/lend-my-skill)

This is my story about how I built a freelance platform.

### How It All Started?

Well, Everything started when our class teacher announced that the `Business Blaster` project is back again. If you guys don't know about it, it is an initiative by `Delhi Government` to encourage students to create their own business and create new jobs instead of consuming them. Then the teacher said that we've only 2 weeks to create a team and select an idea to present to the initial panel of judges. I was thinking not to take part in the project this time but I was forcefully dragged into this. We presented an idea of Creating a Freelance Platform and the judges approved this idea. But from now the real pain begins.

I was the lead and the only developer of this platform as none of the member of our team knew how to create a website or backend. So It took me 1 day to decide the stack and I came up with this stack:

- [Next.js](https://nextjs.org) to be used for the frontend.
- [Prisma](https://prisma.io) to be used to interact with the database.
- [Nest.js](https://nestjs.com) to be used to create the backend.

I starter working on this project right after deciding the stack, it was pretty fun creating the platform. Soon after I realised I need to implement a Payment Gateway to manage payments safely, there were many options:

- Paypal
- Stripe
- Razorpay
- Paytm
  etc...

### Deciding the Payment Gateway Provider.

I check all of these and then was confused in two `Razorpay` and `Paytm`, Both of them supports `UPI` and `Rupay Cards`, then I asked some other devs and they told me that the docs of Paytm has old code example and they no longer work. So, I decided to use Razorpay.

So now everything is sorted and the development begin at its full pace, the platform was ready in about 20 days and I was pretty happy with it but then I realised I made some serious mistakes and I tried to correct them but ended up in breaking the site, so now I am back to where I started, after all this the teacher decided that the seed money will be arriving soon so be prepared with your product. I started to create the website again from scratch and paying attention to the mistakes I made earlier, New Version of the site was ready in 15 days which is live right now.

### Making The Repo `Open Source`.

So, I bought the domain and hosted the site. I showed it to some people, one of them was [`@ujjwal-kr`](https://github.com/ujjwal-kr). He suggested me to make the site open source as it will be unique and you may get some nice contributors, I thought upon this and then finally decided to make it open source. You can use the site and even look at the source code to see how it works. :)
