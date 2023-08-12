# NetNinja's CSS Flexbox Tutorial
https://www.youtube.com/playlist?list=PL4cUxeGkcC9i3FXJSUfmsNOx8E7u6UuhG


# Flexbox

- Set the parent container: display: flex
  - Every child item then becomes a Flex element
  - Flex stacks child items horizontally by default
  - When flex direction is row:
    - align-items controls vertical alignment (cross axis)
    - justify-content controls horizontal alignment (main axis)
    - align-content controls multiple lines (e.g. when wrapped)

## Flex-grow

- flex-grow is used on a Flex element
- flex-grow: [growth rate]
- flex-grow can be used as a grid system
  - E.g. Like a 12 column system:
    1. Box 1: flex-grow: 4;
    1. Box 2: flex-grow: 6;
    1. Box 3: flex-grow: 2;
  
  -
  - This is the same as:
    1. Box 1: flex-grow: 2;
    1. Box 2: flex-grow: 3;
    1. Box 3: flex-grow: 1;

## Flex-shrink

- flex-shrink is used on a Flex element
- flex-shrink: [shrink rate]
- NOT a popular property

## Flex-wrap

- flex-wrap is used on the parent container
  - flex-wrap: wrap;
  - flex-wrap: wrap-reverse;
  - flex-wrap: nowrap;

## Flex-basis

- flex-basis is used on a Flex element
- Similar to the min-width property (when flex-direction: row, in other words, main axis)
  - diff is that min-width will display the scrollbar when the window's width is smaller than the min-width.
  - flex-basis will shrink the flex elements even the window's width is smaller than the flex-basis value.

## Order
- order is used on a Flex element
- lowest number goes first, highest number goes last

## Gap
- gap is used on the parent container
  - gap [row-and-column-gap]
  - gap [row-gap] [column-gap]
  - gap: 10px 15%;  <-- row gap 10px, column gap 15%
  - Add gap between each Flex element


## Flex-flow (flex-direction + flex-wrap)
- flex-flow is used on the parent container
  - flex-flow: row (default)
  - flex-flow: column
  - flex-flow: row-reverse
  - flex-flow: column-reverse
- When flex-flow is set to column:
  - align-items controls horizontal alignment (cross axis)
  - justify-content controls vertical alignment (main axis)
  - flex-basis is appied to the min-height

## Flex (flex-grow + flex-shrink + flex-basis)

- flex is used on a Flex element
- A combination of flex-grow, flex-shrink and flex-basis
  - flex: [flex-grow value] [flex-shrink value] [flex-basis value]
  - E.g. flex 1 0 200px;
  - E.g. flex 1; <-- means flex-grow: 1, flex-shrink: 1, flex-basis: 0px