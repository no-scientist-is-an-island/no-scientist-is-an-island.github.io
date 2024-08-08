---
layout: default
title: Setting up a derived data registry
parent: Start here 
nav_order: 2.1
permalink: /docs/start-here/registry-setup
---

# Setting up a derived data registry

## Assumptions
This setup assumes that researchers are working from a shared primary dataset, have some way to store those data, and work on analyses in project folders. 

Derived data registries should be flexible enough to work regardless of your project folder structures. However, we have two recommendations: 
1. Place project folders in spaces that are shared with team members when possible (e.g., Dropbox, Sharepoint, Box, or your institution's preferred platform). That way, people can understand the context that variables were created in, and can collectively monitor to see if the derived data registry becomes outdated.  
2. Considering adopting a data specification format that is internally consistent across the lab. One option is [Psych-DS](https://docs.google.com/document/d/1u8o5jnWk0Iqp_J06PTu5NjBfVsdoPbBhstht6W0fFp0/edit), an emerging standard (under development) modeled after the [Brain Imaging Data Structure (BIDS)](bids.neuroimaging.io/). Following this data specificaiton standard may foster a more robust science by making it easier for researchers to easily understand one another's project files, including code and analysis.

## Parts of a derived data registry 
A derived data registry has three components: a log, code, and data. This can be a folder with three sub-folders. There can be benefits to tracking this folder using git and GitHub, which supports version control. 

### Derived data log
Here, information about each derived variable (meta-data) is logged. The Psych-DS specification logs this information using a .json file, but a .csv file, or other tracking systems (e.g., Google spreadsheets) can also work. 

In accordance with Psych-DS, we suggest recording some or all of the following information for each variable: name, description, value, identifier, minValue, maxValue, levels, levelsOrdered, na, naValue, alternateName, privacy (see Section 6.1.1 of [Psych-DS](https://docs.google.com/document/d/1u8o5jnWk0Iqp\_J06PTu5NjBfVsdoPbBhstht6W0fFp0/edit) for more details)

Additional meta-data that we recommend specifically for derived variables is described below:  

| Name            | Schema.org type | Definition |
| --------------- | --------------- | ---------- |
| **derived**     | Boolean         | Whether variable was derived. `derived: true` |
| **varAuthor**   | Person          | If the variable is derived, a list of people who contributed to the creation/curation of the derived variable: <br> `"varAuthor": ["Melissa Kline", "Tal Yarkoni"]` <br> or <br> `"varAuthor": [ { "@type": "Person", "givenName": "Melissa", "familyName": "Kline", "identifier": "https://orcid.org/0000-0003-2217-9331" }, { "@type": "Person", "name": "Tal Yarkoni" } ]` |
| **reviewers**   | Person          | A list of people involved in reviewing its code. See format above. |
| **lastUpdated** | Date            | Date this object was last updated; `“YYYY-MM-DD”`. `"lastUpdated": "2024-08-07"` |
| **gitSha**      | String          | Alphanumeric chain associated with the git commit when the code and data were uploaded to the registry. |
| **logStatus\*** | String          | Status of the derivative; one of `“under development”`, `“under review”`, `“registered”`, or `“abandoned”`. `"logStatus": "under development"` |
| **inputVars**   | String          | Names of variables in the raw dataset that this variable is derived from. `“inputVars”: “raw_var_1”, “raw_var_2”` |
| **transformations** | String     | Mathematical operations and/or text description, including all raw variable names listed in `inputVars`. `“transformations”: sum of Z-scored raw_var_1 and Z-scored raw_var_2”` |
| **subset**      | String          | Description of the sample the variable was calculated on (i.e., were there any exclusions?). `“subset”: “participants ages >= 8.0 years with complete data on inputVars”` |
| **inputMissingness** | String     | Description of how missingness on input variables was handled. `“inputMissingness”: “calculated for participants with complete data on inputVars, otherwise NA”` |
| **n**           | Integer         | How many participants this variable exists for. `“n: 249”` |

## Derived data code
Code uploaded to this folder should produce a single variable or one set of highly related variables that undergo a similar transformation process. The file name should contain the name of the variable or variable set. For more information about developing this code, see (ADD LINK).

## Derived data
This folder is populated with tabular data files for each variable or set of variables according to agreed-upon file format (e.g.,  .csv or .rdata). File names should include the name of the variable or variable set. Within each file, the first column(s) should included with any identifiers (id, session, etc). 

The contents of this folder should only be shared with those that have permissions to view the data. If you are using git for version control and the data cannot be uploaded, consider adding this folder to your ().gitignore file)[https://git-scm.com/docs/gitignore/en]