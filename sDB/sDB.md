# Introduction 

** Oliver Nakoinz**

- Introduction: Vision
- Introduction: Reality
- Data types and structures
- Databases
- Metadata
- Workshop


## Introduction: Vision

> **Task**: Provide research data according to the FAIR principles and to the reproducible research philosophy in a manageable way considering the practical conditions.

- Challenge 1: Maintaining databases is very time consuming

    - Solution 1: Simple and permanent solutions (text based system, minimal software requirements, suitable for long term storage, git for versioning and gitlab for multiuser)

- Challenge 2: Project resources tend to drain after some data are produced and there is no time for proper data publication 

    - Solution 2: Efficient template based workflow 

- Challenge 3: Complicated databases prevent its practical use

    - Solution 3: shifting structural complexity to content complexity, differentiation of core data and additional data, de-normalisation, few tables and columns

- Challenge 4: Rigid structures are not compatible with the heterogenity of research approaches.

    - Solution 4: Flexible structures (ontologies and terminologies are data and not fixed, key-value, translation)

- Challenge 5: The concept of dynamic databases is not consistent with the concept of reproducible research

    - Solution 5: Publication of file based database snapshots that are used for certain purposes and are products of their own rights

- Challenge 6: Communities tend to use specific repositories

    - Solution 6: Submit to different data repositories and connect the items (e.g. one doi)

- Challenge 7: Binary attributes do not map reality.

    - Solution 7: Probabilities or membership values attached

- Challenge 8: Documentation can be lost

    - Documentation as complementary text based file side by side with the data

    
## Introduction: Reality

- Lots of old data

    - analogue 

    - pdf

    - xls
    
    - mdb
    
    - postgresql
    
    - sqlite
    
- Active data: project folders with .csv 

- Supportive material: R-packages and Gitlab repositories for specific purposes 

    - ArchChron (methods for handling chronological data on Gitlab)
    
    - dataArch (archaeological data in R-Package ON Gitlab)
    
    - chronsys (collection of chronological systems on Gitlab)
    

- Target repositories 

    - Gitlab 

    - Zenodo 

    - ArkeoGIS 
    
    - opendata@uni-kiel 
    
    - JMA data exchange platform 
    
    - Landman (CRC 1266) 


# Data types and structures

- Numbers
- Text
- Quality assessment
- Spatial data
- Chronological data
- Complex data

*no binary datatypes that require special software (e.g. postgis)!*

## Numbers

* id or uuid

* 37

* 30e23524-df31-11ea-89f8-f894c2a8d12b

- id_parent or uuid_parent

- frequencies of measures

    - 55

    - 65.234753

## Text fields

- name: site names, ...  

    - "Wees-Oxbuell, Steingrab 19"

- cat_no: id of the original catalogue

    - "254a"

    - "43.56.1"

    - "42.45, KS1907.23b"

- class: general category

    - "site"

    - "part"

    - "structure"

- type: object classification

    - simple: "megalithicTomb"

    - string: "grave>megalithic_tomb"

    - comment: consider names that can be turned to proper column names (no spaces and special characters)

- comment

    - "this is an extraordinary site"

## Quality assessment

- location_q: int: quality of location

    - 3: some m

    - 2: about 100 m

	- 1: about 1000 m

	- 0: unknown

- chron_q: num quality of dating

	- 3: save dating with precision of few phases

	- 2: probable dating with precision of at least of epochs (e. g. Preroman Iron Age)

	- 1: plausible dating to broad epochs Metal Ages

	- 0: no chronological information

- info_q: num general quality

	- 3: site exists and location_q and chron_q are 2 or better  

	- 2: site exists and location_q and chron_q are 1 or better

	- 1: site existence questionable or location_q or chron_q are 0 or

	- 0: site does not exist


## Space (Coordinates)

- `x`, `y`, num: coordinate columns

    - 559814.7231

    - comment: points only

    - comment: avoid geographical coordinate system unless the area is extensively large and use projected systems instead

- `WKT`, chr:    coordinates WKT format (SRID=32632 (epsg) in metadata or ewkt)

    - "Point (559814.7231 6056013.7338)"

    - comment: each simple feature geometry possible

    - comment: readable by GIS and by humans

## Time (Chronology)


- chronological Strings:

    - `chronologySystem_Chronologystring_MembershipValue`

    - "fortME_Vorg>EZ>Lt>FLT>LtA_1.0, fortME_Vorg>EZ>Lt>FLT>LtA1_0.5"

    - `14C_LabNo_BP_1sigma`

    - "14C_Poz-16047_3510_30"

