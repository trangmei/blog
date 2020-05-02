---
title: "Coursemology"
excerpt: "Coursemology is a project with a long history of human suffering, one I am very proud to survive."
date: 2020-05-01 15:01:56 +01:00
categories: "projects"
permalink: "/posts/:title"

gallery:
  - url: /assets/files/build_0.jpg
    image_path: /assets/files/build_0.jpg
    alt: "placeholder image 1"
  - url: /assets/files/build_2.jpg
    image_path: /assets/files/build_2.jpg
    alt: "placeholder image 3"
  - url: /assets/files/build_1.jpg
    image_path: /assets/files/build_1.jpg
    alt: "placeholder image 2"
  - url: /assets/files/build_3.jpg
    image_path: /assets/files/build_3.jpg
    alt: "placeholder image 4"
---

After 2018 summer with CVWO, I was employed by NUS to maintain the e-learning platform Coursemology, used by quite a number of courses from NUS and other educational institutions in Singapore, including my old highschool NUS High.

I learned bits and pieces of the project's history through conversations with Prof Ben and engineers who previously worked on it. Apparently it had been rewritten once, both versions in Rails.

The project's reputation preceeded it because it is a common choice for SWE Final Year Project (FYP) for NUS Computer Science students. I heard about it long before I even considered switching into SWE, first-hand and second-hand stories about seniors who finished or gave up on their Coursemology FYP.

Young and naive as I was when I got the job, I was more excited than apprehensive about taking on Coursemology.

To me, it was a great compliment that anyone at all thought I could be trained to eventually manage Coursemology. The people who worked on it before me are all seniors I have long heard about, people who went on to join reputable tech companies.

I started out with a lot of help. Coursemology, its source code and its infra, was still managed by engineers at Ministry of Education's Experimental Systems and Technology Lab (ESTL), while I underwent my training in CS3216.

I had more than half a year working with them on Coursemology before really taking over the project. This is the period that I learned the first thing about frontend (mostly from CS3216) and ops(mostly from Coursemology).

I'm really grateful for the patience these engineers showed while guiding me though the technologies and the system. I don't know how they managed to train someone who knew so little to take on that project.

Through my time working on Coursemology there were a few periods of great learning opportunities.

### Building a server

---

First it was when we have to move Coursemology staging out of ESTL servers, because Prof Ben was leaving ESTL. I was given the chance (and budget) to build a tower server to host Coursemology staging, and to experiment with dockerized deployment.

{% include gallery caption="Building a staging server" layout="half" %}

<figure>
  <img src="{{ site.url }}{{ site.baseurl }}/assets/files/chandler_laptop.jpg" alt="">
</figure>

Getting to roll up my sleeves and build a server was definitely one of the coolest perks of the job.

Setting up the new Coursemology staging server was also the first time I worked with load-balancer, reverse-proxy, SSL certificates, server firewalls, container networking, file share systems, etc.

I really can't list all the cool new things I learned while working on this. It was truly a humbling experience to realize how much I still didn't know about the world of SWE.

### Fixing performance problems

---

The period when we moved Coursemology to dokerized deployment coincide with deployment of another major backend refactoring. During one of the exams with 300 concurrent logins, Cousermology experienced significant slowdown.

The cause was found to be newly introduced N+1 causing some pages to take significantly longer to load.

Eliminating N+1 in Rails-generated frontend is not an easy task. Where N+1 could not be eliminated or alleviated, UI changes were made to limit the amount of information shown, hence limiting the number of queries made to the database.

For example, the feed shown on user's home page when s/he first logged in used to show all pending assignments, announcements, and recent activities from other users. Rendering information such as due dates required separete queries to be sent to the database. In the end the home page was changed to only show a fixed number of pending assignments and announcements.

Dealing with this problem provided me with an opportunity to do a deep dive into the quirks of Rails and its ORM.

---

Coursemology is a project with a long history of human suffering, one I am very proud to survive. Out of the suffering, a sense of belonging is born among its survivors. Even though our tenure scatter along the 5 years of the project, even though there's never been a time when all of sit together in the same office working on Coursemology, we know each other through git blame, through FYP reports, and through home directories. I have nothing but respect and appreciation for all those that came before me and those that's brave enough to take on our legacy.

<figure>
  <img src="{{ site.url }}{{ site.baseurl }}/assets/files/coursemology_support.jpg" alt="">
  <figcaption>Support group for Coursemology survivors</figcaption>
</figure>
