---
title: "Survival guide for CVWO leads"
excerpt: "A big part of being a CVWO team lead is managing people’s expectations and balancing their needs. Just remember it is impossible to please everyone."
date: 2020-05-09 10:01:56 +01:00
categories: "bio"
permalink: "/posts/:title"
---

You are probably reading this because Prof Ben asked you to be CVWO team lead for the coming summer. This is a note written by CVWO team leads, primarily for you - potential leads. The goal is to provide some practical advice on how you can prepare for what lies ahead.

Before you go any further, let us open with a disclaimer: CVWO team lead is likely the most demanding role you will have experienced in a long time. It has a very high risk of burnout, especially in the first week and around launch period. The good news is that it's not permanent, CVWO team leads had burned out and then went on to work at FAANG and other selective places.

Here are the answers to some burning questions we imagine you might have by this point:

- Would we be CVWO team lead for a second summer? No.
- Would we recommend our juniors to take it up? Yes, if we think highly of them.
- What does it mean to be a good CVWO team lead? Depends who you ask.
- What does it take? We can't give an answer now, the function has too many unknowns: the product, the client, the Prof, the team, the lead (yes you).

Let's see what concrete steps you can take to know the unknown, and survive this summer.

### Part 1: Know your project(s)

---

Ideally for legacy projects, you are tapped to be lead because you have already spent a summer working in one of CVWO teams. Succession is of high importance to CVWO projects that are of greater scale and complexity, such as LBSA. If you did not have prior experience working on the projects you are about to take over, try to get some pass-down from the previous lead(s) for those projects.

- Get access to the source code (gitlab) and the production server(s) early.
- Inspect the code base, README, last few PRs, outstanding issues, etc., to get a hang of the state of the project.
- Understand if and how CI/CD are set up.
- Understand how production servers are configured, how database backup is done.
- Understand how essential services, such as SMTP, and monitoring, such as Exception Notification, Rollbar, Sentry, etc., are set up; and get credentials for them.
- Try to arrange for a site visit together with the previous lead, get an introduction to the client.

If you get a new project, arrange to meet with Prof Ben and/or the client before summer starts. Understand client's requirements, Prof Ben's requirements (not always the same), the technology stack, any possible migration from legacy system, etc.

There is one obstacle that sometimes stumbles CVWO projects, causing them to never launch: red tape around data protection. Since we usually work with VWOs that collect and store sensitive data required for their operations, such as medical information, it is good to clear this with the client and Prof Ben before embarking on building the product.

If you follow through with this part, you should have full understanding of the scopes of the projects. It is the essential first step to making sure you survive the first week. How these scopes translate to goals and deliverables is largely up to you.

By now you should realize that there are many stakeholders in this process: the VWO clients, Prof Ben, you, and let's not forget your team members. Sometimes projects come with other, equally if not more important and influential, stakeholders, such as CVWO sponsors, private vendors that VWOs engaged before/during the summer. Their goals and priorities do not always align with each other, let alone with yours. As a team lead you have to manage all of them, and to the best of your abilities abstract them away from the work your team do.

### Part 2: Know your people

---

You team is arguably the most critical stakeholder in the entire experience this coming summer. They are CVWO's raison d'etre.

As a lead you will be involved in the entire CVWO selection process. You will get quite a lot of, but not full, autonomy in forming your team. Even if you know exactly what kind of team you want to build, the different roles you want to fill, it is still very hard to tell from just a brief interview.

To make sure you make informed choices when it comes to people, take time to review the applicants' assignments, check through their git repos, resumes, cover letters, unofficial transcript, ask them questions during interview, get a hang of what they are like as a person, a student, a programmer, etc. 'Informed' does not mean the same thing as 'right' when it comes to picking people. This you will learn, with the power of hindsight.

There's no recipe for selection, every team is different. You have near full control over what kind of team you build, exercise it. Some leads pick people for their technical skills (as assessed through the assignment), some pick for attitude (interview), some pick using some weird spidey senses they have. This is part of the lesson every lead will learn, and there is no consensus. Your self-awareness would be very helpful here. If you know what kind of environment you thrive in, what kind of people you work well with, you would be better equipped to choose people for your own team. Beware of the tendency to pick mini-you's, you risk losing the benefit of diversity.

As early in the summer as possible, have a one-on-one conversation with each and everyone in your team to find out what they hope to get out of the summer. In a way they are your clients too, with their own requirements. Take note and keep this information in mind when you navigate through the summer, give opportunities, assign tasks, etc.

A big part of being a CVWO team lead is managing people's expectations and balancing their needs. The client's, Prof Ben's, your team's, your own (don't forget yourself). Just remember it is impossible to please everyone.

Sometimes you might have a team member who is somewhat lacking in skills or is a poor fit. This happens in real jobs. Your responsibility as a team lead is to make the best of the situation to ensure that the member learns as much as he/she can over the summer while is still able to contribute to the project. If an assigned team member starts to destroy value for your team and becomes a significant management overhead, please highlight to Prof Ben as soon as possible to seek advice.

As a lead, you can decide on your team's working arrangement for the second half of the summer. Whatever arrangement you want to experiment with, it needs to come from you having a good understanding of your team's working style, some transparent performance metrics, and adequate trust. It is generally acceptable for team members to work remotely during the second half of the summer to reduce the overheads from travelling. However, for the first few weeks, our experience has shown that it is much more effective to have the whole team work together physically notwithstanding the travelling costs.

### Part 3: The first week and the launch

---

CVWO is about learning, for every team member and for yourself. Make this known early to everyone in the team. Don't come in thinking you have to know it all, don't condition your team to come to you with every little question. The first week is the toughest usually because everyone is rather clueless, and they look to you for direction. This is why the preparation described in part 1 is going to help.

The opposite situation, where you have team members more well-versed than you in the projects you are going to lead, might cause some leads stress. This should not be a stressor at all. It is a blessing to have subject matter experts on the team. Encourage them to train others including yourself, respect their opinion. Of course this is assuming you can tell if someone knows what they are talking about. It's just intuition. Likewise, your team members can tell if you know what you're talking about. Try to build an environment conducive for learning, where it is ok for everyone, including yourself, to say "I don't know, I'll go and find out how it's done" or "I didn't know, thanks for showing me how it's done".

Keep in mind Murphy's law when planning for product launch. There are many tasks that can easily go unaccounted for, until the week before the launch. Give your team plenty of buffer before and after the launch. Even after you get past all the red tapes around data protection, you still need to account for the server setup, the DB backup arrangement, the domain name and certs, the GA tag incorporation, the SMTP credentials, the monitoring tools, the customer support, and of course the bugs that you don't see until you put in production seeds and onboard real users.

### Part 4: Things to look out for

---

Negativity: Keep a lookout for the sources of negativity, and address them early (especially if you are the source of negativity).

Burnout: The workload + the short project duration can easily induce burnout. Project management work is still work, dealing with people takes its toll, and you might just find it more draining than writing code. You might also feel unproductive if you don't write code. By trying to do everything, you risk getting nothing done, so sort out your priorities early and stick to it. You can read all the literature on the world about burnout and not see it coming, especially to yourself. Appoint a deputy early, and make sure that person can replace you at short notice.

Prof Ben: It is an intense experience working for Prof Ben, he can be very intimidating. Keep in mind he is also a reasonable person. It is up to you to manage the level and the cause of stress in your team. If it comes from above, negotiate. Sometimes stress is self-induced. Know the cause, address it.
