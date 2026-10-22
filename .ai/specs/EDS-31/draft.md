---
item_type: Story
item_id: EDS-31
summary: Cards block skips empty authored cells
labels: [cards]
---

## Description

The cards block at blocks/cards/ turns every authored cell into a card section, including cells
the author left empty. An empty cell becomes an empty cards-card-body element inside the card.
Change blocks/cards/cards.js so that a cell with no content produces no element in the decorated
block. Authors routinely omit cells, and the block should tolerate that without leaving empty
sections behind.

## Acceptance criteria

AC-1 An authored card cell with no child elements and no text renders no element in the decorated block.
AC-2 An authored card cell containing only whitespace renders no element in the decorated block.
AC-3 An authored row whose cells are all empty renders no list item in the decorated block.
AC-4 A cell holding a single picture still renders with the class cards-card-image.
AC-5 A cell holding text still renders with the class cards-card-body.
AC-6 A page containing the cards block loads with no new console errors.

## Out of scope

Any change to blocks/cards/cards.css, to any other block, or to authored content.
