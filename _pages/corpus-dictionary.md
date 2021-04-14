---
permalink: /corpus-dictionary/
title: "Corpus Dictionary"
classes: wide

---



## The Classical Quarterly

* *years*: 1907-1925
* *Number of Volumes*: 19
* *Number of Words*: 5251



## Data Dictionary 

### Divisions

* Front Matter
* Index
* Issue (no1-4)
* Section (further divided below)

### Sections

* Articles
* Reviews
* Summaries of Periodicals

### Plain Text in Sublime Text:
* `@new-page` and `@` bracket page breaks
* `@page-header` and `@` bracket page headers such as article title, author name, and page number
* `@article-title` marks the title of each article
* `@issue-title` marks the title of each issue 
* `@start-article@` and `@end-article@` brackets each article body
* `@article-author` marks the author's name of the article
* `!!start-articles!!` and `!!end-articles!!` brackets the articles and reviews section of each issue
* `!!start-summaries-of-periodicals!!` and `!!end-summaries-of-periodicals!!` brackets summaries of periodicals section

### TEI XML in Oxygen
* For the front matter of the volume:`<div type="FrontMatter">`
* For the issues section of the volume: `<div type="Issues">`
* For the index of the volume: `<div type="Index">`
* For each Issue: `<div type="No1">` 
	* attributes "No1", "No2", "No3", "No4", and "No3-4" are all used 
* the start of each article: `<div type="Article">`
* To mark page number and page headers `<pb n="2" rend="H. I. BELL"/>`
* headers tag also used, but inconsistently based on Hathi generated HTML divisions: `<head></head>`