---
title: "Text Enrichment: Journal Structure part 2"
categories:
  - Blog
classes: wide
show_date: true
---

See [my first post on text enrichmen](/blog/text-enrichment-pt1/) for background on my goals and how I inserted tags in Sublime Text into my plain text files using regular expressions in order to highlight the overall structure of a standard issue of the *Classical Quarterly* Journal. While these tags were useful, the process of using them was tedious. Opening a massive plain text file knowing the tags are there but having no easy way to voisualize the overall structure was not ideal. To fix this, I turned to TEI XML. XML is another means of working with plain text. It's particularly useful for parsing a text, and especially for identify and breaking out the overall structure in a journal. It's also just a useful language for anyone interested in computational methods, because it's such a widely used standard. 

To switch my plain text over to XML, I returned to Hathi Trust and transferred their HTML text for each volume over to an XML file. (Note: I did not separate these Volume files into Front Matter, Issues, and Indices as I did when working in Sublime Text. I kept the volume files intact, which made sense for XML.) Now HTML and XML are not the same, so the first step in this process involved translating HTML into XML. Luckily, the pattern of HTML was standard across all volumes, so I could batch edit these files using regular expressions. I document my process translating the texts to XML [here](https://github.com/comp-methods-fsu-2021/Crenshaw_CQCorpus/blob/main/CQ_XML/CQ_XML_batch-translation.md). 

The next step was to insert divisions into the texts in order to properly parse the structure of the volumes. The Hathi HTML text had some divisions properly noted, so I could simply translate the language into XML. The Hathi text was not perfect, however, and so correcting for these errors involved a bit of hand cleaning as well. I document my process tagging the texts to XML [here](https://github.com/comp-methods-fsu-2021/Crenshaw_CQCorpus/blob/main/CQ_XML/CQ_XML_batch-tagging.md). See again my [data dictionary](/corpus-dictionary) for the tags I used. 

TEI XML creates an outline based on the layers of divisions you insert into the text. Viewing this outline of divisions allows for a better overall picture of the structure of the text. Below is a sample picture of the divisions outline from my Volume 1 XML file (CQ_vol1.xml) and an excerpt from the text:

# Divisions Outline
{% include figure image_path="/assets/images/CQ_vol1_xml-Tree.jpg" %}

Note the divisions I used:
	
* "FrontMatter" for the front matter of the volume
* "Issues" for the section of the volume that includes (generally) issues 1-4
* "No1" through "No4" 
	* note this first volume did not have a No2; this is the kind of structural thing I am interested in! Why no Issue number 2? 
	* Another interesting change to volume structure comes later, starting with volume 12 in 1917: volumes 12-19 combine issues 3-4 instead of printing them individually. 
* "Index" for the volume's various indices (could include a general index, an index locorum, etc.)

Within these divisions are more sub-divisions for each article.

# Text Excerpt

```
{% include CQ_1907_no1_vol1_xml.xml %}
```

# So What?

The goal for these tags is still to help me discern the overall structure of the text. XML's outline makes these structural observations easier. There are other benefits as well. For example, when rendering the XML into a readable facsimile, the tags for the page numbers and page headers remove them from the text. This means I do not have to go through the tedious process of accoutning for these headers and page numbers when performing certain analysis. XML's xPath search function also makes analysis of the text easier. Xpath allows you to isolate different divisions or tags in the text and perform certain functions to them, like find and replace, article count, or word count. 

I have more to do with XML. My tag use is fairly elementary at the moment. TEI has a large set of tags that allow for more specific structuring of the text. It alos allows you to provide contextual data and disambiguation into your text. For example, I can tag the names of all contributors in the text with `<name></name>`. I can further differentiate these with `<name type="author">` and `<name type="editor">`. 




