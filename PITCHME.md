## Workforce Data Initiative

Open Skills Research Hub

Eddie Lin and Tristan Crockett

July 25, 2018

---

# What is WDI?

@fa[arrow-down]

+++

#### What is WDI?

The Workforce Data Initiative is a partnership launched by the Obama White House in 2015 as a partnership between public and private sector workforce data to facilitate standards, structure, and open access point for data underlying training, skills, jobs, and wages.

+++

#### What is WDI?

Work in WDI has been divided into two groups:

- *Open Skills Project* - Create a dynamic, open, common, locally relevant language for skills using public and private data. <- our focus today
- *Workforce Training Provider Scorecards* - Improve available information on education and training outcomes.

---

# What is the Research Hub?

@fa[arrow-down]

+++

#### What is the Research Hub?

The Open Skills Research Hub is a *collection of publicly available generated datasets* produced by the Open Skills Project from a pool of *public and private administrative data sources*, particularly job postings, for the purpose of *collaborative research*.

+++

#### What is the Research Hub?

The Research Hub is aimed primarily at the research community (e.g. labor economists, NLP researchers). One stated goal for the tabular datasets is for researchers not within the core development team at DSaPP to be able to publish whitepapers based on the data. At present, there are two public whitepapers that use Research Hub data.

+++

#### What is the Research Hub?

- Economists would like to answer a variety of questions about the labor market and how it changes over time and geography. Job ads can information about competencies, occupations, and wages that can be viewed across these axes.

- NLP researchers interested in the workforce would like to build on the work we've done in skills-ml

---

# What is in the Research Hub?

@fa[arrow-down]

+++

#### What is in the Research Hub?

- Tabular datasets grouping various attributes of job postings by time and geography
- Tabular datasets detailing different skill extraction methods, paired with evaluation metrics
- JSON-LD datasets each representing an ontology of competencies and occupations, usable by the skills-ml library
- Sequence-tagged labels of competencies for use in skill extraction algorithms

+++

#### Tabular datasets grouping job postings over time and geography

Goal: common entry points for economists, making single files as useful as possible. When possible, choose a 'safe' version of an algorithm like skill extraction to represent here.

- Counts of raw job titles by CBSA (and rolled up nationwide), with top skills, SOC codes, and wage data
- Counts of cleaned job titles by CBSA (and rolled up nationwide), with top skills, SOC codes, and wage data
- Counts of each SOC code by CBSA (and rolled up nationwide)

+++

#### Tabular datasets detailing skill extraction methods

Goal: a window into skill data by either more adventurous economists or NLP researchers looking for more details on the tradeoffs inherent in different skill extraction approaches.

- Exact match (ONET)
- Fuzzy match using levenshtein (ONET)
- Occupation-scoped Exact match (ONET)
- Noun-phrase based (noun phrases that end with certain key words like 'skills' or 'ability')
- bi-LSTM+CRF using human-labelled data from BRAT

+++

#### JSON-LD datasets

Goal:

+++

#### Sequence-tagged labels

Goal:

---

# Architecture

@fa[arrow-down]

+++

#### Architecture

![architecture](https://github.com/workforce-data-initiative/presentations/blob/gitpitch/images/research-hub-architecture.svg)

---

# Lessons Learned

@fa[arrow-down]

+++

#### Lessons Learned

First of slides under lessons learned sub-header
