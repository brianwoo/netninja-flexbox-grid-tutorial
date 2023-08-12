# Grid

- Set the parent container: display: grid

## Columns

- Define # of columns (on parent container): 
  - grid-template-columns: 33.3% 33.3% 33.3%
  - if more than 3 columns, other columns will be added below.
  - **Option**: Instead of using percentage, can use fraction (e.g. 1fr):
    - grid-template-columns: 1fr 1fr 1fr
    - all columns are the same width (i.e. same as using 33.3%)
  - **Option**: Using repeat:
    - grid-template-columns: repeat(3, 1fr)

## Rows

- Define row height  (on the parent container):
  - grid-auto-rows 200px
  - grid-auto-rows: minmax(150px, auto) ◄ min of 150px, but max is autofit
- Define # of rows (on parent container):
  - grid-template-rows 200px 300px 400px 200px  ◄ 4 rows
  - grid-template-rows: repeat(3, minmax(150px, auto))  ◄ 3 rows with minmax

## Gap
- Gap between columns:
  - grid-column-gap 10px
- Gap between rows:
  - grid-row-gap 10px
- Gap between rows + columns:
  - grid-gap 10px

## Grid Lines
- Define grid lines (on the child element)
- Grid lines are the lines between the rows and columns
- Grid lines starts from 1 (not 0 based)
  - Num of Grid lines = num of rows/columns + 1  ◄ because there are surrounding head and trail lines
- To tell where to place the element in the grid, we can use grid lines:
  - grid-column-start: 1;  ◄ grid column starts at grid line 1
  - grid-column-end: 3;    ◄ grid column ends at grid line 3
  - grid-column: 1 / 3;    ◄ grid column starts at 1, ends at 3
  - grid-row: 2 / 4;       ◄ grid row starts at 2, ends at 4
  - grid-row: 2;           ◄ grid row starts at 2 (if just 1 number)
  - grid-column: span 3;   ◄ grid column starts at 1, ends at 4 (span the width of 3 elements)

## Nested Grids
- Treat one of the grid element as a parent
