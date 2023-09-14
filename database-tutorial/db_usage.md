## Install and usage of a database
<section>
In this section you will learn how to **install** *SQLiteStudio*, **create** your first very own *database*, **add** some *tables* with different *columns*, **import** and **export** some data into them. These are some of the basics of using databases, after that you should be able to use it but there is still a lot to learn!

In our example we are using SQLite (https://www.sqlite.org/index.html) and the SQLiteStudio (https://sqlitestudio.pl/). You can download a version for your Linux, Mac or Windows system here (https://github.com/pawelsalawa/sqlitestudio/releases). There is a variety of software to manage databases (DBMS), but we chose this one because of it's very visual interface.
**Follow the instructions of the installer and open the client after you're done.**

### The SQLiteStudio interface
![Alt text](database-tutorial/db_images/ssdb_01.jpg)

</section>

### Creating a database, tables and columns
<section>

#### First step is to create a database file:

![Alt text](database-tutorial/db_images/ssdb_02.png) <!-- width="250px" align="right" -->

* click on **add a database**
* select SQLite 3
* create an .db3 file with a name and folder of your choice

#### Create tables for your data

* click on **create a table**
* add a name for your table
* click on **create a column**
* add a primary key (-> configure autoincrement)
* Now you can add columns that suite your data. If you already have a structure i.e. from a spreadsheet, you can use that for your db modelling. *Be careful about the datatypes, constraints and indexes before you finalize your database!*

![Alt text](database-tutorial/db_images/ssdb_03.png)

</section>

### Enter data into your database (manual and csv import)
<section>

#### Manual entry:

* Click under *data* on **Insert row**, click into fields and enter your data.
* You can also design a form under *Form view*.

![Alt text](database-tutorial/db_images/ssdb_04.png) <!-- width="700px" -->

#### Import/export csv:

![Alt text](database-tutorial/db_images/ssdb_05.png) <!-- width="300px" align="right" -->

* Click on **Import** and select your database and table.
* Select your data type, your .csv file and the encoding (UTF8 is best). Also you can select the data separator and check if your data has a header. Then you can click the finish-button and your data gets imported.
* The same way you can also export your data. Be sure to know your goals for further processing!

### Congratulations, you did it !!! ;-)
Now you know the basics of database usage. Have fun with your projects!!

#### Further reading (german):

* Alfons Kempler, André Eickler: Datenbanksysteme. Eine Einführung. Auflage 9, München 2013.
* Alice Zhao: SQL kurz & gut. 3. Auflage, Heidelberg 2022.

</section>