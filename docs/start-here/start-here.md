---
layout: default
title: Start here 
nav_order: 2
permalink: /docs/start-here
has_children: true
---

# Start here

## What is a derived variable? 
When exploring data and running analyses, researchers manipulate raw data to create many kinds of new variables. Derived variables are variables that are computed from the raw data.

## What derived variables should I keep track of? 
We think a good general rule is that a derived variable (or set of derived varaibles) is likely worth tracking and logging if it is being included into models for analysis. Even simple derivations like summing questionnaire scores can yield different results depending on how you handle missing data, so making those choices transparent can facilitate reproducibility. 

Researchers may also choose to build a derived data registry that extends from a dataset that has already been minimally processed. For example, when using a large secondary dataset that has been scored by a centralized data management team, researchers might focus on logging variables they have derived beyond the existing scoring.

## What is a derived data registry? 
We propose the use of a derived data registry to track and share derived data. A derived data registry has three components: 
1. Derived data log
2. Code for generating derived variables
3. Derived variables