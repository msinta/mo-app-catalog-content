---
description: >-
  Step-by-step guide for administrators on how to add a new app to the
  catalogue, including page setup, tags, variables, and content structure.
hidden: true
icon: location-question
cover: >-
  https://images.unsplash.com/photo-1773751392365-dba450a242b6?crop=entropy&cs=srgb&fm=jpg&ixid=M3wxOTcwMjR8MHwxfHJhbmRvbXx8fHx8fHx8fDE3NzQyOTY5OTN8&ixlib=rb-4.1.0&q=85
coverY: 0
---

# How to Add an App

### Overview

Each app in the catalogue is a GitBook page. The easiest way to add a new app is to **duplicate an existing page** and edit it — this ensures the layout, hint blocks, download buttons, and content structure are all set up correctly from the start.

***

### Before you start, duplicate an existing page

1. In the sidebar, hover over any existing app page inside the **Apps** group
2. Click the **...** actions menu → **Duplicate**
3. Rename the duplicated page to your new app's name
4. Open the page and update the following content:
   * **Page description** — the short subtitle shown under the title
   * **App description** — the main body text describing what the app does
   * **Latest version** — update the version number in the content
   * **Download buttons** — update the links to point to the correct download URLs
   * **Hint block** — update any notes, warnings, or tips relevant to this app

Once the content is updated, follow the steps below to set up the metadata that powers the catalogue card.

***

### 1. Rename the page

Click **...** → **Edit title & slug** and set the page title to the app's name. This is what appears as the card title in the catalogue.

***

### 2. Pick an icon

Click the icon button to the left of the page title and choose an icon that represents the app. This displays inside the avatar on the card.

***

### 3. Add tags

Open the page actions menu **...** → **Add tags** and assign the following:

* **One category tag** — `Data`, `Monitoring`, `Productivity`, `Security`, `Analytics`, or `DevOps`
* **One status tag** — `Stable` or `Beta`
* **Verified tag** _(optional)_ — add `Verified` if the app is officially verified

***

### 4. Add variables

Click the **Variables** icon in the top right corner, make sure you're on **Page** scope, and add the following:

| Variable            | Description                                | Example                     |
| ------------------- | ------------------------------------------ | --------------------------- |
| `version`           | Current version number                     | `3.2`                       |
| `price`             | Price in USD, use `0` for free             | `299`                       |
| `publisher`         | Name of the publisher                      | `Acme Corp`                 |
| `requiredProduct`   | Product required to run this app           | `DataHub`                   |
| `supportedVersions` | Comma-separated list of supported versions | `2022 R1, 2022 R2, 2023 R1` |

***

### 5. Commit and sync

Once all fields are filled in, commit the changes in your content repo and push to `main`. GitBook will sync automatically, and the new app will appear in the catalogue within a few seconds.

***

{% hint style="info" %}
**Tip:** The catalogue filters by category tag, so make sure every app has exactly one category tag assigned. Apps without variables will be skipped and won't appear in the catalogue.&#x20;
{% endhint %}
