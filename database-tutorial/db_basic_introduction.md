## Introduction for better work with archaeological data

In archaeological science you are often confronted with data. Data are connected information who describes in the specific subject of archaeology e. g. sites, features, finds and all behaviours of human culture.

If you have to work with data you have to decide how you get, maintain and use it for research. That includes the decision for usable digital environment to make it possible to manage data.

But before you are going into collect your data there some important tasks to care for. You need to know your reason for the project you work on. The reason is your starting point and gives you orientation in the process of planning your data project.

The planning of your data have to keep different phases of your project. Besides the phases of acquire the information and processing for visualising for example you have to keep in mind what will happen after you have finished your work with your data. It exist the concept of a lifecycle of data. So you have to keep in mind collecting, analysing, archiving and publishing data. The DFG (Deutsche Forschungsgemeinschaft) has published four principles what research data should provide if you want to publish your data and providing for re-use. It is called *FAIR principles*. 
- **F**indable means you add metadata as much as you can to your data so they are findable through search engines. 
- **A**ccessable which means you take care that you ensure your data doesn't will be delete and is everytime accessible for your target audience. An example is redundant publishing with crossreferencing. 
- **I**nteropoerable means you take care that your data can used in different research environments. Important is to support different common platforms independant of the development in IT. 
- **R**e-usable means your data should be in a format that everyone can use it in projects after you have published your including yourself.

The choice depends on the kind of data, how they are structured and how extensive they are. Most common structure in archaeology is a list of sites, features and finds with specific attributes for each observation.

The best format for a small amount is a simple *csv*-file (comma-separated values). Each line in this file represents one dataset where each column is separated by a comma or semicolon. The structure is very easy to understand, reusable and to share. You are mostly free in your choice of the operating system, distribution and software solution.

With rising complexity of the data and relations between these datasets sometimes it is useful to change the management system of your data. In these cases for example you can choose a management system for relational databases like *PostgreSQL* or [*SQLite*]{##Installation and usage of a database}