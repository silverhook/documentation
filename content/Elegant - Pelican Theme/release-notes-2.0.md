Title: Elegant 2.0 release notes
Tags: pelican-theme, web-design, project-management
Category: Release notes
Date: 2019-01-05 20:00
Slug: elegant-2-0-release-notes
Subtitle: First community-ran release
Summary: Big improvements on all fronts – loads of bug fixes, improved W3C conformance, a community development model, and a new website.
Keywords:

[TOC]

# Introduction

With more than 4 years in the making, this release started “better late then never”, but it turned out to _so much **much**_ more then that.

With the [community spark re-ignited][announcement_community], this has become the biggest release since probably 1.0. And as such a very worthy release to carry the 2.0 crown.

[announcement_community]: {filename}/community-drien-project.md

# Stats

**119 issues** were [closed in the 2.0 release][milestone-2.0] – an impressive number, even if we take into account that many of the bugs were of an organisational nature, as Pelican Elegant has changed the development and governance model (more on that in a [separate post][announcement_community]). Compare that to [1.3 release][milestone-1.3], which consisted of 4 issues, or the total amount of closed issues so far, which amount to 133.

[milestone-2.0]: https://github.com/Pelican-Elegant/elegant/milestone/3?closed=1
[milestone-1.3]: https://github.com/Pelican-Elegant/elegant/milestone/1?closed=1

Up until [1.3 release][contrib_to-1.3], the only committer was [Talha Mansoor][talha131] with 357 commits.

From 1.3 release until the [2.0 release][contrib_to-2.0] there were **316 new commits in total** and divided as follows (excluding merge commits):

- [Talha Mansoor – “talha131”][talha131]: 264 commits
- [Pablo Iranzo Gómez – “iranzo”][iranzo]: 8 commits
- [Calf Zhou – “calfzhou”][calfzhou]: 7 commits
- [Andrew Wegner – “AWegnerGitHub”][AWegnerGitHub]: 6 commits
- [Matija Šuklje – “silverhook”][silverhook]: 5 commits
- [Jeremy Thurgood – “jerith”][jerith]: 1 commit
- [Mobile Developer – “0x8BADFOOD”][0x8BADFOOD]: 1 commit
- [Leo Torres – “leotrs”][leotrs]: 1 commit
- [Gan Shen – “gshen42”][gshen42]: 1 commit
- [Gert van Dijk – “gertvdijk”][gertvdijk]: 1 commit
- [Miguel Lechón – “debiatan”][debiatan]: 1 commit


[contrib_to-1.3]: https://github.com/Pelican-Elegant/elegant/graphs/contributors?to=2013-10-11&type=c
[contrib_to-2.0]: https://github.com/Pelican-Elegant/elegant/graphs/contributors?from=2013-10-12&to=2018-12-27&type=c

As we can clearly see, by any metric this is a huge milestone for Elegant.

[pelican]: https://getpelican.com
[AWegnerGitHub]: https://andrewwegner.com
[ashwinvis]: https://ashwinvis.github.io/
[calfzhou]: http://gocalf.com
[talha131]: http://oncrashreboot.comf
[iranzo]: https://iranzo.github.io/
[silverhook]: https://matija.suklje.name
[jerith]: http://rhetoric.jerith.org/
[0x8BADFOOD]: https://0x8badfood.github.io/blog/
[leotrs]: http://leotrs.com/
[gshen42]: https://gshen42.github.io/
[gertvdijk]: https://blog.g3rt.nl/
[debiatan]: https://blog.debiatan.net/

# Highlights

Most issues belonged to bugs and dependency updates, amongst the biggest:

- support for HTTPS out of the box by making the links (incl. CDN) protocol agnostic
- fix for search to work again
- fix of accordion menus not opening up – fixes both issues with categories and comments
- fix of table of content
- much improved build speed
- support for Jinja 2.9 (and newer)

But also new features were added. To list just a few:

- article summaries in recent posts
- added links to social networks (if so desired)
- support for several analytics providers
- support for the `series` plugin (instead of the deprecated `multi_part` plugin)
- non-English languages are now possible as default, as well as having translations of articles
- big steps towards full W3C compliance
- support of LaTeX as input format
- support for Disqus comments
- new website and documentation (more on that in a [separate post][announcement_community])

For a full changelog, see below.


# Full ChangeLog

Below is the full changelog:

## Version 2.0 (under development)

* Link to your social profiles
* Upgraded to Twitter Bootstrap 2.3.2
* Upgraded to Tipue Search 3.1
* Support for `custom.css`
* [Stat Counter Analytics ](http://statcounter.com/) support
* Google Universal Analytics support
* Support for custom icons for social profiles
* Support for Pelican (>3.3) new metadata `modified`
* Support for Social Media Tags
* Support for Google Authorship
* Translations support
* `article.comments_intro` that overrides `COMMENTS_INTRO`. Now you can define
  article specific comments introduction
* Add Disqus comments to Pages
* All customizable variables consolidated in a single `_defaults.html`, making
  it easier for you to customize or even *localize* the theme
* Adds author blurbs at the end of the article

### Performance

* Performance improvement- 4x faster output
* Reduce number of HTTP requests using `assets` plugin
* Shortcut icons, like favicon, are disabled by default. Set
  `USE_SHORTCUT_ICONS` to true to enable it

### Visual Style

* Email newsletter subscriber form style matches rest of the theme
* Article images have a visible border
* Block quotes have a quote icon instead of a thick line on left
* Article's paragraph font size is bigger, for better readability
* Remove unnecessary padding in sidebar's tag list
* Archives page and recent posts on home page have better presentation
* Time stamps in categories and tags pages are justified
* Line number in code block is hidden on tablets and phones to save space for
  content
* More sizes of image for Apple Touch icons
* Fixed: Nested lists have different font sizes
* Fixed: CSS style rules for literal block in reST is missing
* Fixed: Long lines in code block will wrap to next line
* Fixed: Code block will not play nice with line numbers
* Fixed: Subscribe button changes its size on smaller screens
* Fixed: Articles under tag heading on tags page are not sorted
* Fixed: URL scheme for blogs which are not published to the root folder
* Fixed: Footer is always under the fold even on smaller length web pages
* Fixed: Site Name and top navigation menu move to left on wide displays
* Fixed: Page link is not active in the navbar if `SAVE_PAGE_AS` is not set to
  default

### Plugins

* Use `neighbor` plugin to show next and previous articles
* Use `assets` plugin to minify CSS and JS files
* Support for `share_post` plugin
* Support for `related_posts` plugin
* Support for `multi_part` plugin

### Behaviour

* Search results link open in the same window, which is consistent with
  internet search engines
* Comments section message changes when user toggles it
* Fixed: Clicking Search button in 404.html does not trigger search
