---
layout: page
title: Upload to Public Source Server
---

Public Source Servers can handle big files, and downloads at a decent speed in China.

### Choose a Source Server

The Public Source Servers available so far are:

* [Tianjin Public Source Server](https://api.zbx1425.tk:8953/bcs-src) - Contributed at own expense by [zbx1425](https://zbx1425.tk)

### Register and Log in

Press "Sign up", and fill in your information. You email will be requested.

After confirming your email, sign in.

### Upload Files

Upload the contents of that folder named after your email. `author.ini` should be at the root directory.

Up to eight files can be uploaded simultaneously, but uploading folder is not possible. Please create folders manually using [New] -> [Folder].

### Avoid Common Mistakes

**`author.ini` should be at the root directory.** Which means the folder named after your email should not appear at cloud, its contents get uploaded instead.

### Refresh data

The Public Source Server refreshes the metadata every 5 minutes.

If you are so eager to see the result, please [click a button there](https://api.zbx1425.tk:8953/bcs-src/metadata.php), then [open this (a blank page)](https://api.zbx1425.tk:8953/bcs-index/responsemerger.php) to refresh the metadata and flush the cache.

Go to the main page of the app, and choose "refresh" from the menu. If you configured everything correctly, your route should show up in the list.

### See also

The commenting feature of this website is worth noticing. Please [check this out.](rssnotif.html)

Note: You may find files like  `***.thumb.jpg`  in your folder. They are automatically generated, and automatically maintanced. Please leave them as-is. If you need to remove a route, just delete them alongside with other files that belongs to the associated route.