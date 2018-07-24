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

- *Open Skills Project* - Create a dynamic, open, common, locally relevant language for skills using public and private data. **<- our focus today**
- *Workforce Training Provider Scorecards* - Improve available information on education and training outcomes.

---

# What is the Research Hub?

@fa[arrow-down]

+++

#### What is the Research Hub?

The Open Skills Research Hub is a *collection of publicly available generated datasets* produced by the Open Skills Project from a pool of *public and private administrative data sources*, particularly job postings, for the purpose of *collaborative research*.

+++

#### What is the Research Hub's Audience?

The Research Hub is aimed primarily at the research community (e.g. labor economists, NLP researchers). The goal is for these external researchers to be able to publish whitepapers based on the data. At present, there are two public whitepapers that use Research Hub data.

+++

#### How can the Research Hub help the Audience?

- Economists would like to answer a variety of questions about the labor market and how it changes over time and geography. Job ads can information about competencies, occupations, and wages that can be viewed across these axes. We are able to 

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

- Grouping columns: CBSA, year, raw/cleaned job titles or given ONET SOC codes
- Aggregate columns: Counts of job postings, top extracted skills, top inferred SOC codes, wage data

+++

#### Tabular datasets detailing skill extraction methods

Goal: a window into skill data by either more adventurous economists or NLP researchers looking for more details on the tradeoffs inherent in different skill extraction approaches. For each approach, package basic counts (year/soc code) alongside basic evaluation metrics

+++

- Skill extractors: matching based on known competency framework strings, heuristic NLP approaches (e.g. noun phrases that end in 'skill/s'), trained models based on human-labelled data
- Example Metrics: Recall of known competency frameworks (overall and per-occupation), total competency count, competencies per posting, competencies per occupation

+++

#### JSON-LD competency ontologies

Goal: Release known competency frameworks in the same format to inferred ontologies. Using the CTDL-ASN format, we can point the skills-ml Ontology class at URLs here to provide pre-mapped ontologies for use without bundling large datasets in the library code

- Mapping of ONET competencies/occupations
- Can map results of skill extraction to ontologies, but the results are public so we don't need to be the people to do this

+++

#### Sequence-tagged labels

Goal: Release human-tagged labels so NLP researchers can improve on skill extraction approaches without needing to access private data.

Human-tagging is done on a small sample of job postings that we can release so someone externally can build on this work to build a model using their own feature engineering.

---

# Architecture

@fa[arrow-down]

+++

#### Architecture

![architecture](images/research-hub-architecture.png)

---

# Lessons Learned

@fa[arrow-down]

+++

#### Lessons Learned

First of slides under lessons learned sub-header
