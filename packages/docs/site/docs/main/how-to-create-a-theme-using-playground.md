---
title: Build a WordPress Theme
slug: /how-to-create-a-theme-using-playground
---

import ThisIsQueryApi from '@site/docs/\_fragments/\_this_is_query_api.md';

# How to Build a WordPress Theme in WordPress Playground

WordPress Playground is a powerful tool that lets you build, preview, and export WordPress themes—all in your browser or locally via `wp-now`.

This guide walks you through the process step-by-step.

---

## 🚀 1. Creating a New Site

### In the Browser

1. Go to [https://playground.wordpress.net](https://playground.wordpress.net)
2. Click **"Create New Site"**
3. Choose WordPress and PHP versions if needed
4. Click **"Launch"**

### Locally with `wp-now`

1. Install `wp-now`:

    ```bash
    npm create wp-now@latest
    ```

2. Navigate to your theme folder and run:

    ```bash
    wp-now
    ```

3. Access the local site at:

    ```
    http://localhost:8888
    ```

---

## 🧰 2. Preinstall Theme-Building Tools

Install the following plugins for theme development:

-   [Create Block Theme](https://wordpress.org/plugins/create-block-theme/)
-   [Gutenberg](https://wordpress.org/plugins/gutenberg/)
-   [Theme Check](https://wordpress.org/plugins/theme-check/)

Directly use playground links to load plugins: https://playground.wordpress.net/#%7B%22plugins%22:%5B%22hello-dolly%22,%22gutenberg%22%5D,%20%22login%22:%20true,%20%22landingPage%22:%20%22/wp-admin/plugins.php%22%20%7D

### Install via WP Admin

Navigate to:

**Plugins > Add New > Search > Install > Activate**

### Or install via WP-CLI

```bash
wp plugin install create-block-theme gutenberg theme-check --activate
```

## 🎨 3. Install a Starter Theme

Starter themes give you a foundation to begin building your WordPress theme. There are several ways to load a starter theme in Playground:

### 🧩 Option 1: Install from GitHub

You can load a GitHub-hosted theme directly in WordPress Playground using a URL parameter.

**Example:**

https://playground.wordpress.net/?blueprint-url=https://raw.githubusercontent.com/WordPress/blueprints/refs/heads/trunk/blueprints/install-activate-setup-theme-from-gh-repo/blueprint.json


### 📦 Option 2: Upload from ZIP

You can also upload a ZIP file of your starter theme manually:

1. Go to **Appearance > Themes > Add New > Upload Theme**
2. Click **Choose File** and select your `.zip` theme file
3. Click **Install Now**
4. Once installed, click **Activate**

---

## 🧪 4. Import Demo Content

To design and test your theme effectively, you may want to load demo content such as pages, posts, and media.

1. Navigate to **Tools > Import**
2. Select the **WordPress** importer
3. Upload a `.xml` export file containing demo content (e.g., from [wpexport.lxml](https://wordpress.org/plugins/wordpress-importer/))
4. Follow the prompts to assign authors and import attachments

---

## 🔧 5. Build and Customize the Theme

Once your starter theme and demo content are loaded:

-   Use **Site Editor** to modify templates and template parts (Appearance > Editor)
-   Create or customize blocks using the **Block Editor**
-   Activate plugins like:
    -   [Create Block Theme](https://wordpress.org/plugins/create-block-theme/)
    -   [Gutenberg](https://wordpress.org/plugins/gutenberg/)
    -   [Theme Check](https://wordpress.org/plugins/theme-check/)

These tools help you iterate and ensure theme standards.

---

## 📤 6. Export Your Theme

Once your theme is ready, you can export it:

### 🗜️ Export as ZIP

1. Use the **Create Block Theme** plugin
2. Go to **Appearance > Create Block Theme**
3. Select **Export** and download the `.zip` of your custom theme

### 🔗 Export to GitHub

For advanced workflows:

1. Use the Playground query API to clone from a GitHub repo and push back changes
2. Or export the theme zip and upload to your GitHub repository manually

---

## 📥 7. Import from a GitHub Pull Request

You can even test themes from a specific pull request:

**Format:**

?theme=https://github.com/username/repository/compare/feature-branch.zip

Or use GitHub actions to create a ZIP from a PR and link it in Playground.

---

## 🔷 Blueprint URL for Creating a Block Theme

You can quickly create a block theme in Playground by using a blueprint URL. For example, opening the URL below automatically loads the blueprint for a block theme:

https://playground.wordpress.net/?blueprint-url=https://raw.githubusercontent.com/WordPress/blueprints/refs/heads/trunk/blueprints/create-block-theme/blueprint.json

Simply paste this URL into your browser or use it when launching a new site in Playground to get started with a preconfigured block theme setup.

---

With these steps, you can fully design, test, and share WordPress themes within WordPress Playground — without needing a local development environment.
