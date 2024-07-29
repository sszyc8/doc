---
title: GitHub
description: Authentication Module
published: 1
date: 2024-07-29T07:27:08.585Z
tags: auth, module
editor: markdown
dateCreated: 2024-07-29T06:58:39.502Z
---

GitHub Inc. is a web-based hosting service for version control using Git.

# Setup

## A) Create OAuth GitHub Application

1. Go to the [New OAuth Application](https://github.com/settings/applications/new) page on GitHub
 	- You can also use your organization instead of your personal account by going into your organization settings page and click on `OAuth Apps`, then `New OAuth App`.
1. Enter an **Application Name** (e.g. Wiki.js).
1. Enter the **Homepage URL** to your wiki.
1. Enter the **Authorization callback URL**.  
	This value can be found in Wiki.js under **Configuration Reference**, displayed below the settings of the GitHub strategy.
1. Click **Register application**.
1. A **Client ID** and **Client Secret** will be shown. Copy these 2 keys. We'll need them later.
1. *(Optional)*{.caption} Upload an avatar for this application.

## B) Enable the GitHub strategy in Wiki.js

1. In the **Administration Area** of your wiki, click on **Authentication** in the left navigation.
1. Click on **GitHub**.
1. Enter the **Client ID** and **Client Secret** values copied earlier.
	> **For GitHub Enterprise Only:**
		> - Turn on the **Use GitHub Enterprise** toggle.
  	> - Enter your **GitHub Enterprise Domain** *(without http/s prefix or trailing slash, e.g. github.yourdomain.com)*
    > - Enter your **GitHub Enterprise User Endpoint** *(e.g. https://api.github.yourdomain.com)*
	{.is-info}
1. Enable the **Self-registration** option *(unless you plan on authorizing users manually)*.
1. Select the **group** new users should be assigned to when they login for the first time.
1. Make sure the checkbox next to **GitHub** in the list of strategies is checked. The text should now say that the strategy is **active**.
1. Click **Apply** on the upper right of the page to save and apply the configuration.

![](https://static.requarks.io/logo/github.svg =x50){.align-abstopright}
