
<!--

title: "Publishing Data Online"
author: "Lizzie Scholtus"
footer: Research Data Management, 10-14 July 2023, Kiel
institute: Institut für Ur- und Frühgeschichte
language: en

comment:  Presentation for full day workshop "Introduction to Research Data Management" Summer School 2023, mixed target group (students, PhDs)


-->
# Publishing Data Online
**Lizzie Scholtus**  

Institut für Ur- und Frühgeschichte  

Research Data Management, 10-14 July 2023, Kiel

# Why publishing data?

## Why publishing data online?

<div style="float:left; width:50%;">

- To share data
  
  - Open Science
  
  - FAIR Principles

</div>

<div style="float:right; width:50%;">
![](publishing-data/image/why.png)
</div>

## Why publishing data online?

<div style="float:right; width=80;">
<img src="publishing-data/image/Open_Access.png">
</div>


<div style="float:left; width:60%;">

What is Open Science?

- Free access to:
  - Scientific publications
  - Research data and metadata
  - Hypothesis, methodologies, protocols, codes, formats and results
- Participative science

</div>

<div style="float:right; width:40%;">

![](publishing-data/image/Open_science.png)

<small>
*Pillars of the Open Science*  

*according to UNESCO's 2021 Open Science recommendation.*  

Source: [Wikipedia](https://en.wikipedia.org/wiki/Open_science)
</small>

</div>


## Why publishing data online?

::: {style="margin-top: -100px; margin-left: 900px"}
![](publishing-data/image/Open_Access.png){width=80}
:::

:::: {.columns}

::: {.column width="70%"}

What is Open Science?

- An organised community of various disciplines with convergent practices  
[Manifeste des Digital Humanities](https://books.openedition.org/oep/235)
- A government strategy

:::

::: {.column width="30%"}

![](publishing-data/image/plan_national.png)

<small>
*French national plan for Open Science*  
Source: [French Ministry of Higher Education and Research](https://www.enseignementsup-recherche.gouv.fr/fr/le-plan-national-pour-la-science-ouverte-2021-2024-vers-une-generalisation-de-la-science-ouverte-en-48525)
</small>

:::

::::

::: {.notes}

Idea since the start of 2010 and influence research globaly
Questions that are now integreted in government research strategies (in France at least)
  National plan for Open Science and Law for a numeric republic
  numerical data management, spreading and reproducibility

:::


## Why publishing data online?


What are FAIR principles?

![](publishing-data/image/FAIR.png)



::: {.notes}
= a way of constructing, storing, presenting and publishing data in such a way as to make it more easily accessible, understood, exchangeable and reusable by the community.
Introduced in 2014 in response to a growing desire to publish open data and to make the most of big data.

- Easy to find >> file described by metadata (description of file content, authors, dates, etc.) and associated with a unique identifier to make it easy to find (DOI, HAL).

- Accessible >> long-term storage of data and easy access to it 
access to metadata through open and standard protocols + access to data through clear licences (not necessarily open or free)

- Interoperable >> data can communicate with each other = various types and formats of data can be cross-referenced 
give priority to open and widely shared languages and formats + permanent identifiers + alignment with repositories

- Reusable >> must be facilitated by the use of common standards + clear, verified and well-described data >> directly reusable
+ clear and accessible user licence (not necessarily free).

:::

## Why publishing data online?

:::: {.columns}

::: {.column width="50%"}


- To share data
  - Open Science
  - FAIR Principles
  
::: {.incremental}
- To save data
  - Digital data can die
    - Accident
    - Software evolution
  - Version control
  
:::

:::

::: {.column width="50%"}
![](publishing-data/image/why.png)
:::

::::

::: {.notes}
- saving data: digital data can die and we have to multiply the number of backup media
  - Who never lost data? Or was afraid of loosing his computer?
  - Software evolution can also be a problem
    - What happens to the data from your previous research project? Do you open them every year to make sure they are still readable?
    - What about archives?
- Online platforms often offer several extremely useful backup functions
  - versioning
  - cloud
  - software evolution
  - severs
This doesn't mean that you don't need anymore internal back up, but online plateforms offer security
:::

# Where to publish data? {background-color="black" background-image="publishing-data/image/web.jpg" background-size="contain"}

## Where to publish data? {.smaller}

![](publishing-data/image/not_equal.png){.absolute top=230 left=420 width="100" height="100"}

:::: {.columns}

::: {.column width="50%"}
  
::: {.fragment fragment-index=1}
::: {.fragment .semi-fade-out fragment-index=2}
- Institutional
  - EU, Country, University
:::
:::

::: {.fragment fragment-index=2}
::: {.fragment .semi-fade-out fragment-index=3}
- non-specialist
:::
:::

::: {.fragment fragment-index=3}
::: {.fragment .semi-fade-out fragment-index=4}
- To deposit the data as it is
  - Private (personal or institutional cloud)
  - Public ([Zenodo](https://zenodo.org/), [Nakala](https://nakala.fr/), [HAL](https://hal.science/), [opendata@uni-keil](https://opendata.uni-kiel.de/content/index.xml)...)
  - Both ([Gitlab](https://about.gitlab.com/), [Github](https://github.com/))
:::
:::

:::

::: {.column width="50%"}

::: {.fragment fragment-index=1}
::: {.fragment .semi-fade-out fragment-index=2}
- Private
  - Free or not
:::
:::

::: {.fragment fragment-index=2}
::: {.fragment .semi-fade-out fragment-index=3}
- Field specialised
:::
:::

::: {.fragment fragment-index=3}
::: {.fragment .semi-fade-out fragment-index=4}
- To share the data with other datasets
  - ([Ariadne](https://portal.ariadne-infrastructure.eu/), [ArkeoGIS](https://arkeogis.org/), Landman...)
:::
:::

:::
::::

:::{.r-stack}
::: {.fragment fragment-index=4}
- To create your database ([Heurist](https://heurist.huma-num.fr/heurist/startup/))
:::
:::



::: {.notes}
There are lots of online platforms that allow to publish, deposit or share data. They can be from different categories, at different scales and for different usage
:::

## Where to publish data?

. . .

```{r}
#| echo: false

library(DiagrammeR)

grViz("
  digraph {

    node[shape = box, fontname = Helvetica, style = filled, width = 1.5]
    A1[label = 'My research is', fillcolor = 'DarkSalmon'] 
    A2[label = 'I want to', fillcolor = 'DarkSalmon'] 
    A3[label = 'My data is', fillcolor = 'DarkSalmon']
    A4[label = 'I need specific element', fillcolor = 'DarkSalmon']
    A5[label = 'My research is institutional', fillcolor = 'DarkSalmon']
    
    node[shape = circle, fixedsize = true, width = 1]
    B11 [label = 'On going', fillcolor = 'LightSteelBlue'] 
    B12 [label = 'Finish', fillcolor = 'LightSteelBlue']
    
    B21 [label = 'Create\ndata', fillcolor = 'LightSteelBlue']
    B22 [label = 'Save\ndata', fillcolor = 'LightSteelBlue']
    B23 [label = 'Share\ndata', fillcolor = 'LightSteelBlue']
    
    B31 [label = 'Code', fillcolor = 'LightSteelBlue']
    B32 [label = 'Database', fillcolor = 'LightSteelBlue']
    B321 [label = 'Spatial?', fillcolor = 'LightBlue']
    B33 [label = 'Pictures', fillcolor = 'LightSteelBlue']
    B34 [label = 'Results', fillcolor = 'LightSteelBlue']
    
    B41 [label = 'DOI', fillcolor = 'LightSteelBlue']
    B42 [label = 'Version\ncontrol', fillcolor = 'LightSteelBlue']
    
    B51[label = 'Yes', fillcolor = 'LightSteelBlue']
    B511[label = 'There is\n a DPM', fillcolor = 'LightBlue']
    B5111[label = 'Yes', fillcolor = 'LightSteelBlue']
    B5112[label = 'No', fillcolor = 'MistyRose']
    B51111[label = 'I have\nacces to', fillcolor = 'LightBlue']
    B511111[label = 'Institutional\nplatform', fillcolor = 'DarkSeaGreen', width = 1.2]
    B511112[label = 'specialised\nplatform', fillcolor = 'DarkSeaGreen', width = 1.2]
    B52[label = 'No', fillcolor = 'Grey']
    
    A1 -> {B11 B12}
    A2 -> {B21 B22 B23}
    A3 -> {B31 B32 B33 B34} B32 -> B321
    A4 -> {B41 B42}
    A5 -> {B51 B52} B51 -> B511 -> {B5111 B5112} B5112 -> B51111 -> {B511111 B511112}
  }")
```


::: {.notes}
Each platform has its own benefits and inconvenience
- private deposits may be the most simple to use but usually offer the less possibilities (freely)
- deposit in common databases are the most inconvenient in terms of work load > need to adapt the data to their own conceptual model > but they are the ones that all the most diffusion of data
- It is useful to know some of them even without using them
  - to look for data or information
  - to prepare your data in advance
:::

# Three platforms, Three uses {background-color="white" background-image="publishing-data/image/platform2.jpg" .reveal}

```{css}
#reveal {
  position:fixed;
  top: 0px;
}
```

## Git Platforms {background-color="White" background-image="publishing-data/image/github-vs-gitlab.jpg" background-size="contain"}
::: {.fragment .fade-in}
::: {.fragment .fade-out}
![](publishing-data/image/git.jpg)
:::
:::

::: {.notes}
- Platform Git = based on GIT
 - version control system, open source
 - Allows working on different version of the same project and put them together again
 - But only locally
 
- Platforms = cloud based solutions
:::

## Git Platforms {.smaller}

::: {.columns}

::: {.column width="50%"}

[![](publishing-data/image/github.png){width=75}](https://github.com/)

::: {.fragment .fade-in}
- Oldest (2008)
- More people
- Bought by Microsoft
- Less ready to use
  - Users need to pay to integrate elements themselves from third-party application

:::

:::

::: {.column width="50%"}

[![](publishing-data/image/gitlab.png){width=60}](https://gitlab.com/)

::: {.fragment .fade-in}
- Open source
- Completely free at the beginning (not any more)
- continuous integration and DevOps workflows
- Need a paid account for some functionalities

:::

:::

::::



::: {.notes}
- pretty similar
  - For both the idea is to share code
  - For both most basic function accessible
  - BUT still some differences
- continuous integration = for task automation and code deployment
 
:::

## Gitlab {auto-animate=true}


::: {style="margin-left: 400px; margin_top: 100px"}
![](publishing-data/image/gitlab.png){width=300}
:::

## [Gitlab](https://gitlab.com/) {auto-animate=true .smaller}

::: {style="margin-top: -100px; margin-left: 700px"}
![](publishing-data/image/gitlab.png){width=60}
:::


:::: {.columns}

::: {.column width="50%"}

**Description**

- Dedicated to versioning
- Collaborative work
- Code development

::: {.fragment fragment-index=1}

::: {style="color: Chocolate;"}
**Inconvenients**
:::

- works with command lines
- Only a depot, not a real publication

:::

:::

::: {.column width="50%"}

::: {.fragment fragment-index=2 .absolute top="40%"}

::: {style="color: Chocolate;"}
**Advantages**
:::

- Branch system
- Continuous integration
  - Standalone [pages](https://lscholtus.gitlab.io/arkeogis-tutoriels/Alignment.html)
  - [Website](https://lscholtus.gitlab.io/mosaicdata/)
- Deposit can be private or public
- Licence attribution
- institutional instance exist
  
:::

:::

::::

::: {.notes}
- Description: more for code deposition but can be with data
- Inconvenient
  - not easy to use > Git
  - Exist with software but need to be learned
  - not a real publication > not citation, no DOI
- Advantages
  - Branch > allows every author and collegue to work on its part and then merge it to the whole project
  - Standalone pages > allows creation of html pages > easy diffusion with no obligation  
        > website
:::

##  {auto-animate=true}

::: {style="margin-left: 400px; margin_top: 100px"}

![](publishing-data/image/Zenodo_logo.jpg){width=300}

:::

## [Zenodo](https://zenodo.org/) {auto-animate=true .smaller}

::: {style="margin-top: -100px; margin-left: 700px"}
![](publishing-data/image/Zenodo_logo.jpg){width=150}
:::


:::: {.columns}

::: {.column width="50%"}

**Description**

- Dedicated to dataset deposit
- Code can also be deposit
- Created By CERN

::: {.fragment fragment-index=1}

::: {style="color: Chocolate;"}
**Inconvenients**
:::

- Not possible to modify a file
- Fix deposit as for a publication

:::

:::

::: {.column width="50%"}

::: {.fragment fragment-index=2 .absolute top="40%"}

::: {style="color: Chocolate;"}
**Advantages**
:::

- DOI (Digital object identifier)
- Enables easy citation
- Various metadata
- Version control
- Deposit can be private or public
- Licence attribution
  
:::

:::

::::

::: {.notes}
- Description: 
  - Created by CERN to follow the Open Science recommandation
    - It is institutionnal > maintained by CERN and EU
- Inconvenient:
  - Not possible to just modify a file, it needs to be supress and reupload
  - the deposit is fixed, as it is for a publication
- Advantage:
  - Gives a DOI to new publication (if there is already one you can just link it)
  - Various metadata: can document precisely the data and the project and link it to every other publication
:::

##  {auto-animate=true}

::: {style="margin-left: 250px; margin_top: 50%"}

![](publishing-data/image/ArkeoGIS.png){width=500}

:::

## [ArkeoGIS](https://arkeogis.org/) {auto-animate=true .smaller}

::: {style="margin-top: -100px; margin-left: 700px"}
![](publishing-data/image/ArkeoGIS.png){width=150}
:::


:::: {.columns}

::: {.column width="50%"}

**Description**

- Geographical informatic system online
- specific to data of the past
- Created by Strasbourg university

::: {.fragment fragment-index=1}

::: {style="color: Chocolate;"}
**Inconvenients**
:::

- Support only spatial data
- Only datasets
- Data need to be aligned to ArkeoGIS structure

:::

:::

::: {.column width="50%"}

::: {.fragment fragment-index=2 .absolute top="40%"}

::: {style="color: Chocolate;"}
**Advantages**
:::

- Data link with other datasets
- Automatic language alignement
- Automatic chronological alignement
- LOD (Link Open Data)
- DOI
  
:::

:::

::::

::: {.notes}

:::


## [ArkeoGIS](https://arkeogis.org/) {.smaller}

::: {style="margin-top: -100px; margin-left: 700px"}
![](publishing-data/image/ArkeoGIS.png){width=150}
:::

::: {style="margin-top: -30px; margin-left: 700px"}
![](publishing-data/image/arkeopen.svg){width=150}
:::


:::: {.columns}

::: {.column width="50%"}

**Description**

- Geographical informatic system online
- specific to data of the past
- Created by Strasbourg university



::: {style="color: Chocolate;"}
**Inconvenients**
:::

- Support only spatial data
- Only datasets
- Data need to be aligned to ArkeoGIS structure



:::

::: {.column width="50%"}

::: {.absolute top="40%"}

::: {style="color: Chocolate;"}
**Advantages**
:::

- Data link with other datasets
- Automatic language alignement
- Automatic chronological alignement
- LOD (Link Open Data)
- DOI
- Data under password login or completly [open](https://arkeopen.org)
  
:::

:::

::::

::: {.notes}

:::

# What is LOD? {background-color="black" background-image="publishing-data/image/web2.jpeg" background-size="contain" .reveal}

## What is LOD? (Link Open Data) {.smaller}

:::: {.columns}

::: {.column width="50%"}

- Linking online data together using:
  - Semantic web
  - Uniform Resource Identifier (URI)
  - Detailed metadata
  - Resource Description Framework (RDF)

:::

::: {.column width="50%"}


![](publishing-data/image/LOD.jpg)


:::

::::

::: {.notes}
- WEB3.0 = instead of having isolated data repositories, linking them to create a global network. The link is build through internet (data must be online), using:
  - semantic web
  - URI
  - Metadata
  - Resource Description Framework (RDF) = model to describe online data using subject-predicate-object form
:::

## What is Semantic Web? {.smaller}

::: {style="margin-top: -100px; margin-left: 700px"}
![](publishing-data/image/semantic.png){width=150}
:::

:::: {.columns}

::: {.column width="50%"}

- Structure and link information online

::: {.fragment fragment-index=1}
  - Using ontologies to build conceptual data modelling
:::

::: {.fragment fragment-index=2}
  - Using normalised vocabularies
    - [Getty AAT](https://www.getty.edu/research/tools/vocabularies/aat/) for patrimonial data
    - [PACTOLS](https://pactols.frantiq.fr/opentheso/) for patrimonial data
    - [GeoNames](http://www.geonames.org/) for places
    - [Periodo](https://client.perio.do/?page=open-backend) for chronologies
    - [VIAF](https://viaf.org/) for people
:::

::: {.fragment fragment-index=3}
- Enables data browsing

:::

:::

::: {.column width="50%"}

::: {.fragment fragment-index=1}

::: {.fragment fragment-index=2 .fade-out}

![](publishing-data/image/CIDOC.png)
*Conceptual model based on [CIDOC CRM](https://cidoc-crm.org/) ontology*

:::

:::

::: {.fragment fragment-index=2}

::: {.fragment fragment-index=3 .fade-out}

::: {.absolute top="30%"}

  ![](publishing-data/image/thesaurus.png)
:::

:::

:::

::: {.fragment fragment-index=3}

::: {.absolute top="30%"}

  [![](publishing-data/image/ariadne.png)](https://portal.ariadne-infrastructure.eu/search?q=fibula)
  
  [A new platform for humanities](https://gotriple.eu/fr)
:::

:::

:::

::::

::: {.notes}
- Ontologies to allow communication between each database
  - link database variables to concept
- Structure vocabularies = thesaurus
  - various online allowing to link data to specific terms
  - generaly multilingual > link different languages database together
  - A same word can be written in different ways, with the link to a thesaurus it will always refer to a specific term
  
- All of this is how the whole web is constructed and it is how we can use browsers to look for webpages
:::

# What does this mean for you? {background-image="publishing-data/image/Uncle_Sam.png" background-size="50%" .reveal}

## What does this mean to you? {.smaller}

:::: {.columns}

::: {.column width="60%"}
- The first step is to structure your data
- Always precise your data with metadata
- If possible use free format
- Place your data in permanent backup structures (institutional or not) >> DMP
- Specify licences and where possible use the most open ones

:::

::: {.column width="40%"}

![](publishing-data/image/FAIR_small.jpg)  

::: {.absolute bottom="30%"}

![](publishing-data/image/licence.jpg)

:::

:::

::::

::: {.notes}
To integrate best practice standards, you don't have to respect them all! It is possible to apply only some of them initially = habits to have when creating data:

- Structure the data >> avoid text fields wherever possible and use controlled fields in databases.
- link metadata to your dataset (even a simple txt file next to the database work)
- as far as possible, use free formats >> ensure data longevity (it will still be possible to access it in 10 years' time)
- place your data in permanent backup structures (institutional or not) >> not just on your computer and then you forget that the data exists >> In connection with the DMP
- specify licences and if possible leave them open (open does not mean necessary free)
:::

# The French Data Management Environment

## A government strategy


:::: {.columns}

::: {.column width="50%"}

- National plan for Open Science
- Law for a numerical Republic
- Aim:
  - Research Data Management on a national level
  - Dissemination and reproducibility

:::

::: {.column width="40%"}

![](publishing-data/image/cnrs.png){width=80}

::: {.absolute bottom="20%"}

![](publishing-data/image/ESR.png){width=150}

:::

:::

::::

## {background-image="publishing-data/image/Huma-Num.png" background-size="contain"}

::: {.notes}

This government strategy is reflected in the French research landscape through the Huma-Num infrastructure
- Mission = to create a digital infrastructure enabling Humanities communities to develop, implement and preserve research programmes - and their data and tools - over the long term, in a context of open science and data sharing. 
- but put in place practices and tools for Humanities communities
- in accordance with the FAIR principles

:::

## {background-image="publishing-data/image/masa.png" background-size="contain"}

::: {.notes}

Huma-Num is organised into consortia to support each discipline.
Since 2013, the MASA (Mémoire des Archéologues et des Sites Archéologiques) consortium has been helping archaeologists to digitise and make available their excavation archives.
- is working to disseminate the precepts of the FAIR principles within the French archaeological community.
The aim is to help archaeologists make their data interoperable and open up their datasets on the web, while ensuring that they are safeguarded.

:::

## {background-image="publishing-data/image/masa2.png" background-size="contain"}


::: {.notes}

The MASA digital ecosystem is designed to help archaeologists.
It is based on the famous data life cycle.
The aim is to identify existing tools (or, if they are lacking, to put them in place) and to provide best practices to make the task easier for researchers, from the data acquisition phase through to reuse.

It follows the same steps as those defined by Huma-Num, but with specific tools for archaeologists.

These best practices are structured around the FAIR (Easy to Find...) principles.

:::