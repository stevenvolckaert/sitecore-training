<p align="center">
    <a href="introduction.md">← Introduction</a> | <strong><a href="#">Module 1</a></strong> | <a href="module-2.md">Module 2 →</a>
</p>

# Module 1: Sitecore Overview

***Content for module 1 is not in the booklet - We'll get it on Friday.***

* Sitecore Experience Editor (in 7.2) = Sitecore Page Editor in 7.0/7.5
* Sitecore is an ASP.NET application. Requirements for 8.0: ASP.NET 4.5 / MVC 5.1 / IIS Integrated mode. See
  compatibilty table on kb.sitecore.net/articles/087164. More compatibility tables are available in the knowledge base.
* [Sitecore Developer network (SDN)][1] is outdated. Use it for pre-8 versions. Use [community.sitecore.com][2] for
  newer versions.
* There's a Slack channel of Sitecore community. See Google to find it.
* You can post support tickets on [support.sitecore.net][3], but you need to be Sitecore certified.
* [Sitecore Knowledge Base][4]

A Sitecore solution has 3 databases:
* `core` (SQL)
* `master` (SQL)
* `web` (SQL)
* xDB = Experience database. MongoDB NoSL collection; available since 7.5
* Reporting (SQL)

Only SQL databases are supported at this time. No possibility to distribute the `master` database.

* Sitecore doesn't have default presentation. You need to create that yourself. Exception Sitecore SXA (not sure about
  the spelling of this abbreviation).

* In a live environment, we should disable access to the Sitecore client (*/sitecore). **This is not the case with
  www.barco.com.**

[2]: https://sdn.sitecore.com
[1]: https://community.sitecore.com
[3]: http://support.sitecore.net
[4]: https://kb.sitecore.net

<p align="center">
    <a href="introduction.md">← Introduction</a> | <strong><a href="#">Module 1</a></strong> | <a href="module-2.md">Module 2 →</a>
</p>
