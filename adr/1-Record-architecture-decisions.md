
# 1. Record architecture decisions
======
Date: 30-01-2022 01:30:44

## Status
======

Accepted

## Context
======

We need to record the architecture decisions made on this project to ensure the team has a common understanding of which decisions were made and, more importantly, why they were made.



## Decision
======

We will use Architecture Decision Records, as described by Michael Nygard in [this article](http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions)

We will use [go adr tool](https://github.com/marouni/adr).

This tool can be installed by 
```
go get github.com/marouni/adr
go install github.com/marouni/adr@latest
```
and we can use 
```
adr new amazing architecture decision
``` 
to create new ADR.

## Consequences
======

One ADR describes one significant decision for the project and all ADRs are published along with the project code.

