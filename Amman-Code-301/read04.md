# CSS GRID

Grid layout is a very efficient and consistent way to layout your web pages. The grid system allows us to distribute our elements on the page however way we want. It is responsive to the screen size, and along with the flexbox, they will grant us the superpower of styling pages with more responsive features. 

## Terminology

1. **Grid Container** is the parent box that contains all the elements inside the grid. 
2. **Grid Element** it is any child element inside the grid container.
3. **Gridline**  the grid is divided into rows and columns with lines containing them inside. 
4. **Grid cell** any area inside the grid enclosed by four lines, two horizontal and two vertical.
5. **Grid area** can contain more than one cell.
6. **Grid track** any row or column that is formed by any two parallel lines.

## properties

### Parent container properties

Display: it takes one of two values; grid or inline-grid.
Grid-template-columns and Grid-template-rows: takes size units; px, fr, %. It forms the columns and the rows of the grid.
Grid-template-area: take line numbers, line names, or grid area names.
Grid-template: it is a shorthand for all grid template properties.
Column-gap and Row-gap: takes size unit that determines the gap between cells.
Gap: a shorthand for rwo-gap and column gap.
Justify-items: align items horizontally.
Align-items: to align items in the grid vertically.
Place-items: shorthand to align-items and justify-items.
Justify-content: to align the grid area along the horizontal axis.
Align-content: aligns the grid area along the vertical axis.
Place-content: shorthand for align-content and justify-content.
Grid-auto-column and Grid-auto-row: take a size unit to determine the size of the implicitly created grid areas.
Grid-auto-flow: takes one of three values: row, column, and dense.
Grid: a shorthand to set all of these properties: grid-template-rows, grid-template-columns, grid-template-areas, grid-auto-rows, grid-auto-columns, and grid-auto-flow.

### children elements properties

grid-column-start, grid-column-end, grid-row-start, grid-row-end: takes line numbers or names.
Grid-column, grid-row: shorthands for the above four properties.
Grid-area: takes a name value, could be any name. It takes line values as well.
Justify-self: align a single item on the horizontal axis.
Align-self: aligns single item on the vertical axis.
Place-self: a shorthand to align-self and justify-self.