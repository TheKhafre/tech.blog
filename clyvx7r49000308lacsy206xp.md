---
title: "What Happens When You Type "www.google.com" in your Browser and Click Enter?"
datePublished: Sun Jul 21 2024 18:58:05 GMT+0000 (Coordinated Universal Time)
cuid: clyvx7r49000308lacsy206xp
slug: what-happens-when-you-type-wwwgooglecom-in-your-browser-and-click-enter
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/zhZydTyNMPg/upload/93ea33e482524facc1f135c3a320f966.jpeg
tags: programming-blogs, backend, internet

---

First things first, this is a fascinating journey into the world of backend development. The working of the world wide web has been one of the most fascinating topics since ther introduction of the internet. so, if you find yourself asking several questions about how the message you sent from one of your phones in Nigeria gets delivered to the other person in seconds (in fact, split-second in cases of fast internet connection on both ends), trust me, you're not weird... lol, I had to add that part.

Okay! here is the thing, if you are a noob to backend development and just looking around to learn something new in the backend (which I suspect brought you here in the first place), then a lot of what you will be reading here today will sound cray-cray; I mean a lot of the things you will read here today will sound VERY strange, but trust I'll do my best to break down most of the new things.

So, without wasting any further keyboard buttons, let's get straight into it.

## What is a Browser?

think of your browser as a waiter in a restaurant who takes your order to the chef who will make the food you want to eat there. Okay, that might be a bit too over-simplified, so, let's talk like real devs. Your browser is something that acts in the capacity of a client in the request-response circle when you visit a webpage.

When you type a website into the address bar of a browser, you trigger the beginning of a long circle known as the request-response circle. A simple way to understand this circle is that when you try to access a website, you are ***requesting*** the files that are used to develop that website from a location known as the ***server***.

Now, that definitely opens up another rabbit hole right? lol... I thought as much, so let's talk about a server.

When a website is developed, such as our main focus today "[google.com](http://google.com)", the files that were used to develop the website are saved in a web-based storage (some people call this "cloud storage"), this location is known as a server. So, whenever anyone needs to access this website, they use their browser to make a request for the files that will make the website load on their computer. This request is made to a server which after confirming a few things then sends the files through a web protocol known as the HTTP i.e. HyperText Transfer Protocol.

However, in some cases, there is a need for some dynamically generated content like user profile updated blog content and so on, these extra files are saved in a special kind of location known as a ***Database***. Now that you understand these basics, let's move on to talk about what happens when you type "[www.google.com](http://www.google.com)" in the address bar and click on enter.

## How Does the Internet Work?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721587600417/eb88a391-bda8-4ed2-a750-93fcb7169464.jpeg align="center")

In your elementary computer science class, your teacher might have mentioned once or twice that computers can only understand 1s and 0s. So, here is the adult explanation of 1 and 0 from the website approach.

Any and every website you can think of today is mapped to a unique IP (***Internet Protocol***) address in the giant web phonebook known as a ***Domain Name System (DNS)***. immediately you type [www.google.com](http://www.google.com) and click enter, your browser sends a request DNS to get the IP address of [google.com](http://google.com). If the website exists the DNS server will respond with the IP address of the website.

Immediately the browser gets the IP address of the website, in this case, [google.com](http://google.com), it uses the IP address to look for the server where the [google.com](http://google.com) files are located and goes ahead to establish a connection with the [google.com](http://google.com) server. The process it uses to establish this connection is known as the ***Transmission Control Protocol*** (aka TCP), and the overall process of *using the IP address to locate a web server through the TCP is known as a* ***handshake***.

## How Does The Web Security Work When Accessing The Website?

Before a connection is established with the server through the handshake protocol, most web servers have something known as a firewall installed that checks all incoming and outgoing connections with the server. Amongst many of the security checks most firewall checks, two prominent checks that are common to all are to check if "you have permission to access that page you are requesting" and "if your connection is secured".

In this case, if you tried to access an admin panel of [google.com](http://google.com) without authorization or trying to access the website through a portal or channel the server feels might be insecure, your request will be denied and the handshake request will be disconnected. However, in most cases as seen on the internet today, not only the inbound connection is secured, the file transfer process is now mostly through a secure channel. Have you noticed that "s" in the website's "http" protocol? that's to tell you that the file transfer process with the said website is through a secure channel.

Once you pass the secure checks, the handshake will be initiated successfully and the file request will be completed through either the ***"Transport Layer Security (TLS)"*** or ***"Secure Socket Layer (SSL)"***.

## What is a Load Balancer?

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721587908465/6f7ff47f-38ce-4afe-a48f-7da59cf4b0e1.png align="center")

Let's look at it this way, suppose you go to a restaurant that has 100 waiters taking orders from a hundred people but there's just one chef to cook all the orders. How efficient do you think the restaurant will be? trust me, there are going to be a lot of unsatisfied customers. But, imagine there is another restaurant that has a point where everyone can make their order but 100 chefs are available to cook, that is what we call efficiency.

A load balancer is a software that distributes clients' requests across servers to prevent one server from getting overloaded. I mean think about it, imagine there are no checks in place to check how doctors attend to patients in a hospital, it won't be long before you will notice that one doctor has a long wait list where there could be another doctor without a patient.

For a website like [google.com](http://google.com) which has millions of users using the website every second, a load balancer helps it distribute the server request to prevent server overload and downtime. the response is usually the same HTML, CSS, JS, Python files, etc that form the building blocks of the website.

### Bonus: Where Does the Database come in?

A database is a kind of storage for saving important files and dynamic contents. usually, this includes admin files, user information, product files, new blog additions, and so on... you get the point, dynamic content.

When the handshake is completed and the response process has been initiated, if one of the files we've requested is not part of the static files on the server, the server then makes a request to the database which is also usually behind a firewall to prevent leaking sensitive and important files. Once the database can also verify the source to be a valid source it responds with the requested file.

At the end of all these circles and verifications, you get the requested web page: [google.com](http://google.com). The more interesting part of these processes is that they happen so fast that you don't even get to think about it or notice all these were done.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1721588112570/a9b7e091-9e39-41a4-81d2-bfd0c9ee2028.webp align="center")

okay, that's a long post, so, here is a potato to keep your mouth full. lol!