---
layout: post
title:      "Fetch or Axios?"
date:       2019-09-29 12:28:49 -0400
permalink:  fetch_or_axios
---


I recently attended a meeting where the discussion centered around the differences and benefits or using either the Fetch API or Axios npm for HTTP requests. (I should mention, that everyone agreed that both are absolute improvements on the Jquery ajax method.) This discussion was enlightening to me because I always thought they were basically the same thing except Axios had cleaner syntax. Well, that's not exactly true, is it?

I spent some time researching the two and here is what I came up with -

Fetch is a *global* method that fetches resources asynchronously across the network. It is a native part of JavaScript and therefore already part of the browser and as a part of JavaScript is also standard-compliant.

Since it is already available in the browser, there is no additional baggage added to an application. There are no third party dependencies or libraries to be added. This may seem negligible on a small application but depending on the project and if you aren't using Node, this may save a lot of weight. 

However, as in all things there are some issues that raise concerns.

When receiving a response from the HTTP request it is just a Promise and not the actual JSON object. The response must be handled in order to get the data needed. This includes stringifying the response and targeting specific data types in order to get the data needed.

With error handling, since fetch() returns a Promise, the response will resolve normally. The request will not be rejected even if the response is an HTTP 404 or 500. Instead, it will only reject on network failure or if anything prevented the request from completing. This can be handled by using a conditional to throw an error if the response is not ok. So, add a bit more code.

Axios is a HTTP client for the browser and node.js which is Promise based. It is a third party library which must be added to the application. Depending on the project and the amount and size of requests this may have some affect. 

However, as a benefit, the axios.get()  method has some advantages over the native fetch() method. 

Axios has transformers which allow performing transforms on data before a request is made or after a response is received. This is especially noted on responses - the JSON object is returned and there is no need to stringify the HTTP response. This allows cleaner handling of errors at the time the response is returned.

Interceptors allow you to modify  requests and/or responses  and async operations can also be performed before a request is made or before a Promise settles.

Axios also provides automatic CSRF (cross site request forgery) protection.

So, there are some differences but both have their benefits. Depending on the project choose the one that works .

For another explanation, I found this video to be very informative

https://youtu.be/Fp7uawSUuFE


