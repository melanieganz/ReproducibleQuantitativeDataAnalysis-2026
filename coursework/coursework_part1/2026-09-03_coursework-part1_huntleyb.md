# Reproducibility in my PhD research: current state and planned measures

**Author:** Huntley Brownell (hb@ign.ku.dk)
**Course:** Reproducible Quantitative Data Analysis 2026 — Coursework Part 1
**Date:** 2026-09-03

## Where I start

In my PhD I work in the area of forest modelling. This has largely taken the shape of applying empirical projection models or machine learning models to existing data. I began with tabular data of tree and plot measurements extracted from two different databases in my department, one an archive of long-term experiments dating back to 1871, and a second of National Forest Inventory data from 2003 to 2023. There are collectively millions of individual tree records in these databases. As the data includes location, I have been able to augment our data with open geodata from various sources. I have also been working with LiDAR point cloud data collected from national airborne laser scanning campaigns covering all of Denmark.

The department databases are all tabular data, and live in the antiquated and proprietary .sasdb format. I've no interest in learning a dying programming language so the extractions have been done by my supervisor or database manager based on my wishes - i.e., they have written a script in SAS to extract the data from the database and save it to .csv format. Perhaps you can imagine that this introduces the first complication in terms of data provenance, since the extraction code may have bugs and live on the local machine of the person doing the extracting, etc. These files are hundreds of MB in size but can still be opened on a laptop and saved locally, etc. The LiDAR data is of a different magnitude and so far amounts to around 25 TB. The most recent national scan was around 18 TB. This requires a different pipeline to work with; it is stored on network drives in archive form but processing must take place on an HPC with a local copy.

For analysis, when I began the PhD I realised I needed to learn to code. Previously as a research assistant working with data I had built a large and complicated excel modelling framework for an earlier project. I think it was as well-designed as it could be for an excel workbook in terms of reproducibility and transparency, but this was incredibly difficult to do, so it was obvious that any future data projects I would undertake had to be in code, mainly for reasons of provenance - i.e., so I could check all the calculations and transformations of data more easily than if they were buried in formula cells. I was just becoming proficient in python when agentic coding arrived in my IDE, and that has transformed the way I work with code and data. I think these tools offer great potential in terms of standardising best practices - for example, I could easily add guidelines and instructions for agents to follow in terms of file naming, version control, etc., and these could easily be standardised across sections or departments.

However, this still requires some effort to set up. And some of my projects began before the arrival of these tools so grew in a very organic fashion; naturally I eventually ran into many of the problems described in this course with file and directory names not maintaining coherence. I also have been collaborating with others, sharing data that I have processed on our network drive, and this of course has also caused version control problems. However, as I have been learning from this course I have begun to apply better practices - but still face limitations when collaborating with others who are not used to using version control tools like git, or cannot read my python data processing code, or have not yet discovered agentic coding tools that could convert my python code to their R code or whatever they are using.

## Measures already in place

So I would say that I had already begun following some best practices "by accident" because they also make your life easier - one project one folder, readme files in project directories (once I began collaborating with others), and I recently began to use git and encourage others in my department to switch to open data formats instead of proprietary ones.

---

### Summary of current practice

| Measure | Lecture | Status | Note                                                                                                                  |
|---|---|---|-----------------------------------------------------------------------------------------------------------------------|
| **Planning** | | |                                                                                                                       |
| Written data management plan | 1.02 | Not yet | No DMP; data management has been ad hoc                                                                               |
| Analysis plan fixed before results | 1.05 | Not applicable | Everything has been exploratory so far - perhaps less applicable since I have existing data?                          |
| **Organisation** | | |                                                                                                                       |
| One project = one folder | 1.02 | In place | Adopted early on, especially once I started using an IDE for my own convenience                                      |
| `README.md` in project directories | 1.02 / 1.07 | In place | Began doing so recently - wish everyone in the department did on network drives!                                      |
| Consistent file and directory naming | 1.02 | Partial | Older projects grew organically before conventions settled, once I started coding I saw the need for good names       |
| **Provenance** | | |                                                                                                                       |
| Extraction from source database scripted and archived | 1.03 | Not yet | SAS extraction scripts live on the extractor's local machine                                                          |
| Raw data immutable, separate from derived | 1.03 | In place | Raw extracts kept separate from processed outputs                                                                     |
| Processing in code rather than GUI or spreadsheet | 1.03 | In place | Deliberate move from an Excel framework to Python                                                                     |
| Metadata describing collection and processing | 1.02 / 1.03 | Not yet | No metadata written to accompany the extracts                                                                         |
| **Storage and formats** | | |                                                                                                                       |
| Open, non-proprietary formats for working data | 1.02 | Partial | `.csv` working copies extracted from proprietary `.sasdb` sources                                                     |
| Backup distinct from archive | 1.02 | Partial | LiDAR archived on network drive, working copy on HPC, forest data backed up with multiple copies and also Rigsarkivet |
| **Code** | | |                                                                                                                       |
| Analysis code under version control | 1.08 | Partial | Recently adopted                                                                                                      |
| Dependencies pinned with versions | 1.04 | Partial | Recently begun but still need to add versions                                                                         |
| Code shared publicly / archived with a DOI | 1.01 / 1.04 | Not yet | Planned                                                                                                               |
| **Collaboration and sharing** | | |                                                                                                                       |
| Single authoritative version of shared data | 1.02 / 1.08 | Not yet | Network-drive sharing has caused divergent copies                                                                     |
| Collaborators can re-run the analysis | 1.01 / 1.04 | Not yet | Collaborators work in R and do not use git                                                                            |

* Note that this table/checklist was compiled using AI tools. Lecture numbers refer to the day 1-2 slide decks: 1.01 Definitions & Origins,
1.02 Storing Data & Code, 1.03 Data Provenance, 1.04 Reproducibility is Hard,
1.05 Documentation & Pre-registration, 1.07 Markdown for Documentation,
1.08 Version Control & Social Coding.*

## Measures I can take to increase reproducibility

It is noted in the table above where I fall short of best practices - it occurs to me that in the collaborative research environment we all have a responsibility to advocate for best practices and encourage others in our departments to follow them. I will also incorporate these principles into my future advising of students. The easiest things to implement are improvements to my own practices. Again, I suggest that with the right safeguards, it would be straightforward to set up an AI agent to enforce these rules and ensure best practices are followed. Collaboration with others is a little more challenging, but I think there is low-hanging fruit - always including copies of data extraction scripts for auditability (and this can be built into the script itself) as well as metadata. And I can certainly draft a DMP. Though I did not do it for my last paper, for future papers I will publish the code I used, though much of the forest inventory data we have cannot be made public. I need to learn how to share analysis code for data that cannot be released (are there best practices for this?).

## Measures that are more difficult or that I am uncertain about

I won't be able to get the department to drop the proprietary file formats anytime soon, but we have actually set up a parallel PostgreSQL database for our departmental data (of course we have to make sure it is updated from the true original!) that I will encourage everyone to begin using so we can maybe transition fully, eventually. I can also make sure all of my directories on the network drive have readme files, and I can also place my extraction/processing scripts there alongside the data when I share it with others so they can use it even if they aren't familiar with git. I'd like to learn more about alternatives to our network drive system for storing and sharing code that don't include commercial services like github that can disappear.