- chronological reference system at chronsys gitlab repository



## Chronology Reference: Traditional approaches

- [https://perio.do/en/](https://perio.do/en/)

    - does not consider chronological hierarchies

    - download (.csv possible) mainly contains links, hence, not usable for reproducible research.

- [https://chronontology.dainst.org](https://chronontology.dainst.org)

    - online only (download (.json only) for single phases only and no text based download), hence, not usable for 
    reproducible research.
    
    - not organised based on chronological systems


## Chronology Reference: chronsys (Gitlab Repositorium)

- [https://gitlab.com/oliver.nakoinz/archchron](https://gitlab.com/oliver.nakoinz/archchron)
- csv-files focused on chronological systems and hierarchical order
- columns:

    - **c_system**: name of the chronology system

    - **id**: identification number inside the chronology system

    - **p_id**: id of the superior entity

    - **c_level**: hierarchy level starting with the most general entity

    - **c_order**: order inside one hierarchy level

    - **datstring**: chronology string

    - **name_short**: short name, must be identical with the last phase name of the chronology string, avoid tailing spaces

    - **name_long**: more comprehensive name of the phase

    - **start**: start year of the phase, negative means BC, same year as end year of the previous phase

    - **end**: end year of the phase

- interval scale (0 and - 55.3 are valid) instead of numerical lables for years

- now web-view, just data

- You can easily construct your own chronsys-csv-file


## Complex data


- user defined desciption language, text

- example: Fortification Description Language (FDL)

    - $(b1,2(b3(d134,3)))$ is a ring wall with murus gallicus and ditch. This is preceded by a section ditch and this in turn 
    by a section rampart with ditch.
    
    - $((d1)(c1))$ is a ring wall and an adjoining, i.e. adjacent, semicircular rampart.

    - $(d1(d1,1)))$ three nested ring ramparts, the innermost of which has a ditch. 

    - $c1\subset(d1)$ a semicircular extension added to a ring rampart. The enclosure may not be complete. 

    - $(b1{d1})$ secure section rampart with more uncertain ring rampart.

    - ${b1(d1)}$ secure ring wall with insecure section wall

    - $(b1);(b1)$ two m.w. facing section ramparts

    - ${d1((d1);(d1))}$ two separate ring ramparts surrounded by an insecure comprehensive ring rampart

    - $((<b1(<b1)(b1>))$ two section walls directed to the left and one to the right close off an area.


# Database

- Principles
- Format
- Denormalisation
- Tables
- Key-value


## Principles

- as few tables as possible
- as few columns as possible
- not ignoring normalisation completely but focus on targeted denormalisation
- core content in one or few main tables
- additional content (sparse or less relevant) in an additional key-value table

## Format 

- File based formats in reproducible projects

    - text based formats (e.g. .csv) if possible

    - established and simple binary formats (e.g. sqlite) if required

- No server based formats in reproducible projects

    - snapshots to files allowed

- No xls., .mdb, .dbase etc.!

- No Excell for working with data

    - OO or LO calc is allowed

## Denormalisation

- combine names in one field (searching much easier)
- use complex text fields (e. g. wkt)
- allow for flexible hierarchies with references inside tables
- consider the power of regex


## Tables

- use same or similar structure for tables if possible

- example:

    - sites

    - features

        - same structure as sites

        - if the size of sites of the main table would grow to fast, otherwise can be included via class field ("sites" and "features")

    - chronsys

    - key-value

    - thes

## Key-value

- allows for 

- KeyValue.csv table

    - **id**: int, id or uuid

    - **table**: chr, table name to which the entry belongs 

    - **id_secondary**: int, row to which the entry belongs

    - **key**: chr, category of value (to be explained in the metadata)

    - **value**: chr, value



# Metadata

- Dublin Core and .yaml
- Example

## Dublin Core and .yaml

- [Dublin Core](https://www.dublincore.org) defines meta data categories
- [yaml](https://yaml.org) is a simple hierarchical serialization language that can be stored in text files
- every data file should be joined with a associated .yaml metadata file with the same name that is the basis for filling the metadata in the different repositories

## Metadata: yaml

```{}
---
contributor:     author1name, author1email, author1orcid; author2name, author2email, author2orcid
creator:         creator1name, creator1email, creator1orcid
location:        DE, 
period:          Bronze Age, Iron Age
date:            2022
subject:         archaeological sites
title:           xxxxdataname
type:            sites 
version:         1.0.0
description:     
    - `id`, int:     identification number
    - `cat_no`, chr: catalogue number according to Willroth
    - `name`, chr:   site name
    - `type`, chr:   site type:  refer to thes.csv
    - `chron`, chr:  chronology string according to https://gitlab.com/oliver.nakoinz/chronsys/-/blob/main/landscWillroth1992.csv with tailing probabilities
    - `comment`, chr: any comments, German
    - `source`, chr: particular source information
    - `location_q`, int: quality of localisation (refer to thes.csv)
    - `chron_q`, int: quality of chronological dating (refer to thes.csv)
    - `info_q`, int: general quality of the information comprising chron_q, location_q and general quality of observations (refer to thes.csv)
    - `WKT`, chr:    coordinates WKT format, SRID=32632, precision=site (see column location_q for specific information)
source:          xxxreference
language:        en, de  
rights:          https://creativecommons.org/licenses/by/4.0/
format:          csv, sep=";", utf-8
---
```

# Worlflow 

## Worlflow

1. Explore data
	- What kind of data are available in which form?
	- How are the Components (documents and details) related?
	- Are there different versions of the data?
	- How can we handle different versions?
	- Where are gaps in the data?
	- How can we fill the gaps by combining data or including external data?
	- Which information has to be extracted from the documents in which way (sql, copy paste, ...)?
	- Which coordinate system is in use?
	- Which chronological system is in use?
	- Which data are redundant?
	- Which data are relevant and which are not?
	- Which data are core-table data and which one additional?
	- What do we know about the quality of the data?
2. Make decisions
	- licence
	- data to include
	- core-table data
		- non-standard columns
	- key-value data
		- categories
3. Create tables (usually .csv) and metadata files (.yaml)
	- main tables in standard format (e.g. sites)
		- add non-standard fields
	- key-value table
	- chronology table
	- dc-yaml-metadata for each file
4. Fill tables and metadata
	- create a row with id for each entity
	- insert original identifications
	- fill in names, comments etc.
	- fill spatial data (usually wkt) by
		- copying of original spatial data
		- transforming original coordinated to wkt
		- projecting original coordinates
		- geo-referencing and digitising maps
		- obtaining coordinates for the places as approximation of unknown sites
	- fill in chronological information with chronology strings
	- filling other details into the main tables
	- filling the key value table
5. Review and preparations
	- Mowing documents to a separate folder
	- reviewing the content
	- testing the content 
		- conting entries
		- mapping the content
		- searching the column names for problematic characters (including space)
		- filtering  empty fields etc. 
		- searching for duplicate entries or duplicate ids
6. Planing dissemination of data
	- deciding for target platforms
	- if necessary (e. g. ArkeoGIS: making copies and adapt the format (usually by scripting)
	- filling in metadata forms (e.g. landman)
	- submitting data

# simple Data Base (sDB)  {background-color="#9DB2CB"}

## sDB Principles

- based an the concept of relational data bases
- targeted denormalisation
- file based
- simple concept
- easy to maintain
    - text based system 
    - minimal software requirements
    - suitable for long term storage
    - key-value allows to include additional content without changing the structure
    - UTF-8 encoding (mandatory!)
- easy to use
    - few tables
    - few columns
    - shifts structural complexity to content complexity
    - differentiation of core data and additional data
- supports reproducible workflows
    - enables git based development of projects and content
- flexible
    - minimal standardisations
    - suggests certain standardisations
    - does not force to use specific thessauri or chronology systems
- metadata included
    - text based yaml-files
- allows to switch to sqlite
- fuzzy sets
    - assignment values or probabilites are possible for chronolology and typology by attaching "_0.5" for 50 % probability. 
    - multiple chronology and typology entries as well as multiple names (refering to one entity) are possbile.
- hierarchies
    - typology and chronology consider hierarchies. The whole string of superrior entities is included into the entry to enforce unambiguity and simplify filtering

## sDB

- The main-table(s) contain the main content of the database. The idea is to have similar basic fields and to use as few tables as possible. 
- The tables can have internal references and flexible hierarchies. A site can be a sub-entities of another sites and can have structures or artefacts as sub-categories. 
- With the core-information that is the same for all levels all information fit into one table and additional information can go into the keyvalue table. If there is important additional information (sword length in a sword-database) it makes sense to add this column into the sword table and hence not to mix swords and sites in one table. 
- Key-value contains all additional information. The value is always text and can be converted to numbers within the analysis. 
- All tables use UTF-8 encoding. 
- Do not use special characters (including space etc.) in type names, categories and column names. 
- Multiple terms can be separated with "," (for name, type, chron).

## sDB tables

:::: {.columns}
::: {.column width='50%'}
- main 
- kv (key-value)
- thes (ontology)
- chron
:::
::: {.column width='50%'}
![](../4figures/shkr_ER.svg)
:::
::::



## sDB tables: main

- main (in case of more than one main table the name can be modified, e. g. "main_sites", primary key
    - `id`, int|chr:     identification number (simple integer or uuid)
    - `id_source`, chr: catalogue number according to source
    - `id_sec`, int|chr: id of the superiour entity inside this table or in another main-table, usually foreign key
    - `name`, chr, mult:   entity name (combination of name elements, e.g. site, country)
    - `category`, chr: category, e.g. site
    - `type`, chr, mult, fuzzy:   entity type according to thes, probabilities can be attaches (e.g. "_0.5") 
    - `chron`, chr, mult, fuzzy:  chronology string according to https://gitlab.com/oliver.nakoinz/chronsys/-/blob/main/xxxxx.csv with probabilities attached  (e.g. "_0.5") 
    - `comment`, chr: any comments, German/English
    - `source`, chr, mult: particular source information, if citation is availabe in ref.bib, the bib-keys separated by comma are sufficiant
    - `location_q`, int: quality of localisation (according to thes)
        - 3: some m
        - 2: about 100 m
        - 1: about 1000 m
        - 0: unknown
    - `chron_q`, int: quality of chronological dating (according to thes)
        - 3: save dating with precision of few phases
        - 2: probable dating with precision of at least of epochs (e. g. Preroman Iron Age)
        - 1: plausible dating to broad epochs Metal Ages
        - 0: no chronological information
    - `info_q`, int: general quality of the information comprising chron_q, location_q and general quality of observations (according to thes)
        - 3: site exists and location_q and chron_q are 2 or better  
        - 2: site exists and location_q and chron_q are 1 or better
        - 1: site existence questionable or location_q or chron_q are 0 or
        - 0: site does not exist
    - `WKT`, chr:    coordinates WKT format, SRID=epsg:32632 (as example, in general projected coordinates systems are preferred) precision=site (see column location_q for specific information)
    
## sDB tables: kv

- kv (key-value)
    - `id`, int|chr:     identification number (simple integer or uuid), primary key
    - `tab`, char:       table name (one of the main tables) to which the entry belongs 
    - `id_sec`, int|char:  row to which the entry belongs, foreign key
    - `key`, char:         category of value (to be explained in the thes)
    - `value`, char:       value or attribute content
    - `comment`, char:     comment

## sDB tables: thes

- thes (ontology)
    - `id`, int|chr:     identification number (simple integer or uuid), primary key
    - `cat`, char:       category to which the term belongs (e. g. "settlement")
    - `order`, int:      relativ order of the entries inside the superior category
    - `code`, char:      code for this entry, used in other tables as reference, usually chain of terms or number-code (e.g. "sites>settlement>fortifiedSettlement")
    - `name`, char:      name of this individual entity (e.g. "fortifiedSettlement")
    - `chron`, chr, mult, fuzzy:  chronology string according to https://gitlab.com/oliver.nakoinz/chronsys/-/blob/main/xxxxx.csv with probabilities attached  (e.g. "_0.5") 
    - `source`, char:    source of definitions, citation or bib-key, with pages if available; including links to web semantics
    - `comment`, char:   

## sDB tables: chron

- chron
    - `c_system`: name of the chronology system
    - `id`: identification number inside the chronology system
    - `p_id`: id of the superior entity
    - `c_level`: hierarchy level starting with the most general entity
    - `c_order`: order inside one hierarchy level
    - `datstring`: chronology string (chronstring)
    - `name_short`: short name, must be identical with the last phase name of the chronology string, avoid tailing spaces
    - `name_long`: more comprehensive name of the phase
    - `start`: start year of the phase, negative means BC, same year as end year of the previous phase
    - `end`: end year of the phase


## sDB metadata

.yaml

## sDB references

.bib

# Workshop  {background-color="#9DB2CB"}

- Prepare data for publication
    - data
        - your own data, or
        - Holzmaar (simple), or
        - Schlei (advanced)
    - use *sDB* (simpleDatabase) template


##  ![](../4figures/icons/bib.svg) References


