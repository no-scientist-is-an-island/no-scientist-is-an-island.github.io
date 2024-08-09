---
layout: default
title: Code review
parent: Proposed workflow
nav_order: 3.3
permalink: /docs/workflow/code-review
---

# Code review
software developers check their code a lot; scientific data analysts and programmers can, too\!

<img style="float:right" src='../../files/review.png' width='85%' > 

## Process
* The code author documents the context and aims to write efficient, well-commented code that follows agreed-upon lab specifications to the best of their ability.   
* The code reviewer is ideally done with someone who did not write the code who  
  * verifies that the code works and produces the intended numbers  
  * provides feedback on elements including but not limited to the modularity, math and logic, and overall code (e.g., formatting, typos, comments, documentation)  
* The code author is responsible for implementing feedback

## Implementation
* Code review alongside the process (i.e., early\!) is more manageable and catches errors along the way.  
* Small chunks of code review (max 200 lines at a time) can prevent reviewer burnout.  
* Code review can be done synchronously in a face-to-face meeting with groups of varying sizes; it can also be done asynchronously. Either way, opportunities to ask questions can be helpful.  
* Software and AI may be helpful to an extent, especially for formatting consistency and errors.  
* A need to re-create environments may come up. (Link to resources: )  
* Culture matters. Sharing code can be vulnerable but will reduce errors and improve reproducibility. It is easier in a culture where perfection is not the expectation, but rather kindness.

## Example checklist

### For a code reviewer
- [ ] There is a clear top-level description of the script’s purpose  
- [ ] The code is modular  
- [ ] Running the code generates the identical output (if not, what changes are needed?)  
- [ ] Line by line, the code is logical and accurate  
- [ ] The overall script is organized sensibly  
- [ ] The code is formatted in agreed-upon ways (or is internally consistent)  
- [ ] The folder, file, variable names, and outputs are formatted in agreed-upon ways (or are internally consistent) and are names are sufficiently informative  
- [ ] The code is easy to follow   
- [ ] The script is included in the GitHub repository (if using)  
- [ ] Distinguish “must haves”/required changes  vs “nice to haves”/suggested changes  
- [ ] Raw data files are not overwritten or altered in any way  

#### Resources:   
**Rokem, A. (2024). Ten simple rules for scientific code review.**  
**Link:** Manuscript in press, direct link tbd. In the meantime, see [https://uwescience.github.io/neuroinformatics/2017/10/08/code-review.html](https://uwescience.github.io/neuroinformatics/2017/10/08/code-review.html)

**Pew Research Center Process**  
**Link:** https://www.pewresearch.org/decoded/2023/04/05/how-we-review-code-at-pew-research-center/
