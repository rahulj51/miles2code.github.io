---
layout: post
title:  "Data Team Roadmap"
date:   2020-10-15 10:18:00
categories: Data Planning Roadmap
cover: https://images.unsplash.com/photo-1581922819941-6ab31ab79afc
---

This is a post about my experience creating a 2021 roadmap for my team at Omio. I say data team in the title but perhaps it's more apt for a data engineering team such as the one I am leading. It's that time of the year again when some of us start building a mental map of what's next. My shower time was consumed by exactly these kind of thoughts for the last few weeks so I decided to put all of it on paper.

## Mindmap

To chart out my thoughts, I decided to use a Mindmap for its well documented benefits. It's a great framework to represent structured thought and good mindmap tools allow easily expanding/collapsing the nodes which makes it helpful to navigate a big map. 

Our actual mindmap had more concrete information specific to my context at Omio but here's a more abstract version of the same.

![/assets/data_team_roadmap/Data-Team-Roadmap.png](/assets/data_team_roadmap/Data-Team-Roadmap.png)

Here's the collapsed version only showing the key themes

![/assets/data_team_roadmap/Data-Roadmap-Collapsed.png](/assets/data_team_roadmap/Data-Roadmap-Collapsed.png)

A few meta-points to note:

- This is a more action-based representation of the roadmap. You can also choose to model it by capabilities. It depends on how you mentally picture your world 🙂
- It helps to add specific technologies and tools at the very end of the branches to avoid tool affinity. Think first of the problems you want to solve or capabilities you wish to build.
- Keep the roadmap at a slightly higher level of abstraction. Avoid over-mapping all the way to Jira tickets 🙂
- Stay away from adding tactical tasks blindly. First check where they fit in your roadmap.
- Also avoid feeling too constrained by your limitations (ex. team-size etc.) . Be realistic but also be ambitious.
- Your team must be an important feature of any roadmap. Unfortunately, it is often forgotten. Adding the team explicitly to the map helps to not lose sight of their growth.
- Hierarchically structuring information is good but sometimes the most important information can get buried deep under multiple levels of hierarchy. If there is something very important to you in the roadmap, feel free to elevate it to a higher level in the representation just so you can keep the right level of focus on it. For ex., you may want to pull-up a really big project / initiative to a higher level for this purpose.
- You may not like duplicates in your data but it is perfectly fine to have duplicate information in your mindmap (*ex. the same branch / node can exist in two different places simply because it is relevant in both*). Some mindmap tools allow you to connect related information together but I found that a little noisy and distracting in the tool I was using ([MindNode](https://mindnode.com/)).
- Above all, remember that [The Map is Not The Territory](https://fs.blog/2015/11/map-and-territory/).

## Key Themes

Now, let's take a sneak peak into each of the core themes in our roadmap. 

### Raw Data Tracking

![/assets/data_team_roadmap/Screen_Shot_2020-10-10_at_9.15.24_AM.png](/assets/data_team_roadmap/Screen_Shot_2020-10-10_at_9.15.24_AM.png)

Raw Data Tracking is obviously the source of all data into our Analytics stores (lake/warehouse). We decided to split it by sources because our tracking infrastructure at Omio is clearly split along those lines. Then for each of these, we decided to split them further into 

- Coverage - Is there a need to add more sources or upgrade existing
- Tooling - Do we need to evolve existing toolset or Introduce new tools
- Quality of raw data -  What do we want to improve here? How?

Needless to say, each of these can be further branched out to add more specific details. 

### Data Products

![/assets/data_team_roadmap/Screen_Shot_2020-10-10_at_9.14.40_AM.png](/assets/data_team_roadmap/Screen_Shot_2020-10-10_at_9.14.40_AM.png)

In 2021, my team and I want to re-imagine our data-pipelines as end-to-end data products oriented towards specific business themes (ex. Funnel Analytics could be a product, Unit-Economics could be another, Marketing-spend could be yet another). This will allow us to think more holistically about what value we offer to the users of our data beyond just the data itself. 

Therefore, The Data Products branch is mainly a list of all key products that we wish to support. For each product, we then sub-branched it into 

- Features - What does the product do? What features does it support?
- User Experience - How do users interact with the product? What interfaces do we offer ?
- System Capabilities/Architecture - Data Pipelines and Flow, Data Models, Configurability etc.

Outside of these core products, we still have a lot of custom data-pipelines/ETLs. These, we decided to club under `Bespoke Data Pipelines` to separate them from our core products. Some of these pipelines could eventually evolve to become end-to-end products. 

### Infrastructure

![/assets/data_team_roadmap/Screen_Shot_2020-10-10_at_9.15.59_AM.png](/assets/data_team_roadmap/Screen_Shot_2020-10-10_at_9.15.59_AM.png)

Here, we split the roadmap a little differently - by groups of activities that we find ourselves occupied with. Notice that some of these will overlap with tooling/architecture branches in other themes but that's ok. 

Cost Management, DevOps and Security are also key capabilities that constantly evolve and therefore added here so they get the right level of attention in our planning. 

We felt that this was a better way of splitting the Infrastructure roadmap instead of platforms and tools and systems since it made it easier to understand what exactly the team should focus on.

### Data Governance

![/assets/data_team_roadmap/Screen_Shot_2020-10-10_at_9.16.38_AM.png](/assets/data_team_roadmap/Screen_Shot_2020-10-10_at_9.16.38_AM.png)

This is a bit of a catch-all for all things data. Personally, the term `Governance` has always confused me and perhaps a better word would be `Data Management`. 

For our team at Omio, we decided to split this theme into

- Data Definitions - An area that we wish to explore more and see if `metadata` can help us more consistently define our domain entities beyond how they are stored.
- Discovery - As our data landscape grows, we will soon find ourselves in a situation where consumers of data will find it difficult to get to the data they need. Adding this to our roadmap to start brainstorming on how do we go about solving this problem when it becomes a reality.
- Data Quality Management - Everything we wish to do about data quality management. In fact, in our actual roadmap, we elevated this as a central theme because we want to really focus on improving the quality of data in 2021.
- Data Protection, GDPR
- Data-Ops and Self-servability of data

### People / Team

![/assets/data_team_roadmap/Screen_Shot_2020-10-10_at_9.17.13_AM.png](/assets/data_team_roadmap/Screen_Shot_2020-10-10_at_9.17.13_AM.png)

We decided to split this into 

- Growth - How do we grow our team and Individuals? How do we create the right opportunities for ourselves?
- Skills - What skills do we want to focus on next?
- Visibility / Exposure within the organization and outside

Depending on your team's goals, you may have fewer or more branches here.

## What's Next

Once you build a roadmap like this,

- Mark the themes/sub-themes and activities as `NOW` , `NEXT` or `LATER` as a high level time horizon. But avoid putting dates till you are absolutely sure. This is a roadmap, not a project plan.
- Add other relevant meta-information like key-stakeholders, priority and success-criteria.
- Review the map each month/quarter with the team to see how you are doing. Did you change course? Why? Does it need to be updated ? What areas are getting neglected?
- Use it as a tool for conversation with your teams and stakeholders.
- Observe how and how-not the roadmap maps to your team structures. Do the central nodes represent your teams? Is it good? Bad?

## Closing Thoughts

This turned out to be a very helpful exercise for our team. An interesting observation from the team was that the roadmap helped them get a sense of the myriad of things we do as a team - an aspect that is not always evident in the day-to-day grind.

Needless to say, this roadmap is very specific to our context / environment and when you set out to build one for yourself, make sure that it reflects your own world more closely.

I'd be happy to hear what you think of this exercise for your data teams. Did you find anything conspicuous by its absence in the above roadmap?

***

*Edit - Dec 28, 2020*

#### Template files

I used [MindNode](https://mindnode.com/) for this mindmap. 

If you are looking for raw files, here are the markdown and freemind versions:

* [Markdown format](/assets/data_team_roadmap/roadmap.md) . Many mindmap tools support this. You can also use [markmap](https://markmap.js.org/) or [diagram.codes](https://www.diagram.codes/)

* [Freemind format](/assets/data_team_roadmap/roadmap.mm)




