---
title: How to use Razorpay in Next.js?
description: How to properly use Razorpay in Next.js
pubDate: 14 Sep 2022
layout: ../../layouts/BlogPost.astro
---

While working on the freelance platform, I started to implement Razorpay's sdk to accept payments. I searched on google to find some official sdk for React but couldn't find any. I read some blog posts where they showed the older methods using `document.createElement`, I implemented it but it was kinda slow because it takes some time for the sdk to load. Then I came up with my own solution, I am using [`Mantine`](https://mantine.dev) so when user pressed the order button I open a modal showing the amount of the order and a checkbox saying `I accept to Payment Terms`.After the checkbox is checked, the disabled button(which no longer is disabled) can now be used to initiate a transaction. The Modal has a Nextjs's Script tag with `strategy="lazyOnLoad"`, it loads the Razorpay's script and the script binds itself to the `window` object. The time taken by the user to read the details and mark the checkbox is enough for the script to load. As soon as the modal is opened, I create a websocket connection with the backend, when the user click on the order button, the frontend emits an event asking the backend to generate `order_id` which is then supplied to the Razorpay's sdk to complete the transaction.

The Script is Loaded Like this:

```typescript :client/components/Modals/Payment.tsx
import Script from "next/script";
// snip

<Script
  strategy="lazyOnload"
  src="https://checkout.razorpay.com/v1/checkout.js"
/>;
```

You can then check if this script is loaded by doing `window.Razorpay` if it is undefined then this script isn't yet loaded, you can either tell the user to wait for the script to load or use `document.createElement` to create a script tag and load the script.
