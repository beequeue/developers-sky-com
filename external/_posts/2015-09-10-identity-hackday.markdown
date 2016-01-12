---
layout: post
title:  "Sky Identity Hackday - the lowdown"
date:   2015-09-19 11:36:00
author: "Paul Thornton (Delivery Manager - Sky Identity)"
categories: hackday
image: /images/blogs/identity/hackteams.jpeg
excerpt: "For those who aren't aware, Sky Identity is the delivery area behind Sky's authentication services,
comprising of four Scrum Teams (Sky iD, Oogway, Rango, Europa), and a dedicated security (i3) and DevOps teams.
As such, the wealth of talent was recently put on display during at our internal hackday.  Find out what we got up to..."
---
## About the event

First off, thanks to all those who assisted with the preparation and who contributed to Identity’s hackday, it was good to see so many involved and some interesting ideas progressed. Special thanks to Rob McRitchie and Satnam Suman to help organise, and to Jon Mullen and Simon Cantlon for assisting with the judging.

![](/images/blogs/identity/hackteams.jpeg)

### Winner

The winner was **Team Skyfall** (Bulut Korkmaz and Sanjida Gafur) who produced the **“Multi-lingual Sky iD Admin Widget with Content Management (using a graph database)”** with added special effects!! It allows administrators to update the text and order of fields that the widget renders, in a friendly/innovative manner.

The front-end was built on Sky iD's current technology stack, leveraging HTML5, JavaScript, CSS3, and AngularJS. To store messages in the back-end, the [neoj4](http://neo4j.com/developer/get-started/) graph database and Java [spring-data-neo4j](http://projects.spring.io/spring-data-neo4j/) API was used.

Well done Bulut and Sanjida!

![](/images/blogs/identity/IMG_0548.jpeg)

A short demo can be viewed below.

<video width="100%" controls=""><source src="/images/blogs/identity/admin widget.mp4" type="video/mp4"> Your browser does not support the video tag.</video>

### Second Place

In second was **Team Teflon** (Adam Niklaus, Juan Vaccari, Vinit More, Dawid Sawa, Patric Hogan) with **"Hardening of Sign-in"**, they introduced an innovated way of improving the security on the sign-in journey, with minimal (if not any) impact to the customer, but with a great benefit - effectively invalidating most, if not all, existing malicious scripts.

The idea has since been passed on to the Sky iD Scrum Team to assess in more detail and to determine whether it can be roadmapped.

Given the nature of the hack, we don't want to advertise the proposal in detail, but if you are interested feel free to contact the [Sky iD i3](mailto:DL-i3@bskyb.com) security team for more information.

![](/images/blogs/identity/i3.jpeg)

### Third Place

In third was **Team Bulut** (Adarsh Ramamurthy, Jay Parmer, Yasin Efe) with **"Spring Cloud Config Admin App"**, they presented a polished application demonstrating runtime configuration management using [Spring Cloud](http://projects.spring.io/spring-cloud/).

![](/images/blogs/identity/Bulut.jpeg)

They demonstrated how [Spring Cloud Config](http://cloud.spring.io/spring-cloud-config/) can be used to build an Admin app for managing both app-specific and common config across multiple microservices.

![](/images/blogs/identity/springcloud/Config Server.png)

The hack also demonstrates that the config changes can be hot-pushed to individual microservices (or in bulk) without having to restart them. If a change needs to be persisted, one could update the central Git repository (where the config files for all the apps for all the environments will be stored) and reload the apps (not demonstrated but possible using Spring Cloud Config).

![](/images/blogs/identity/springcloud/1.png)

**Technologies used:** Spring Boot, Spring Cloud Config, Spring Cloud Bus, Rabbit MQ, Git, Docker, Docker Compose, Gradle, Groovy, Java 8

![Terminal showing multiple Docker containers logging config event broadcast related info to console.](/images/blogs/identity/springcloud/8.png) 

Again, thanks to all who took part and let’s look to take some learnings into the next one to make it bigger and better.

![](/images/blogs/identity/JoIan.jpeg) ![](/images/blogs/identity/RamAndrew.jpeg)
![](/images/blogs/identity/Charles.jpeg) ![](/images/blogs/identity/DaveIbra.jpeg)
![](/images/blogs/identity/james_ben.jpeg)
