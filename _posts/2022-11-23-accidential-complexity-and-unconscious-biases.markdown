---
layout: post
title:  "Accidental complexity and our unconscious biases"
date:   2022-11-23 10:30:00
categories: data engineering career
cover: https://source.unsplash.com/ICdZeEGz-0I/1920x1440
---

<br>
*<b>Note: This post was first published on [LinkedIn](https://www.linkedin.com/pulse/accidental-complexity-our-unconscious-biases-rahul-jain/) .</b>*

In the wake of the Twitter saga, there's a been a lot of talk about accidental complexity in architecture. There is some truth in it. In large parts, this frenzy for complexity was fuelled by the bull run in Tech in the last 10 years and our obsession with "scale". Perhaps it's our industry's best kept secret but the truth is that there were strong incentives for Tech teams to build architectures that were often way too complicated.

The seminal paper on software complexity - [No Silver Bullet - Essence and Accidents of Software Engineering](http://www.cs.unc.edu/techreports/86-020.pdf) distinguishes between Essential vs Accidental complexity, the former a product of the inherent problem that the software is trying to solve; and the latter which is induced because of choices we make in the solutions.

<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/lHTsv06Yle0" frameborder="0" allowfullscreen="true"> </iframe>
</figure>

Even for the well meaning engineers, accidental complexity can often creep into software due to unconscious cognitive biases at play. This has been studied for long and here's two papers discussing this in more academic language - [Cognitive biases as project & program complexity enhancers](https://www.pmi.org/learning/library/cognitive-biases-complexity-enhancers-projects-1454) and [Cognitive Biases in Software Engineering: A Systematic Mapping Study](https://www.pmi.org/learning/library/cognitive-biases-complexity-enhancers-projects-1454)

In this article, I share my own version of the biases I have most often observed. I don't offer a remedy for these but perhaps just a reflection on how these biases impact our decision making.

**Vanity bias:** This bias is caused because showing off your skills is perversely incentivized in some tech communities and orgs. In a world of low attention span, it becomes a proxy for true knowledge, skills and relevance. This causes an inclination to build complex architectures that create an asymmetry of knowledge and make one look smarter than our peers and stand out in a crowd.

**Fomo (Fear of missing out) bias:** Caused by the fear that one is missing out on the latest trends in technology; or that one will become obsolete. This creates an unconscious bias towards selecting trendy architectures/technologies just to remain relevant. Also known as resume-driven-development.

**Not-invented-here bias:** This one's caused by a fear or distrust of anything that's not built in-house. This bias encourages reinventing the wheel because one believes that the existing solutions won't scale, aren't secure or won't meet their specific needs and they must build everything from scratch.

**Not-invented-there bias:** Caused when one puts blind trust in an architecture/solution/process just because someone well-known and respected (for ex. a large company or a thought-leader) vouches for it.
Loss-aversion bias: Related to Not-Invented-There, this bias stems from a fear of taking any kind of risks and sticking to the tried and tested. Engineers with this bias try to maintain status-quo and refuse to question their deeply held beliefs about system design or architecture.

**10x-engineer-from-Google bias:** No offence to Google but often a team hires someone from a high-profile, top-tier company and the rest of the team is rather afraid to challenge their authority, leading to an architecture that's not reviewed/vetted by the team.

**Boredom bias:** Tech work can very often be drab, boring and mundane. To overcome the boredom of the same-old-same-old, one is sometimes inclined to pick the latest, shiniest new toy - a cool new language/framework or a more complicated architecture.

**Wishful-thinking bias:** This bias is driven by an over-estimation or optimism of how the system would potentially grow and the need to accommodate all the possible features in the design and architecture.

**Simplicity bias:** Similar to Not-invented-here, this is a bias towards building something because the MVP is relatively easier (or more convenient) to build. Although well intentioned, this bias causes teams to underestimate the inherent complexity. This leads to complicated structures over time. Also known as "Hold my beer.." effect.

There are, of course, plenty of other cognitive biases that affect our decision making. After all, human beings are [irrational decision makers](https://en.wikipedia.org/wiki/Predictably_Irrational). In my experience, the best way to mitigate these biases is to start by acknowledging them and creating a feedback loop both within and outside the team to catch these biases from creeping in.
***

