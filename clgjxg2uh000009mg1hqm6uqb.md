---
title: "What Happens When we type google.com and hit enter?"
datePublished: Mon Jan 01 2024 23:00:00 GMT+0000 (Coordinated Universal Time)
cuid: clgjxg2uh000009mg1hqm6uqb
slug: what-happens-when-we-type-googlecom-and-hit-enter
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/cYyqhdbJ9TI/upload/d30e7bd2a43c081f03e151013139f32f.jpeg

---

## **Introduction**

**When you type a URL into your browser and hit enter, a complex interaction of frontend and backend web technologies takes place. To gain a fuller appreciation of just how intricate this process is, it’s essential to understand the DNS request, which translates a domain name (like google.com) into an IP address (like 216.58.194.174).**

Then there’s the TCP (Transmission Control Protocol) connection; a protocol designed to guarantee reliable, orderly and error-free delivery of data. However, this connection can be blocked by a firewall, set up to protect networks against unauthorized access, viruses and malicious programs.

The browser will then send an HTTP (Hypertext Transfer Protocol) request to the server. The server forwards this request to the appropriate web server application which, in turn, retrieves the webpage content from the database or file system and any associated resources, like images and style sheets. If the connection is an HTTPS (Hypertext Transfer Protocol Secure) link, then data is encrypted using either SSL (Secure Sockets Layer) or TLS (Transport Layer Security) encryption.

Sometimes the request may need to be directed through a load-balancer which distributes network traffic across multiple servers to improve performance and scalability. Upon processing, the server sends an HTTP response with webpage content, headers and necessary metadata back to the browser. Then the HTML (Hypertext Markup Language) document is parsed by the browser to build a Document Object Model (DOM) of the webpage – a hierarchical structure illustrating the webpage’s content and structure.

Finally, the browser uses the DOM to render the webpage and execute any JavaScript included on the page. It’s clear to see that the journey from URL to rendered webpage is complex and involves an array of technologies. The Domain Name System (DNS), Transmission Control Protocol (TCP), Hypertext Transfer Protocol (HTTP), Hypertext Transfer Protocol Secure (HTTPS), Secure Sockets Layer (SSL) and Transport Layer Security (TLS) all play an important part in the functioning of the internet. Even firewalls, used for security, and load-balancers, used for performance, can impact the process. Therefore, comprehending these components is fundamental for anyone wanting to understand the web.

PS: This is a simpler explanation to give you a firsthand understand of the whole process. A more technical explanation will be published later for advanced learning.