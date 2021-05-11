---
layout: post
title:  "16 fundamental principles for transforming data in a warehouse"
date:   2021-05-11 20:30:00
categories: Data datawarehouse 
---

The current discourse on data can get a little tiring because of its [over focus on tooling](https://twitter.com/rahulj51/status/1254447785170042882). It feels like a new SaaS gets launched every week in the data space.

Here's a short infographic I recently wrote to distill some fundamental principles for organizing and transforming data in a warehouse. These are principles that my team and I learned the hard way in the course of building our data warehouse at Omio over last three years.

You will notice that this chart does not indulge in the debate about data lake vs warehouse or marts, suggests technologies or obsesses over Kimball vs Inmon vs Linstedt. Instead, it offers suggestions that are orthogonal to these choices and more fundamental in nature. 

As you will notice, this is a highly opinionated set of guidelines. The reader is advised to not treat these dogmatically, nor get triggered by some seemingly extreme views. Most of these principles are very contextual. YMMV. :-)

![/assets/data-modeling/data-model-arch.png](/assets/data-modeling/data-model-arch.png)   

#### General Principles for data transformations (*in no specific order*)

1. Practice immutability. Each row should only be written once to a table. In other words, do not insert a row and then update it in a subsequent step. 
1. As much as possible, break a complex transformation into various sub-steps. Adopt single responsibility.
1. Join datasets from different data sources as late as possible. Decoupling helps manage changes better.
1. Facts/Events should always have a business timestamp and an arrival timestamp.
1. Perform upserts by primary keys only. Never delete-insert based on timestamps alone.
1. Avoid upserts if you care about [bitemporal](https://martinfowler.com/articles/bitemporal-history.html) history. 
1. Cleaning data is an anti-pattern. Avoid cleaning data. If you must, do this in a separate step in the transformation flow.
1. Do not model anything motivated purely by ease-of-use or convenience. Each transformation step must be "valuable".
1. Avoid querying source tables that are more than 2 layers below the target layer.
1. Never re-implement any business logic from source systems. 
1. Use unmaterialized views where possible for Aggregations (Views in Snowflake and BQ are cheap to build and change, but have some limitations
1. Do not create / invent any fundamentally new domain entity directly in the data warehouse. If you must, do this deliberately and not as a side-effect of some other transformation.
1. Do not coalesce multiple attributes into a single attribute. Coalesces are hard to reason about. Instead, use records/structs to store multiple values.
1. Do not model anything in a visualization layer like Tableau/Looker. Those models are hard to reason about and can not be reused outside the tool.
1. Create multiple usage-centric views/aggregations of the same data instead of creating a Frankenstein's dataset. 
1. Tables should evolve using principles of API evolution. Create a new version, communicate to users, migrate and deprecate.

