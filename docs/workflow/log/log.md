---
layout: default
title: Logging Your Progress
parent: Proposed Workflow
nav_order: 2.1
permalink: /docs/workflow/log
---

# How to log your progress

An important interaction with the derived data registry is to regularly update your derivative's status. This status (`logStatus` field in the registry) communicates to your group where you are in the workflow:

* <span style="background-color: #F88379">under development</span>: you've conceptualized the data derivative and are working on developing and testing the script to generate it
* <span style="background-color: #fcea50">under review</span>: the derivative is accurate and you're able to reproduce it--now it's time for code review!
* <span style="background-color: #24db2f">registered</span>: the derivative passed code review and is fully described in the derived data registry
* <span style="background-color: #a1a4a5">abandoned</span>: you have ceased working on this derivative and an explanation is included in the `description` field 
