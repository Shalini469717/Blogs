---
title: "How does the Internet work?"
seoTitle: "How does the Internet Work?"
seoDescription: "Internet is an integral part of our daily lives, but have you ever wondered how it works?"
datePublished: Sat Apr 01 2023 09:34:56 GMT+0000 (Coordinated Universal Time)
cuid: clfxs276m000y09me69q8eau9
slug: how-does-the-internet-work
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1681237375473/4e4eed1e-2f55-46ef-8c13-edbe26801fa5.webp
ogImage: https://cdn.hashnode.com/res/hashnode/image/upload/v1680341648957/f9c21840-adc3-4979-b63e-37e327cd3716.jpeg
tags: programming, web-development, computer-science, hashnode, wemakedevs

---

## Introduction

The internet has become an integral part of our daily lives, whether we're using it to check email, stream videos, or browse social media. But have you ever wondered how it all works? In this post, we're going to take a closer look at the basics of how the Internet works.

To understand how the internet works, let us first understand the basic unit which is the computer network. A computer network is a group of computers connected together. The Internet is the collection of these computer networks.

## How did it start?

During the space and arms race between Russia and America, America made an agency to research high-level projects which is called ARPA - Advance Research Projects Agency. Since the buildings were far away from each other and they needed a way to communicate with members of other branched and send files to each other, they developed something called ARPA net.

More and more computers were added later and they talked using protocols. But there was one thing that was missing, i.e. getting redirected to the other documents when the links on a research paper were clicked. www enters the scenario and it was a project meant to store these research projects. With this, they could open other documents using the links. But the search option which we see now was still not available.

## Protocols

In networking, a protocol is a set of rules for formatting and processing data. Network protocols are like a common language for computers. The computers within a network may use vastly different software and hardware; however, the use of protocols enables them to communicate with each other regardless.

TCP/IP stands for Transmission Control Protocol/Internet Protocol and is a suite of communication protocols used to interconnect network devices on the Internet.

When we are using the internet, we try to send different types of files like videos, images and secure files. In the case of secure files, we must ensure atomicity. For example, when you try to send an email, then there must be a set of rules which must be followed so that the email is reached safely. The Internet Society comes up with these rules.

If you were watching a video, then you might be ok with watching it with decreasing quality as long as it doesn't start buffering. In these cases where you wouldn't mind if 100% of the content reaches you, UDP - User Datagram Protocol is used.

## IP Address

The data sent between devices on the internet is broken down into small chunks called packets. These packets are sent individually and reassembled at the destination device, which ensures that the data is transmitted reliably and efficiently. To ensure that the data is protected from interference or interception, it is also encrypted using a variety of protocols such as SSL or TLS.

An IP address is a unique address that identifies a device on the internet or a local network.

If you were to enter www.google.com into your search bar, then a webpage is rendered from a server. How does it find the server to which it has to connect? Servers are also identified with IP addresses. Every single device has an IP address associated with it.

It is denoted in the format of **x.x.x.x** where each x is in the range of 0-255.

Curious about the IP address of your device? Try using the following command in cmd

`curl` [`ifconfig.me/ip`](http://ifconfig.me/ip)

It gives the IP address of your ISP. Now you know which server you are accessing from. You might be having a router at your home, it assigns local IP addresses to the devices connected with it. But if a particular application requests the data, then the data sent as a response must also be sent to that application only.

How does it know which application is making the request?

## Port Numbers

This is known using port numbers - PN. If it is a 16-bit, then 16-bit PN can be used, which means a total of 2 ^ 16 = 65536 port numbers are possible.

The port numbers from 0-1023 are reserved port numbers. Ex: HTTP has a port number of 80. These can't be used by us. The port numbers from 1024 - 49152 are registered for applications like SQL, MongoDB etc. The remaining we can use.

## Speed

What does 1mbps stand for? It means 1 megabit per second.

1gbps - 1 gigabit per second

1kbps - 1 kilobit per second

When you send the data, from your computer to another computer, it is called upload. If you are receiving it, then it is called a download.

You can check your upload and download speed using free sites on the internet.

## How are computers connected?

Check out the below link to know how submarine cables are laid across the world. These are laid on the ocean floor and are sturdy enough.

[Submarine Cable Map](https://www.submarinecablemap.com/)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1680340121686/c3a239cf-7c75-4951-9954-f87b518d218d.webp align="center")

## Conclusion

Ultimately, the Internet is a complex system that relies on many different components and protocols working together seamlessly to ensure that data is transmitted quickly, reliably, and securely. It's amazing to think that all of this happens in just a matter of milliseconds, and it's a testament to the engineering marvel that is the internet.

*Hope you enjoyed reading the blog. I'd love to hear from you: Did I leave anything out? Any suggestions to improve? What other topics should I write a blog on? Comment below and let me know.*

Reference:

[Computer Networking Full Course - OSI Model Deep Dive with Real Life Examples - YouTube](https://www.youtube.com/watch?v=IPvYjXCsTg8&list=PL9gnSGHSqcnoqBXdMwUTRod4Gi3eac2Ak&index=4&ab_channel=KunalKushwaha)