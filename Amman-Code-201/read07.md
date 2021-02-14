# Object-Oriented Programming, HTML Tables

## Domain Modeling

Domain modeling is the process of creating a conceptual model in code for a specific problem. A model describes the various entities, their attributes and behaviors, as well as the constraints that govern the problem domain. An entity that stores data in properties and encapsulates behaviors in methods is commonly referred to as an object-oriented model.

A domain model that's articulated well can verify and validate the understanding of a specific problem among various stakeholders. As a communication tool, it defines a vocabulary that can be used within and between both technical and business teams.

When building your own domain models:

1. When modeling a single entity that'll have many instances, build self-contained objects with the same attributes and behaviors.
2. Model its attributes with a constructor function that defines and initializes properties.
3. Model its behaviors with small methods that focus on doing one job well.
4. Create instances using the new keyword followed by a call to a constructor function.
5. Store the newly created object in a variable so you can access its properties and methods from outside.
6. Use the this variable within methods so you can access the object's properties and methods from inside.

## HTML Tables

A table is a representaion of date in a grid format. Using tables to display certain types of data make it easier for the reader to understand the data since it is shown in a two axes grid. Each block of content in the tables is called a cell, and data is added to the table in form of rows of cells.

### Creating tables

We create tables using the \<table> tag. We the add rows using the \<tr> tag and inside each row we add a collection of table cells using the table data tags \<td>.

```html
<table>
<tr>
<td>15</td>
<td>15</td>
<td>30</td>
</tr>
<tr>
<td>45</td>
<td>60</td>
<td>45</td>
</tr>
</table>

```

We can also specify table heads using the \<th> tags, which can be added to make either rows or column heads. To determine that a table head represents a row or a column we can use the `scope` attribute with two values: col , row. If there is any empty cells we still need to add an empty table head to indicate the presence of that empty cell, otherwise the table will not be rendered correctly.

```html

<table>
<tr>
<th></th>
<th scope="col">Saturday</th>
<th scope="col">Sunday</th>
</tr>
<tr>
<th scope="row">Tickets sold:</th>
<td>120</td>
<td>135</td>
</tr>
<tr>
<th scope="row">Total sales:</th>
<td>$600</td>
<td>$675</td>
</tr>
</table>

```

Sometimes you may need the entries in a table to stretch across more than one column. The colspan attribute can be used on a \<th> or \<td> element and indicates how many columns that cell should run across.

```html

<table>
<tr>
<th></th>
<th>9am</th>
<th>10am</th>
<th>11am</th>
<th>12am</th>
</tr>
<tr>
<th>Monday</th>
<td colspan="2">Geography</td>
<td>Math</td>
<td>Art</td>
</tr>
<tr>
<th>Tuesday</th>
<td colspan="3">Gym</td>
<td>Home Ec</td>
</tr>
</table>

```

You may also need entries in a table to stretch down across more than one row. The rowspan attribute can be used on a \<th> or \<td> element to indicate how many rows a cell should span down the table.

```html

<table>
<tr>
<th></th>
<th>ABC</th>
<th>BBC</th>
<th>CNN</th>
</tr>
<tr>
<th>6pm - 7pm</th>
<td rowspan="2">Movie</td>
<td>Comedy</td>
<td>News</td>
</tr>
<tr>
<th>7pm - 8pm</th>
<td>Sport</td>
<td>Current Affairs</td>
</tr>
</table>

```

You can also add more semantic features to a table using these three tags:

1. \<thead>: for table headers.
2. \<tvody>: for the tables main data contnets
3. \<tfoot>: for table footers.

The reason for having these sematics in our code is because sometimes we have tall tables with huge amount of contents and you want to keep tracking the table headers and footers, so using these tags you can add some unique styling and sticky fratures to the table head and foot.

```html

<table>
<thead>
<tr>
<th>Date</th>
<th>Income</th>
<th>Expenditure</th>
</tr>
</thead>
<tbody>
<tr>
<th>1st January</th>
<td>250</td>
<td>36</td>
</tr>
<tr>
<th>2nd January</th>
<td>285</td>
<td>48</td>
</tr>
<!-- additional rows as above -->
<tr>
<th>31st January</th>
<td>129</td>
<td>64</td>
</tr>
</tbody>
<tfoot>
<tr>
<td></td>
<td>7824</td>
<td>1241</td>
</tr>
</tfoot>
</table>

```

### Some outdated attributes that is replaced using CSS:

1. width : to indicate how wide that table should be. It can be used on table ot cells
2. cellspacing: to add space inside each cell of the table
3. cellpadding: to create space between each cell of the table
4. border: to indicate the width of the border in pixels, and it can be used with the table or the cells
5. bgcolor: to indicate background colors of either the entire table or individual table cells