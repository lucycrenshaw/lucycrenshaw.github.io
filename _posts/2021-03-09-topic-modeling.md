---
title: "Adventures with Topic Modeling"
date: 2021-03-09T15:34:30-04:00
categories:
  - blog
tags:
  - Jekyll
  - update
classes: wide
show_date: true
---

# Intro

I worked with issues 1-4 in volumes 1-6 of Classical Quarterly from my corpus to try some topic modelling. I used the Topic Modelling Tool. While Underwood's blog was useful for providing some context for topic modelling, I'm not sure I still fully understand how it works. I have many questions about the topics that my corpus produced and what the topics actually represent. I also do not understand if running the topic modeling tool multiple times makes a difference or not. That being said, I think I can see some real potential with my corpus if I can figure it out. My main hurdle for now appears to be issues with cleaning my text. I need to progress further with cleaning before I can see real results. This includes removing headers, footers, page numbers, etc. from more of my corpus. I will also probably need to identify and remove tables that the OCR could not translate to clear out some of the noise. It would also likely be helpful to isolate the articles and book reviews into individual files but this will take time. 

The basic steps I followed were:

1. I created a metadata file for the topic modeling tool, though I'll admit I'm not sure what the metadata file does for the topic modeling.
2. Cleared out the headers, page numbers, and markups I put into my plain text files for input into the topic modeling tool. 
3. I ran these through the topic modeling tool a few times, choosing different numbers of topics. I played around with 5, 10, 20, and 30 topics. I settled on 10, though I'm not sure there is any real reason, besides just needing to pick a number. 
4. I made a pivot table and line chart with the topic modeling results. I'm not sure about the overall value or meaning of the pivot table (this is clearly a theme). The x axis is the date of publication for the issues in each volume and y-axis is the average of the 4 topics I chose to highlight across the issues. 
5. I tried to use issues of Classical World as reference text but the plain text was too messy to produce much

# Results?

The ten topics produces were:

0. caesar arbitration pompey roman battle enipeus argos rome senate liv romans dio camp pharsalus kromayer dr field henderson river south
1. est amici merc mil ps truc capt si poen rome socii trin pers foedus mr bcd amicitia septen dial cas
2. 1 2 3 4 5 om 6 7 8 9 10 13 12 11 14 15 16 17 dative 18
3. mss readings reading ms isidore iliad sparta octavian augment cp 1910 family treveth bauli scor oed odyssean soc zeus suppliants
4. και δε το των ι εν τ ή περί τα κ τε του οι δ μεν aristotle έν λ ο
5. ferrero signor helvetii ariovistus mother caesar apollo agar ode earth temple gaul plato hymn religious deities helen world god euripides
6. narrative augment tomic speeches scansion iliad b2 caesura syllabic odyssey days trochaic aorist elision break 4th semi towns unaugmented day
7. 1 2 3 de ii και 4 cf 5 6 read greek 8 7 words iii sense est text der
8. om la à les le il des wind favourable en césar helvètes ferrero signor ship qu dans holmes ships une
9. ο ι mr marx urv lat skr ur lucilius latin fragment ellis base cornford fragments article jr uv mueller thucydides

The most interesting to me are topics 0, 1, 3, and 6. I will repeat what I have already said multiple times: I'm not sure what exactly these topics are telling me. If I'm following Underwood's blog correctly, it seems like these topics should tell me the general discourse behind the scenes in the academic community in these years (or at least the academic community submitting articles to this particular journal). This is obviously limited by the number of volumes I used, 6, and the years covered, 1907-1912. What is not clear to me is the cohesion of the individual words in the topics. Why are "isidore iliad sparta octavian" all included in the same topic?

The line chart shown below, produced from my pivot table, I think shows the distribution of the 4 topics I chose (0,1,3,6) across the various issues. If this is correct, it is perhaps interesting that they spike across years, issues, and volumes.

{% include figure image_path="/assets/images/PivotTableTopicModeling.jpg" %}
