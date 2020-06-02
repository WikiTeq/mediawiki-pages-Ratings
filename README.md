Ratings Book
============

Requirements
------------

* SemanticMediawiki
* MyVariables
* PageForms

Contents
--------

* Template:RatingWidget - displays rating widget
* Template:RatingWidgetAutoedit - renders a single star with an autoedit link
* Template:Rating - stores rating data in the Rating namespace
* Template:GetUserRating - utility, fetches user rating
* Template:GetAverageRating - fetches average page rating
* Template:GetVotesCount - fetches votes count
* Template:GetPageID - utility, fetches page id
* Form:Rating - processing form
* Property:Rating subject - stores related rating page
* Property:Rating user - stores user rated a page
* Property:Rating value - stores rating value

Setup
-----

Import pages contents respectively to their namespaces, or use `GitExport` extension for easier importing:

```
php extensions/GitExport/maintenance/importPages.php --source .
```

