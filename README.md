Ratings
============

Requirements
------------

* [SemanticMediawiki](https://www.semantic-mediawiki.org/wiki/Semantic_MediaWiki)
* [SemanticResultFormats](https://www.mediawiki.org/wiki/Extension:Semantic_Result_Formats)
* [MyVariables](https://www.mediawiki.org/wiki/Extension:MyVariables)
* [PageForms](https://www.mediawiki.org/wiki/Extension:Page_Forms)
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
git clone https://github.com/WikiTeq/mediawiki-ratings.git ~/mediawiki-ratings
cd /mediawiki
php extensions/PagePort/maintenance/importPages.php --source ~/mediawiki-ratings
```

Import via PageExchange
-----

Import page contents as a package using [PageExchange](https://www.mediawiki.org/wiki/Extension:Page_Exchange) extension:

* Make sure you have the PageExchange extension installed
* Add the following line to the bottom of your `LocalSettings.php` file: `$wgPageExchangePackageFiles[] = 'https://raw.githubusercontent.com/WikiTeq/mediawiki-ratings/master/page-exchange.json';`
* Navigate to `Special:Packages`
* Hit `Install` on the package card
* run `php maintenance/runJobs.php`

Usage example
------

The simplest use case is to add a `{{RatingWidget}}` template call to a page.
This will render a 5 star rating widget allowing users to vote for the page rating.
Once votes the template will create a `Rating:1234/USERNAME` page with vote information stored there.

Properties stored are:
* `Subject` - page the vote relates to
* `Rating` - a number 1 to 5, the vote value
* `User` - the username of the user voted

