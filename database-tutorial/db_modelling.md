
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

<section>

(attribute + tupel?)

In order to understand databases, there are a few things that you should have heard about.






### Relational Datamodel


There are many different ways on how to build databases, but the most popular approach is the relational one.

In this, everything is based on tables. You can think of a database as many different spreadsheets that get interlinked through so-called ***keys***. Something that doesn´t exist in usual tables are ***constraints***, which allow for further specifications on the values in the constrained column. 

The structure of the database is defined by a ***schema***. It´s really not much more than the header you have in a regular table. For example, in our table for Graves, we have the number of the Grave, the width and the form. This is the schema of that table. 

For each column in your schema, you determine the ***datatype*** that the values in the column should have. 
For instance, the Width of the Graves will only need to have number values, whereas the Form will take text input. We give an overview of available datatypes below.

</section>
### Keys

There are two different kind of keys: **Primary and Foreign Keys**.

Primary Key:

In a database, you can´t have duplicates. To ensure the uniqueness of each line, you need to define a Primary Key. It serves as a distinct identifier for this specific line. 
In our case, it makes sense to take the grave number as our ID. Similarly, the artefact number will be the primary key for the artefact table.

Foreign Key:

A foreign key references the primary key of another table. 
For example, the artefact table has a column in_grave, which shows us to what grave the artefact belongs to. As you can see, in_grave uses the value of grave_number, the primary key of the Grave table. By that, we can match the artefact with the specific grave. All the information is linked together but it is stored in a way that is easier for us to overview. This is one of the big advantages of using databases.

You can define a column to be a foreign or primary key (or both), when creating the column


### Datatypes

There are many different datatypes. We will stick with the most common ones here, but also stick to SQLite Studio´s standard types.

- Integer 
Integer is a type that is used for numbers, that do not contain any comma. 
Numbers like 15, 900, -6, -17 are all accepted for that datatype, but not something like 5.3 or 2/3.

- Real & Numeric
These datatypes serve for all types of numerical data. In particular, you can also use comma values for that.
The difference between the two types is linked to the way that they are stored in the computer. Numeric stores the exact, precise representation, whereas Real stores an approximation of the value. For most cases in archaeology, you mustn´t concern yourself too much with these. You may choose what feels more comfortable to you.


- Text 
For text SQLite Studio has the very simple Datatype Text. You can write any and all kinds of symbols in that type. However, note that special characters like the german "ä" might end up being misintepreted. It´s usually best to avoid these. If you can´t, make sure to inform yourself about the correct format to use. UTF-8 is recommendable.

In most other database programs, the datatype to use for text is Varchar. So, if you ever end up using a different program, this is the type to use.


- Blob
In most cases, we only have Text or Numerical Data, so Blob is rarely ever used. You would use Blob for large data like audio and video files.


### Constraints

Other than defining primary and foreign keys, you can also determine certain other conditions that the values in a column have to meet.

- NOT NULL: With this, it is not allowed to leave this column empty.

- UNIQUE: 
This means, that the value in the column each must be unique. For instance, a primary key is also automatically unique.

- CHECK:
With this you can define your own rules, which the specific column has to meet. For basic use, you must not worry about this. 



## Creating a database concept

When creating a database, there are certain steps to follow:

1. Define your schema - How many tables do you need? 
2. Define the datatypes for each column - What values are permitted, which are forbidden?
3. Determine the relations between your tables - How can you interlink them?











