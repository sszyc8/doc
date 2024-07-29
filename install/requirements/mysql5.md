---
title: MySQL 5.7 Notice
description: Limited support for this MySQL version
published: 1
date: 2024-07-29T07:05:19.853Z
tags: 
editor: markdown
dateCreated: 2024-07-29T07:01:06.900Z
---

# Affected versions

- MySQL **5.7.8** and up in the 5.7.x range.

# Limited Functionality

## Uploads

Uploading assets is only possible in the root folder. It's not possible to upload files in a folder or nested folders. Doing so will result in an error at upload time.

# Cause

MySQL 5.7.x does not support the `WITH RECURSIVE` expression, which is required to fetch the folder hierarchy. This expression was introduced in version 8.0.