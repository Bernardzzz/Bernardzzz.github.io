---
layout: post
title:  "How to truncate tables in PostgreSQL without downtime"
date:   2018-12-15 12:29:00 +1100
categories: lost & found
---

## Scenario

A few months ago, one of the PostgreSQL databases I'm working on was about to ran out to storage. Since the database instance is hosted at AWS RDS, there was no way to expand the storage space without downtime([Now RDS supports zero downtime storage space modification]())

## Prerequisites

Why would you need to truncate tables in PostgreSQL? The approach in this post only applies to situations which meet the assumptions below.

1. The database users do not specify schema name in the queries.
2. There is no reading operation on the tables you want to truncate.

## The trick




