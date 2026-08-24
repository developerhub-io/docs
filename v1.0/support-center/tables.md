---
type: page
title: Tables
listed: true
description: 
index_title: Tables
hidden: false
keywords: 
tags: blocks
---

%product% tables consist of a header row and data rows.

To create a table:

{% synced id="open-block-menu" /%}

- Select Table {% icon classes="fas fa-table" /%}

### Table Example

{% table layout="auto" %}
{% row %}
{% cell header=true %}
Parameter
{% /cell %}
{% cell header=true %}
Type
{% /cell %}
{% cell header=true %}
Default Value
{% /cell %}
{% /row %}
{% row %}
{% cell %}
user\_id
{% /cell %}
{% cell %}
int
{% /cell %}
{% cell %}
Auto generated
{% /cell %}
{% /row %}
{% row %}
{% cell %}
user\_name
{% /cell %}
{% cell %}
string
{% /cell %}
{% cell %}
John Doe
{% /cell %}
{% /row %}
{% row %}
{% cell %}
user\_age
{% /cell %}
{% cell %}
int
{% /cell %}
{% cell %}
25
{% /cell %}
{% /row %}
{% /table %}

## Table Options

To view the table options, right-click on a cell of the table. You will be able to:

- **Insert column left** or **Insert column right**.
- **Insert row above** or **Insert row below**.
- **Duplicate row** or **Duplicate column**, which inserts a copy next to the current one.
- **Merge cells**, or **Split cell** to break a merged cell back apart.
- Set a **Colour** for the cell from the swatches, or **Clear colour**.
- Align the cell contents left, centre or right.
- **Toggle header row** on or off.
- **Pin header row while scrolling**, so the header stays in place as you read down a long table. Select **Unpin header row** to undo it.
- Switch the table between **auto layout** and **fixed layout**.
- **Delete row** or **Delete column**.

To remove an entire table, hover over it and open the block's menu from the drag handle on its left, then delete the block.

## Pinning the Header Row

A table can keep its header row in view while the rest of it scrolls. This pays off most on a very long table, a parameter or field reference for example, where a reader partway down the rows has long since lost sight of what each column means.

To pin it, right-click a cell and select **Pin header row while scrolling**.

A table short enough to fit on screen has nothing to scroll, so pinning leaves it looking exactly as it did.

## Reordering Rows and Columns

Hover over the table to reveal a small grip handle above each column and to the left of each row. Grab a handle and drag it to move that column or row to a new position. A guide line shows where it will land as you drag.

## Resizing Columns

To resize column, hover right before a column ends. A vertical handle will show that is either:

- Grey: Indicates that a width has not been specified. The column auto-sizes.
- Red: Indicates that a width has ben specified. The column has a fixed size.

You can then resize the column by dragging the handle.

To remove set fixed sizing, double click on the handle.

{% callout type="warning" title="Check other screens" %}
If you set a fixed size for a column, then it is best to make sure that it works for other screen sizes.
{% /callout %}

If a table has a fixed size column, then on [exporting](exporting-documentation.md) the documentation, it will not be in markdown format as markdown does not support fixed column widths notation.

## Copying \& Pasting

To copy an entire table, select the table entirely. To make sure you're doing that right, select the line above it and below it then copy. You may then paste it where you need and remove the extra lines.

To copy fields of a table to another table, select the fields in the source table, copy and paste into the destination table. Make sure that the destination table has enough size for the source fields to be pasted in. You may also copy from external sources and paste into %product%.
