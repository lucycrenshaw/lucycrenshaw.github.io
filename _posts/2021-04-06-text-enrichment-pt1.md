---
title: "Text Enrichment: Journal Structure part 1"
excerpt_separator: "<!--more-->"
categories:
  - Blog
classes: wide
show_date: true
---

I am working with volumes 1-19 of the Classical Studies Journal *Classical Quarterly* to practice transforming closed textual materials into open formats and experiment with methods to analyse and enrich those materials. My immediate goals are not aimed at producing material for a thesis or dissertation. Rather, my main goal is to acquire practical skills in computational methods that I can then take with me into the job market. Because my goal favors experience over producing specific results, I have dipped my toes into many different ways to enrich my text. Overall, though, I have focused on reproducing accurately the overall structure of the volumes of this journal rather than on the actual words within the articles. This includes: 1) removing any extra-textual material that transfer from scans of physical texts, (e.g. library stamps, handwritten marginal notes) from the plain text; 2) isolating and tagging page-headers, page numbers, and other elements that are essential to the print version of the text but not necessarily relevant when performing analyses of the actual text; 3) tagging the larger sections of the text such as Front Matter, Issues, Indices, etc. to get at the structural elements of the volumes. 

This process essentially amounts to: regex the sh\*t out of the plain text. I started this process working in simple plain text in Sublime Text. After acquiring the plain text files of scans produced by Hathi Trust (all open access), I split the larger volumes into individual files for Front Matter, Issues 1-4, Indices. I focused on the Issues and attempted to "tag" the structure of the text using regular expressions. The elements I wanted to tag to organize the structure of the texts were: 

* Articles
* Reviews
* Summaries of Periodicals


Within these sections I wanted to tag further details such as: 
		
* Issue title
* Article Title
* Author

Finally, there were things like the page number and page header that I wanted to keep in my plain text file but wrap in a tag in order to easily isolate them when necessary. All of this amounted to a system of tags which I lay out in my data dictionary, which you can find [here](/corpus-dictionary)

Below I give excerpts from the plain text file as it was freshly downloaded from Hathi Trust and as it is now following my tagging and some general clean up:

# Original Plain Text

```
{% include CQ_1907_no1_vol1_original.txt %}
```

# Tagged Plain Text

```
{% include CQ_1907_no1_vol1.txt %}
```

Note the tags I inserted. The regexes I used to produce these results across multiple issue of this journal can be found [here](https://github.com/comp-methods-fsu-2021/Crenshaw_CQCorpus/tree/main/CQ_Issues_vol1-19#readme)

# So what?

The goal for these tags is to help me discern the overall structure of the text. This is useful not just for scrolling through the massive text files or using the "find" function. I can use these tags to help me prepare a text file for analysis. For example, If I'm interested in comparing the length of articles printed in the volumes over time, I can use the tags to isolate the articles section and extract those for word counts. If I want to compare the types of sections included in the volumes over time, these tags are also useful. Finally, if I want to see what words are used frequently in the journal I can use the headers, footers, and page number tags to quickly remove these features so they do not skew my results. 

Because my focus was on structure and not the text itself, you will likely note that the text itself is a bit of a mess. The nature of the articles in these early volumes of the *Classical Quarterly* (largely philological and technical) means that there are a lot of tables and notation for diagramming sentences or counting syllables that do not translate well into plain text. Add in the fact that ancient Greek is used fairly frquently and you've got a recipe for a disaster OCR text. The process of cleaning up the text itself will take a lot longer and will require significant cleaning by hand. Because I wanted to learn specific skills like using regular expressions, I narrowed my focus.


[Text Enrichment Part 2 Here](https://lucycrenshaw.github.io/blog/text-enrichment-pt2/)
