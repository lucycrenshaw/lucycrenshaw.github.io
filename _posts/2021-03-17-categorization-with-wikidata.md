---
title: "Categorization with Wikidata"
date: 2021-03-17T15:34:30-04:00
categories:
  - Blog
tags:
classes: wide
show_date: true
---

# Finding data on Wikidata - Queries

My corpus is issues of the classics journal *Classical Quarterly*. I know that most major journals have a wikipedia page, so I was curious to see what journals I could turn up in a wikidata query for journals in classics. I searched "instance of > academic journal" and "main subject > classics" but this only returned two results: *Transactions of the American Philological Association* and *Mouseion*. I played around with both statements, but I quickly found that this type of query would not produce the results I wanted because the categorization was not consistent. I searched for the wikidata pages for various journals (*Classical World, Classical Journal, Classical Quarterly, AJA, Hesperia*) to try to find some standard categorization but there was no consistency in how these were categorized. For example, journals can be variously categorized as "academic journal", "history journal", "periodical", etc. Additionally, for some classics journals the next most specific category was "title" or "date", which does not allow for a narrowed but still broad search like I wanted to do. Where journals did have more specific statements that categorized them as "classics", there was a wide variation of categorization used. I could search for classics as a "major topic" or "academic discipline" or "field of work", for example. I don't know which choice is necessarily best, but there is no clear standardization for specifying the academic field of focus, which makes it difficult to produce more than one or two journals at a time with each variation of the search. Other also issues arise when searching for these journals, like classical philological and archaeological journals being categorized as "philology" and "archaeology" but not "classics". 

## Give data to Wikidata

I wanted to try out the kind of additions I would add to wikidata to help connect these journals under some type. I added the statement "main subject > classics" to *Classical Quarterly* and *Classical Journal* wikidata. This seems to be the most common statement used to categorize journals in the field of classics. 