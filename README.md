# Build Your Own Storefront -- Day 1

## Store Brief

### Niche Selection

**Chosen Niche:** Musical Instruments & Studio Equipment

I have chosen to build an online musical instruments and studio
equipment store. The store will offer products such as guitars,
keyboards, pianos, drums, microphones, audio interfaces, studio
monitors, headphones, and music accessories.

### Product Complexity Justification

This niche provides sufficient product complexity to demonstrate
advanced Shopify functionality throughout the module. Products naturally
have multiple variants, including brand, colour, size, instrument type,
handedness, number of strings, key count, finish, connectivity
(wired/wireless), and skill level. These characteristics make the store
well suited for implementing product variants, collection filtering,
custom metafields, and structured Metaobjects later in the project.

------------------------------------------------------------------------

## Audience and Page Scope

### Target Audience

This store targets beginner, intermediate, and professional musicians
who want high-quality instruments and studio equipment for practice,
performance, and recording. It also serves music teachers, students,
producers, and hobbyists looking for reliable products, expert buying
guidance, and educational resources.

### Custom Pages

#### 1. Buying Guides

**Purpose:** Help customers choose the right instrument based on their
experience level, budget, and musical goals.

**Potential Metaobjects:** - Buying Guide - Skill Level - Recommended
Product - Instrument Category

------------------------------------------------------------------------

#### 2. Brand Spotlight

**Purpose:** Showcase the history, product range, and unique strengths
of major music brands available in the store.

**Potential Metaobjects:** - Brand - Brand Story - Country of Origin -
Featured Collections

------------------------------------------------------------------------

#### 3. Learning Hub

**Purpose:** Provide educational content, maintenance tips, beginner
lessons, and instrument care guides to support customers beyond their
purchases.

**Potential Metaobjects:** - Lesson - Instructor - Instrument Guide -
Maintenance Guide

------------------------------------------------------------------------

## Development Environment

**Development Store:** *To be added after the Shopify development store
has been created.*

**Hot Reload Verification:** *Pending completion of
`shopify theme dev`.*

# SoundCraft – Day 2 Planning

## Part 1 – Filter Inventory

### Filter 1: `money`

* **Section/File:** `sections/main-product.liquid`
* **Purpose:** Formats the product price as South African Rand currency, making prices easier for customers to read.

### Filter 2: `image_url`

* **Section/File:** `snippets/card-product.liquid`
* **Purpose:** Generates the correct URL for each product's featured image so that product cards display optimized images.

### Filter 3: `upcase`

* **Section/File:** `snippets/card-product.liquid`
* **Purpose:** Displays the product brand or instrument category in uppercase to improve visibility and create a consistent design.

### Filter 4: `truncate`

* **Section/File:** `snippets/card-product.liquid`
* **Purpose:** Shortens long product descriptions on collection pages so that product cards remain uniform in height and easier to browse.

### Filter 5: `handleize`

* **Section/File:** `sections/main-collection-product-grid.liquid`
* **Purpose:** Converts collection or tag names into URL-friendly handles for links and HTML identifiers.

---

## Part 2 – Conditional Logic Plan

### Liquid Object / Property

`product.selected_or_first_available_variant.inventory_quantity`

### Conditional Logic

If the selected product variant has an inventory quantity greater than zero, the product page will display an **"In Stock"** message and allow customers to add the item to their cart.

If the selected product variant has no available inventory, the page will display an **"Out of Stock"** message and disable or hide the **Add to Cart** button to prevent unavailable purchases.

### Location

The conditional logic will be implemented in:

`sections/main-product.liquid`

