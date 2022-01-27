---
permalink: /docs/new_user.html
layout: default
title: Information to add or update members on team page
pagetype: doc
---

### Adding a New Team Member

#### US CMS DEI website
You should submit a pull request with the photo, a markdown file with the summary information above, and your proposal to this repo:

<https://github.com/uscms-diversity-equity-inclusion/uscms-diversity-equity-inclusion.github.io>

* Add a photo named `First-Last.jpg` or `.png` to the [assets/images/team folder](https://github.com/uscms-diversity-equity-inclusion/uscms-diversity-equity-inclusion.github.io/tree/master/assets/images/team). It should be 320x240 pixels.
* Add a "`<your github username>.md`" file to the [people folder in the website repository](https://github.com/uscms-diversity-equity-inclusion/uscms-diversity-equity-inclusion.github.io/tree/master/_data/people). Here is an example:

```yml
---
active: true
hidden: false
institution: CERN
name: George P. Burdell
photo: "/assets/images/team/<First name>-<Last name>.jpg"
shortname: gpb
title: Test User
website: https://en.wikipedia.org/wiki/George_P._Burdell
---
```
