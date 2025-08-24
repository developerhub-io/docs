---
type: page
title: Tables
listed: true
slug: tables
description: 
index_title: Tables
hidden: 
keywords: 
tags: blocks
---

%product% tables consists of a header row and data rows.

To create a table:

{% synced id="open-block-menu" %}
{% /synced %}

- Select Table {% icon classes="fas fa-table" /%}

### Table Example

{% table %}
| Parameter | Type | Default Value | 
| ---- | ---- | ---- | 
| user_id | int | Auto generated | 
| user_name | string | John Doe | 
| user_age | int | 25 | 
{% /table %}

## Table Options

To view the table options, right-click on a cell of the table. You will be able to:

- Insert column left {% icon classes="fas fa-plus" /%}
- Insert column right {% icon classes="fas fa-plus" /%}
- Delete column {% icon classes="fas fa-times" /%}
- Duplicate column {% icon classes="fas fa-clone" /%}
- Insert row above {% icon classes="fas fa-plus" /%}
- Insert row below {% icon classes="fas fa-plus" /%}
- Delete row {% icon classes="fas fa-times" /%}
- Duplicate row {% icon classes="fas fa-clone" /%}
- Reorder rows and columns {% icon classes="fas fa-caret-up" /%} {% icon classes="fas fa-caret-down" /%} {% icon classes="fas fa-caret-left" /%} {% icon classes="fas fa-caret-right" /%}

Note: You can also add new rows to the end by tapping {% key key="Tab" /%} key.

## Resizing Columns

To resize column, hover right before a column ends. A vertical handle will show that is either:

- Grey: Indicates that a width has not been specified. The column auto-sizes.
- Red: Indicates that a width has ben specified. The column has a fixed size.

You can then resize the column by dragging the handle.

To remove set fixed sizing, double click on the handle.

{% callout type="warning" title="Check other screens" %}
If you set a fixed size for a column, then it is best to make sure that it works for other screen sizes.
{% /callout %}

If a table has a fixed size column, then on [exporting](/support-center/exporting-documentation) the documentation, it will not be in markdown format as markdown does not support fixed column widths notation.

## Copying & Pasting

To copy an entire table, select the table entirely. To make sure you're doing that right, select the line above it and below it then copy. You may then paste it where you need and remove the extra lines.

To copy fields of a table to another table, select the fields in the source table, copy and paste into the destination table. Make sure that the destination table has enough size for the source fields to be pasted in. You may also copy from external sources and paste into %product%.