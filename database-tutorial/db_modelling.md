
## Modelling Databases


Before we move to the technical part on how to use SQLite Studio, we should discuss on how databases work and structure their data. 

We will be using a simple running example to explain the different concepts. Here we have two tables. One for Graves, the other ones for artifacts found within these graves. 
As you can see, grave 4 is a very rich grave.
Obviously, you would usually have far more information, but for our purposes, we will stick with these values.

| Grave | Width | Form |
| -------------------- |:-------------:| -----:|
|1|90| rectangle|
|2|110| rectangle|
|3|100| square|
|4|148| rectangle|

| Artifact | Type | in_Grave |
| -------------------- |:-------------:| -----:|
|1| ring | 1|
|2| microlith | 2|
|3|ring | 4|
|4|bracelet| 4|
|5|earring| 4|
|6|pendant| 4|

## Basic Concepts
(attribute + tupel?)

In order to understand databases, there are a few things that you should have heard about.

1. Relational Datamodel

There are many different ways on how to build databases, but the most popular approach is the  relational one.

In this approach, everything is based on tables. You can think of a database as many different spreadsheets that get interlinked through so-called ***keys***. Someting that doesn´t exist in usual tables are ***constraints***, which ...

The structure of the database is defined by a ***schema***. It´s really not much more than the header you have in a regular table. For example, in our table for Graves, we have the number of the Grave, the width and the form. This is the schema of that table. 



For each column in your schema, you determine the ***datatype*** that the values in the column should have. 
For instance, the Width of the Graves will only need to have number values, whereas the Form will take text input. We give an overview of available datatypes below.


When creating a database, there are certain steps to follow:

1. Define your schema - How many tables do you need? 
2. Define the datatypes for each column - What values are permitted, which are forbidden?
3. Determine the relations between your tables - How can you interlink them?

2. Schema and Datatypes

- Integer (float)
- Text (varchar)
- Real 
- Numeric
- Blob




1. Primary Key
2. Foreign Key
3. Constraints

