---
title: What Happens When  You Visit a Website? 
date updated: 2024-06-08 11:10 AM
---
### Summary

In this article, I will try to explain what happens behind the scenes when you visit a website.

Have you ever thought about what processes are running in the background when you access a website?

![[what-happens-when-you-visit-a-website.png]]

### Introduction

First, when you click on a site or search for a site through your address bar—if you search through your address bar, this query is sent to your search engine (e.g., Google, DuckDuckGo, Yandex)—your browser connects to a server called DNS.

So, what is DNS?

Simply put, every website on the internet has a unique IP address.
DNS converts these IP addresses into more user-friendly addresses, such as _[www.example.com](http://www.example.com)_, to make them easier for users to remember.

When DNS finds the IP address corresponding to the desired URL, it sends this IP address to your browser, allowing it to communicate with the server hosting the website.

### Communication with the Server

Once the browser has the desired IP address, it uses a protocol called TCP (Transmission Control Protocol) to send a request called a GET request (because we want to **GET** the web content).
Why do we use TCP instead of UDP (another communication protocol)? Although TCP is slower than UDP, TCP performs extra checks that UDP does not, resending any missing packets. This ensures that no data is lost along the way.

After connecting to the server, a process called SSL Handshake occurs. In short, SSL Handshake provides the server's security certificate, informing the browser that all traffic is encrypted and that the site you are visiting is secure. You can recognize this if the URL starts with _**https**_ or if there is a lock icon next to the address bar. Thanks to the SSL Handshake, you are assured that your traffic is protected from anyone trying to spy on it.

Afterward, the server reviews your request using a firewall. This ensures the server’s security, prevents the request from passing through an incorrect connection, and blocks harmful requests sent to the server.

If you pass the firewall without any issues, your request is finally directed to the actual web server. The web server retrieves the data based on your GET request and sends it back to your browser.

That’s it—this is what happens behind the scenes when you click on a website.
""
Just think about it: so many complex operations happen so quickly that you don't even notice them. This is precisely what motivates me to think, ponder, and research these topics. Thank you for taking the time to read.

### References

Medium article by Carter C: ["What happens when you visit a web page"](https://cclements3150.medium.com/what-happens-when-you-visit-a-web-page-e407a38db95f)

Wikipedia article on DNS: [Domain Name System](https://en.wikipedia.org/wiki/Domain_Name_System)

Replit's YouTube video: ["What Happens When You Visit a Web Page?"](https://www.youtube.com/watch?v=SbqjHmqozIk)
