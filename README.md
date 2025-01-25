# Make It Space Wiki

Welcome to the **Make It Space Wiki** repository. This repository contains all the resources, templates, and instructions to document and manage equipment for the Make It Space project. Below, you'll find detailed instructions on creating new equipment pages, using templates, and working with the repository structure.

This project uses the **Just the Docs** template, which is a clean, customizable, and responsive documentation theme for Jekyll. For more information, visit the [Just the Docs website](https://just-the-docs.com/). If you need additional help with Jekyll, refer to the [official Jekyll documentation](https://jekyllrb.com/).

---

## **Creating a New Equipment Item**

To add a new equipment item to the Wiki:

1. **Start with the Template:**
   - Navigate to the `_equipment` directory.
   - Copy the `templatefrontmatter.md` file and rename it to match your new equipment name, e.g., `LaserCutter.md`.

2. **Fill Out the Front Matter:**
   Update the front matter of your new file with the following fields:

   ```yaml
   ---
   layout: equipment
   title: [Equipment Name]
   permalink: /docs/equipment/[equipment_slug]/
   name: [Equipment Name]
   parent: Equipment
   picture: /data/productpictures/[image_name].jpg
   description: |
     [Detailed description of the equipment]
   rate: [Green/Amber/Red]
   qty: [Number of items available]
   manual: [Link to manual or "/data/equipment/manual.pdf"]
   sop: [Link to SOP or "/data/safety/sop.pdf"]
   materials:
     - [Material 1]
     - [Material 2]
   resources:
     - title: [Resource Title]
       link: [Resource Link]
   ---
   ```

3. **Save Pictures and Documents:**
   - Save equipment pictures in `/data/productpictures`.
   - Save SOPs in `/data/safety`.
   - If manuals are not available online, upload them to `/data/equipment`.

4. **Verify the Page:**
   - Add your new equipment file to the `docs/equipment/` directory.
   - Run the development server locally to preview changes:
     ```bash
     bundle exec jekyll serve
     ```
   - Access the site at `http://127.0.0.1:4000/` and verify your equipment page is listed under the **Equipment Index**.

---

## **Tracking Changes**

We are using the following spreadsheet to track the progress of equipment documentation:
[Equipment Tracking Spreadsheet](https://docs.google.com/spreadsheets/d/1gl224OAmsTvoBz5uktKIdwRRtR62sBOruspWH7qHvdM/edit?usp=sharing)

### Spreadsheet Legend:
- **Orange Rows:** Someone else is working on this item. Ensure you have checked the spreadsheet and clicked the item before making changes.
- **Green Rows:** The page is complete and contains all required information.

---

## **Development Workflow**

To manage unconfirmed pages or changes:

1. **Use the Development Branch:**
   - Always push new or unverified changes to the `development` branch.
   - Create a new branch from `development` for larger edits.

   ```bash
   git checkout development
   git checkout -b feature/[new-feature-name]
   ```

2. **Test Your Changes:**
   - Preview the site locally using:
     ```bash
     bundle exec jekyll serve
     ```

3. **Submit a Pull Request:**
   - Once changes are verified, submit a pull request to merge into the `main` branch.

4. **Deployment:**
   - The `main` branch triggers automatic deployment and updates the live site.
   - Only the **MIS Officer** has permission to merge changes into `main`.

---

## **File and Directory Structure**

- **Equipment Pages:** `_equipment/`
- **Pictures:** `/data/productpictures/`
- **SOPs:** `/data/safety/`
- **Manuals:** `/data/equipment/`

---

