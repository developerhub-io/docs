---
type: page
title: Synced Blocks
listed: true
description: Discover how to streamline your content management with synced blocks. Learn to create, reuse, edit, and archive these blocks for consistent messaging across pages. Enhance efficiency by ensuring changes reflect everywhere instantly. Perfect for teams looking to save time!
index_title: Synced Blocks
hidden: false
keywords: 
tags: blocks
---

Synced blocks enable you to create a single piece of content (single-sourcing) that can be reused across multiple pages as often as necessary. When you modify a synced block, those changes are automatically reflected across all pages where the block is utilised, ensuring consistency and efficiency in your content management.

## Reuse Content - Creating Synced Blocks

To create a synced block:

{% synced id="open-block-menu" /%}

- Choose Synced Block {% icon classes="fas fa-clone" /%}.
- Choose Create New Synced Block. A form will show.
- In the form, you need to define:
  - **ID:** An identifier for the synced block. Once saved, the ID cannot be modified. This ID will be visible in your exports. For example, if you are creating a guide on installing Docker, your ID could be `docker-installation`.
  - **Title:** Select a title that accurately represents the content, making it easy for your teammates to locate. Note that the title is editable and can be changed later.
  - **The contents:** Utilise the editor to compose the contents of the synced block. These contents are flexible and can be modified later. Feel free to include any [blocks](writing-documentation/blocks.md) that are already supported in %product%.

{% image url="https://image-archive.developerhub.io/image/upload/v2_1/itgncmmhvfhnqhspyiqk/1637268467.gif" /%}

## Reuse a Synced Block

To reuse a synced block:

- Start a new line (using {% key key="↵" /%})
- Click on {% icon classes="fas fa-plus" /%} to open the blocks menu.
- Choose Synced Block {% icon classes="fas fa-clone" /%}.
- Choose Choose Existing Synced Block.
- Select the synced block you want to reuse, or search for it first.
- Click on Choose.

{% image url="https://image-archive.developerhub.io/image/upload/v2_1/clvzrwd0iaap0ssxtzdd/1637268820.gif" /%}

## Identifying a Synced Block

When you're in the editor, synced blocks will have a {% badge text="Synced" type="warning" /%} badge at the top right. Once you hover on a synced block, an orange dotted line will show what contents are exactly in the synced block.

{% image url="https://image-archive.developerhub.io/image/upload/v2_1/yq1zxvfhyehbrrfvzyvd/1637269710.jpg" /%}

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

## Editing in a Synced Repository

If your project uses [GitHub Sync](github-sync.md), your synced blocks are mirrored to the repository under `_synced-blocks/`, one file per block, named after the block's ID. You can write and review a block there like any other change, and blocks you edit in the editor are committed back. See [Synced Blocks](github-sync.md#synced-blocks) for the file layout and frontmatter.

## Using Page Links in Synced Blocks

You can link to pages inside a synced block. However, there are limitations to its use.

{% callout type="warning" title="Page Linking Limitation" %}
When the synced block is used in a different version than the one created in, it will be matched using the page slug. Changing the page slug in the source version or the destination version will break the link - and you will be notified when viewing a page that has the synced block.

For example: If you created a synced block that links to "Contact Us" page in v1.0 having "contact-us" slug, then used the synced block in v2.0 and later changed the Contact Us page slug to "how-to-contact-us", then the page link will break in v2.0. You would need to create a separate synced block for v2.0 to handle this situation.
{% /callout %}
