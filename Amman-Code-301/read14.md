# DATABASE NORMALIZATION

Normalizing a database is a process where we optimize databases and organize them into tables where each table serves only one purpose. It helps eliminate issues that happen when tables built to serve more than one goal and contain more information about different topics. This issue may arise as a reason to duplicate data when we try to modify or search for data. Normalization is a set of rules that we can follow one by one, and as we move to successive rules, we will increasingly notice the performance improvement. 

## Reasons to normalize a database

* Decrease the amount of duplicate data
* Simplify queries
* Avoid modification issues

## Data Duplication and Modification Anomalies

Duplicate data increases the amount of consumed storage and makes modifications more difficult. Below, there is a list of the most common anomalies that happen as a result of this:

* Insert Anomaly: we can't insert unless we know more information than we already have
* Update Anomaly: if we want to modify a fact for all records, we have to go through all the records once at a time to modify them, which is painful
* Deletion Anomaly:  deleting a row involves not only deletion of the data we want but also the deletion of other data that might be important

## Search and Sort Issues

These issues appear when we try to query data with the same type but spread out to multiple columns. If we, instead, have the data in a separate column, we would query this column easier and simpler.

## Forms of database normalization

There are three sets of rules to normalization that follow one another. We can't achieve one unless we apply the previous ones:

* First Normal Form – The information is stored in a relational table with each column containing atomic values. There are no repeating groups of columns.
* Second Normal Form – The table is in the first normal form, and all the columns depend on the table’s primary key.
* Third Normal Form – the table is in second normal form, and all of its columns are not transitively dependent on the primary key