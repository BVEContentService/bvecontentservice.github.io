---
layout: page
title: Comment Notification
---

Utterances based on Github Issues is used currently as commenting system by BCS. Unfortunately, it is bind with my account, so all the comments poured into my email inbox instead of yours.

Because of the expense of most sendmail services, so email relay is not provided. But we still managed to provide a way to let you know the newest comments.

**RSS Source.** Although it seems that this is not how RSS should work, we are using it to present the comments to you.

Find a RSS reading service of your favor, which must feature manually adding a subscription link. You can use Outlook on PC, or [com.madsvyat.simplerssreader](https://cn.apkshub.com/app/com.madsvyat.simplerssreader) on android.

Your link will be:

```
https://api.zbx1425.tk:8953/bcs-ugc/rss.php?author=[Your email used in BCS]
```

For example:

```
https://api.zbx1425.tk:8953/bcs-ugc/rss.php?author=zbx1425@outlook.com
```

You can try commenting your own route, and then sync the RSS. Remember to enable automatic sync, and check regularly.

![Valid RSS](https://validator.w3.org/feed/images/valid-rss-rogers.png) This RSS source has been validated by W3C :D