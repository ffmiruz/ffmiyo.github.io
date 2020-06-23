---
template: post.html
title: DNS Flow
date: 2020-06-23
---
Computers are communicating using IP Address. But numbers(IP Address) is not memorable to human. 
So, domain names are used to map the IP Address which gives birth to Domain Name System(DNS).

### Figure out the address for a domain for the first time

* You enter an url in the browser. `example.com`
* The browser check for the domain in its cache. 
* The browser ask for information from OS.
* OS check for the domain from its cache.
* OS send request to the resolver.
> Resolver server is usually your ISP
* The resolver check its cache.
* The resolver makes request to root server.
* Root server gives address to the specific Top Level Domain(TLD) server. `.com TLD server`
>Root server stores address to TLD servers.
* The resolver saves the TLD server address for future use.
* TLD server gives authoritative name servers of the domain. `ns1.example.com, ns2.example.com`
>Registrar is the one who communicates authoritative to the TLD server.
* The resolver query one the name server for the IP address.
* Finally, the authoritative name server gives the IP address to the resolver. `52.31.120.213`
* The resolver stores the IP address. 
* The resolver gives the address to OS, and the OS to browser. Both stores the address in their cache.

The process happens in milliseconds. The browser can now make connection to the website using the IP address.
