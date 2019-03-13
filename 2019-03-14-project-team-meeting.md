---
date: '2019-03-14'
title: '**ACCASP Project Meeting 2**'
subtitle: 'Characterizing range shifts in British Columbia groundfish species in response to local climate velocities'
output: pdf_document
---

# Meeting objectives

1. Ensure everyone has an up-to-date understanding of the project objectives as
   defined in the ACCASP Proposal and the current status of this project.

1. Enhance familiarity with each other's strengths and expertise.

1. Use open discussion to establish a consensus around the high-level
   approaches that will be applied in implementing this project.

1. Define publishable units and ways to make results relevant to DFO science
   and fisheries management.

1. Become familiar with each team member's interest, available time to devote
   to this project, and goals in terms of authorship.

1. Assess progress towards stated project milestones and set a draft timetable
   going forward.

1. Brainstorm list of potential technical break-out group tasks.

1. Work in teams on group tasks to hopefully clear some important analytical and
   conceptual hurdles.


## Day 1: Thursday, March 14th 2019

Colvile Room, **Coast Bastion Hotel**, 11 Bastion Street, Nanaimo

9:00 am -- 4:00 pm

### Meeting agenda

* Introductions

* Welcome and review of meeting objectives and agenda

* Review of stated deliverables and timeline (Sean/Philina)

* Any brief presentations on related work from working group members

* Brief review of data sources (Sean/Philina)
    - Synoptic trawl surveys
    - Hard-bottom long-line
    - Sablefish
    - Halibut (Andy)

* Functionality now built into the sdmTMB model (Sean)
    - Spatial and spatiotemporal or independent spatiotemporal random fields
    - A complete set of families and links
    - Prediction on new data sets through a predict() function with a full predictive-process projection
    - AR1 spatiotemporal random fields (new)
    - Time-varying parameters (new)
    - Centre of gravity calculations (new)
    - Standard errors on predictions (new)
    - Ability to input arbitrary INLA meshes (new)

* Simulation testing of the sdmTMB model (Philina)

* Overview of environmental sensor data (depth, temperature, dissolved oxygen, salinity)
    - data availability
    - basic data quality checking and cross-correlations (Philina)
    - preliminary models of environmental variables for projection grids
        - TMB (Sean)
        - INLA (Philina)

* Visualizing time-varying depth and temperature effects through time (Sean)

* High-level discussion/brainstorming of how to achieve project objectives:

    - Start with free idea sharing
    - Provide opportunity for idea refinement, clarification, and discussion of broad conceptual approaches
    - Discuss how to define publishable units

* Technical discussion of how to achieve project objectives:

    1. Parameter-focused inference vs. projection-based inference (e.g. weighted-mean temperature)
    1. Salinity projection issues
    1. Should synoptic survey regions be treated separately or stitched together?
    2. Modeling frameworks: TMB vs. INLA vs. Stan vs. machine learning
    3. Should we attempt to use other survey data: IPHC, HBLL (inside and outside), sablefish?
        Which environmental variables do these other surveys collect?
    4. How do we model all 3 spatial dimensions of climate velocity (latitude, longitude, depth) and variables (temp, salinity, O2)?
    5. Are centre of gravity and area of occupancy appropriate response variables for Canadian waters?
    6. Do we want to account for size structure of populations?
    7. Should we consider multi-species covariance?
    8. Species to focus on

### Break for lunch

* Broader scope planning (while most people are present)
    - Review project objectives, deliverables, and timeline
    - Discuss each team member's interests, availability, and desired roles
    - Set goals and guidelines for on-going collaboration

* Brainstorming of ideas for breakout group topics:

    - Some possibilities include:
        1. Brainstorming visualizations approaches.
        1. Searching broadly for any relevant literature we might have missed.
        1. Implementing a random walk for environmental covariates in R-INLA (time varying quadratic effects of O2, temperature, depth and salinity).
        1. Implementing and comparing barrier models in R-INLA
        1. Implementing area of occupancy calculations and weighted average temperature etc.
        1. Brainstorming our hypotheses for expected outcomes. Are there expected patterns across species groups because of their biology? Are there existing hypotheses for some species groups and regions?
        1. Improving environmental projection model or theory behind those.
        1. Developing or completing spin-off projects? E.g. Robyn's cumulative depth profile work.
        1. Reviewing guidelines for INLA meshes and developing a defensible mesh for our surveys/coastline.

* Choose priorities and who should tackle which problem in breakout groups

* Start breakout groups

## Day 2: Friday, March 15th 2019

Room T325 (old library room), **Pacific Biological Station**, 3190 Hammond Bay Road, Nanaimo

9:00 am -- 2:00 pm

* Welcome back and review of breakout group objectives and any progress from previous afternoon

* Breakout-group work (remainder of the morning)

* Review conclusions from both discussions and breakout-group work

\clearpage

# Authorship agreement

We will adopt the authorship guidelines from the Nutrient Network research consortium, which specifies that one must meet at least two of the criteria in the table below to qualify for authorship on any given paper. Expectations for our authorship agreement include additional participation as requested by the leads of each paper, including but not limited to timely comments and edits on the manuscripts themselves. All authors will be asked to state how they plan to contribute to each paper moving forward and this information will be kept in a file shared with all participants. Additional authors will be invited based on need of their expertise. Final decisions on authorship are up to the lead of each paper and workshop chairs.


+---------------------------------+---------------------------------+
| **Authorship Rubric**           | **Example Contribution**        |
+---------------------------------+---------------------------------+
| Developed and framed research   | Originated idea for analysis as |
| question(s)                     | PI or co-PI; contributed        |
|                                 | significantly to framing the    |
|                                 | ideas in this analysis at early |
|                                 | stage of manuscript             |
+---------------------------------+---------------------------------+
| Data coordinator                | Coordinated data collection,    |
|                                 | proofing, and submission of     |
|                                 | data for at least one dataset   |
|                                 | used in this manuscript         |
+---------------------------------+---------------------------------+
| Analyzed data                   | Generated models (conceptual,   |
|                                 | statistical and/or              |
|                                 | mathematical), figures, tables, |
|                                 | maps, etc.                      |
+---------------------------------+---------------------------------+
| Contributed to data analyses    | Provided comments, suggestions, |
|                                 | and code for data analysis      |
+---------------------------------+---------------------------------+
| Wrote the paper                 | Wrote the majority of at least  |
|                                 | one of the sections of the      |
|                                 | paper                           |
+---------------------------------+---------------------------------+
| Contributed to paper writing    | Provided suggestions such as    |
|                                 | restructuring ideas, text and   |
|                                 | citations linking to new        |
|                                 | literature areas, copy editing  |
+---------------------------------+---------------------------------+

# Supporting documents

### ACCASP Proposal

https://www.dropbox.com/s/ot9xbtz60skrok8/ACCASP-proposal-gf-rangeshifts-2018-09-06.pdf?dl=1

### A reproducible data synopsis for over 100 species of British Columbia groundfish (in press)

https://www.dropbox.com/s/r0uf3tp21yf6dt0/pbs-gf-synopsisv0.7.2.pdf?dl=1