---
title: Jekyll Pages
---

There is two types of webpages: a blog post and a standalone [page](https://jekyllrb.com/docs/pages/). A blog is usually time-dependent, you published it on a certain date therefore the filename must include a date (which can be any date since you can edit the published date using the `date` front matter tag); whereas a page is meant to be evergreen, so the filename does not have a date.

Another key difference is that blog posts are saved in the `_posts` directory and drafts are saved in the `_drafts` directory whereas pages are saved in any directory. The URL of a page will match the directory it is saved in. For instance, a page in the root directory will be `example.com/page`, a page in `/documentation` will be `example.com/documentation/page`. The URL can be overwritten using the `permalink` tag. Files and folders that begin with an underscore (`_`) are ignored when Jekyll builds your website. The `_posts` and `_drafts` folders are special. You can think of them has having a global permalink in `_config.yml` to take the filename and making a URL from it. For example, `/_posts/2024-11-05-election-day.md` will be converted to `example.com/2024/11/05/election-day`.
