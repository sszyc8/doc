---
title: Local
description: Authentication Module
published: 1
date: 2024-07-29T07:27:11.034Z
tags: 
editor: markdown
dateCreated: 2024-07-29T06:58:43.197Z
---

This is the default, built-in authentication module for Wiki.js.

It's enabled by default and cannot be disabled.

# Setup

There's nothing to configure in order to use this authentication strategy. However, there're extra settings you can enable, such as self-registration.

From the **Administration Area**, click on **Authentication** in the left navigation and click on **Local** in the strategies list.

## Self-registration

Users can create accounts on your wiki when you enable the **Self-registration** option.

Unless your wiki is public and allow anyone to create an account, it's generally a good idea to set an email **domain whitelist**. Enter a valid domain (e.g. example.com) and press <kbd>Enter</kbd>. You can add as many domains as needed.

Make sure to set a **group** to be assigned to when the user login for the first time.

Click **Apply** at the upper right of the page to save and apply the configuration.

> :warning: You **must** setup the mail SMTP settings (under **Mail** in the Administration Area) for the registration emails to be sent. Users won't be able to login until they verify their account, using a link sent to their email address.
{.is-danger}