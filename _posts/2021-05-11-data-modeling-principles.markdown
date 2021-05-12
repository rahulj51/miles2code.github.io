---
layout: post
title:  "16 fundamental principles for transforming data in a warehouse"
date:   2021-05-11 20:30:00
categories: Data datawarehouse 
---

The current discourse on data can get a little tiring because of its [over focus on tooling](https://twitter.com/rahulj51/status/1254447785170042882). It feels like a new SaaS gets launched every week in the data space. This, however, should not be at the cost of establishing basic, first-principles understanding of data engineering. 

Here's a short list of some fundamental principles for organizing and transforming data in a warehouse. These are concepts that my team and I learned the hard way in the course of building our data warehouse at Omio over last three years.

The list does not address the question of what storage type to use (data lake vs warehouse vs marts), nor obsesses over Kimball vs Inmon vs Linstedt style of modeling. Instead, it addresses concerns that are somewhat orthogonal to these choices. 

As you will notice, this is a highly opinionated set of guidelines. The reader is advised to not treat these dogmatically, nor get triggered by some seemingly extreme views. Most of these principles are very contextual, of course. YMMV. :-)


![/assets/data-modeling/data-model-arch.png](/assets/data-modeling/data-model-arch.png)   

#### Principles for Data Transformations (*in no specific order*)

1. Practice immutability. Each row should written only once to the table. In other words, do not insert a row and then update it in a subsequent step. 
1. Break complex transformations into smaller sub-steps. Adopt single responsibility.
1. Delay joining tables from different data sources. Decoupling helps manage changes better.
1. Ensure that all Facts/Events have a business timestamp and an arrival/etl timestamp.
1. Perform upserts by primary keys only. Never delete-insert based on timestamps alone.
1. Avoid upserts if you care about [bitemporal](https://martinfowler.com/articles/bitemporal-history.html) history. 
1. Avoid cleaning data. Cleaning data is an anti-pattern. If you must, do this in a separate step in the transformation flow.
1. Do not model anything motivated purely by ease-of-use or convenience. Each transformation step must add "value".
1. Avoid querying source tables that are more than 2 layers below the target layer (see diagram above).
1. Never re-implement any business logic from source systems in the warehouse. 
1. Use un-materialized views wherever possible for aggregations (Views are relatively cheaper to build and modify, but have some limitations)
1. Do not create/invent any fundamentally new domain entities directly in the data warehouse. If you must, do this deliberately and not as a side-effect of another transformation.
1. Do not coalesce multiple attributes into a single attribute. Coalesces are hard to reason about. Instead, use records/structs to store multiple values.
1. Do not model anything in a visualization layer like Tableau/Looker. These models are hard to reason about and can not be reused outside the tools.
1. Create multiple usage-centric views/aggregations of the same data instead of creating a Frankenstein's dataset. 
1. Adopt an evolution strategy for your tables using principles of API evolution. Create a new version, communicate to users, migrate and deprecate.

