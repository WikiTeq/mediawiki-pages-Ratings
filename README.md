Ratings
============

Requirements
------------

* SemanticMediawiki
* MyVariables
* PageForms
* [PagePort](https://github.com/WikiTeq/PagePort) or [PageExchange](https://www.mediawiki.org/wiki/Extension:Page_Exchange)

Contents
--------

* `Template:RatingWidget` - displays rating widget
* `Template:RatingWidgetAutoedit` - renders a single star with an autoedit link
* `Template:Rating` - stores rating data in the Rating namespace
* `Template:GetUserRating` - utility, fetches user rating
* `Template:GetAverageRating` - fetches average page rating
* `Template:GetVotesCount` - fetches votes count
* `Template:GetPageID` - utility, fetches page id
* `Form:Rating` - processing form
* `Property:Rating subject` - stores related rating page
* `Property:Rating user` - stores user rated a page
* `Property:Rating value` - stores rating value

Import via PagePort
-----

Import pages contents respectively to their namespaces, or use [PagePort](https://github.com/WikiTeq/PagePort) extension for easier importing:

```
php extensions/PagePort/maintenance/importPages.php --source .
```

Import via PageExchange
-----

Import page contents as a package using [PageExchange](https://www.mediawiki.org/wiki/Extension:Page_Exchange) extension:

* Make sure you have the PageExchange extension installed
* Add the following line to the bottom of your `LocalSettings.php` file: `$wgPageExchangePackageFiles[] = 'https://raw.githubusercontent.com/WikiTeq/mediawiki-ratings/master/page-exchange.json';`
* Navigate to `Special:Packages`
* Hit `Install` on the package card
* run `php maintenance/runJobs.php`


