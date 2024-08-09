---
layout: default
title: Checking the registry
parent: Proposed workflow
nav_order: 3.1
permalink: /docs/workflow/log
---

## Getting started
You've thought of a data derivative--now what? The first step is to check the derived data registry, specifically the log, to see if someone else has already worked on this derivative, and if so, where are they in the [workflow](docs/workflow/workflow.md). Critically, completing this first step avoids unnecessary duplication of effort. If the derivative already exists, check to see if it works for your use or if you need to adapt it. If it doesn't exist, add it to the log as `logStatus`: `under development` and [create the derivative](docs/workflow/code-devo)! 

## logStatus

An key attribute in the registry log is the `logStatus`. This communicates to your group where you are in the workflow:

* <span style="background-color: #F88379">under development</span>: you've conceptualized the data derivative and are working on developing and testing the script to generate it
* <span style="background-color: #fcea50">under review</span>: the derivative is accurate and you're able to reproduce it--now it's time for code review!
* <span style="background-color: #24db2f">registered</span>: the derivative passed code review and is fully described in the derived data registry
* <span style="background-color: #d4d6d6">abandoned</span>: you have ceased working on this derivative and an explanation is included in the `description` field 
