---
type: page
title: Synced Blocks
listed: true
slug: synced-blocks
description: 
index_title: Synced Blocks
hidden: 
keywords: 
tags: blocks
---

Synced blocks enable you to create a single piece of content (single-sourcing) that can be reused across multiple pages as often as necessary. When you modify a synced block, those changes are automatically reflected across all pages where the block is utilised, ensuring consistency and efficiency in your content management.

## Reuse Content - Creating Synced Blocks

To create a synced block:

{% synced id="open-block-menu" %}
{% /synced %}

- Choose Synced Block {% icon classes="fas fa-clone" /%}.
- Choose Create New Synced Block. A form will show.
- In the form, you need to define:
    - ID: An identifier for the synced block. ID cannot be modified once the synced block is saved. The ID will be shown in your exports. For example, if you are writing a guide about how to install docker, then your ID could be `docker-installation`.
    - Title: Choose a title that describes what the content is about, so your teammates can find it easily. The title can be changed later.
    - The contents: Use the editor to write the contents of the synced block. The contents can be changed later. The contents can be anything you can already add on %product%.

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1637268467/v2_1/itgncmmhvfhnqhspyiqk.gif" mode="responsive" height="986" width="1580" %}
{% /image %}

## Reuse a Synced Block

To reuse a synced block:

- Start a new line (using {% key key="↵" /%})
- Click on {% icon classes="fas fa-plus" /%} to open the blocks menu.
- Choose Synced Block {% icon classes="fas fa-clone" /%}.
- Choose Choose Existing Synced Block.
- Select the synced block you want to reuse, or search for it first.
- Click on Select.

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1637268820/v2_1/clvzrwd0iaap0ssxtzdd.gif" mode="responsive" height="986" width="1580" %}
{% /image %}

## Identifying a Synced Block

When you're in the editor, synced blocks will have a {% badge type="warning" text="Synced" /%} badge at the top right. Once you hover on a synced block, an orange dotted line will show what contents are exactly in the synced block.

{% image url="https://res.cloudinary.com/developerhub/image/upload/v1637269710/v2_1/yq1zxvfhyehbrrfvzyvd.jpg" mode="responsive" height="654" width="886" %}
{% /image %}

## Editing a Synced Block

Modifying a synced block changes its contents in all instances it is used. This operation can only be done by Publishers.

To edit a synced block:

- Go to a page that has the synced block to be edited.
- Click on the {% icon classes="fas fa-pencil-alt" /%} icon at the top right of the synced block.
- A form will appear where you can modify the title and contents.
- Make the changes and click Save.

## Deleting/Archiving a Synced Block

Once a synced block is added to your project, it can never be deleted but it can be archived. Archiving a synced block does not remove its instances from any page it is added to, but it only removes it from the list of synced blocks that your teammates can choose.

To archive a synced block:

- Start a new line (using {% key key="↵" /%})
- Click on {% icon classes="fas fa-plus" /%} to open the blocks menu.
- Choose Synced Block {% icon classes="fas fa-clone" /%}.
- Choose Choose Existing Synced Block.
- Find the synced block to archive, and hit the {% icon classes="fas fa-times red" /%} icon next to it.
- Confirm your choice.

## Using Page Links in Synced Blocks

You can link to pages inside a synced block. However, there are limitations to its use.

{% callout type="warning" title="Page Linking Limitation" %}
When the synced block is used in a different version than the one created in, it will be matched using the page slug. Changing the page slug in the source version or the destination version will break the link - and you will be notified when viewing a page that has the synced block.

For example: If you created a synced block that links to "Contact Us" page in v1.0 having "contact-us" slug, then used the synced block in v2.0 and later changed the Contact Us page slug to "how-to-contact-us", then the page link will break in v2.0. You would need to create a separate synced block for v2.0 to handle this situation.
{% /callout %}