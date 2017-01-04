---
layout: page
title: "XML Terms"
teaser: "A Proposed Database of XML terms and when to use them"
date: 2016-12-01
author: Samantha Lappin
tags: -XML -Database -terms
image:
  header: ""
  thumb: "https://github.com/Fibinocci1123/blog-posts/blob/patch-1/Database.png"
---
The most common xml terms are: <cb>, <div>, <head>, <p>.
-<cb> is used to indicated column breaks, does not wrap anything, and goes in front of the information from the column it indicates. It also has the characteristic "n." So the beginning of the page would begin with <cb n="1"/> to indicate the beginning of column one.
-<div> is the most common xml term, used to wrap divisions in the paper, like between articles, pages, and within articles that have small divisions. There are many characteristics associated with the division, the most common being "type."
    -Type will be immediately followed by ="", no spaces. In the quotations will be the type of division. Of these there are article (any piece which does not fall under the other categories to follow and is a written article), item (generally used for advertisements, followed by "scope="advertisement"," but can also be followed by any other scope which will be further discussed later.), section (for when the piece has many divisions within it and is not an advertisement or financial table), subsection (the divisions under "section"), wireReport (for the articles which deal with the Reuter and Havas reports which are generally found on page 3, not the financial table), page, and issue (a division for the full days’ worth of pages, when the paper is compiled).
-<head> wraps the heading of the division and must come first in the division or it will cause errors.
-<p> wraps paragraphs in the paper.

Some other xml terms that you might need are as follows: (all of which must be wrapped within a <div>
-<table> this tag requires the element cols="" inside the tag (i.e.: <table cols="3"></table>). Then, within there are the tags <row> and <cell>. Row can have the element cols="" or role="label", the element cols="" will increase or decrease the amount of columns in that row, either removing one from the end or adding on to the side of the table. Role="label" will make the entire row into a label; this does not have to be the first row of the table and can be used more than once.
-<measure> wraps any sort of measurement recorded in the paper, and is generally followed by the element unit="". The following common units in the paper are supported by our xml library: $, LE, ard, balles, cantar, fcs, min (minutes), mm (millimeters), PT, sack, sh (shillings), tal (talari), ton, and £.
-<date> wraps all dates provided in the paper, contains the element when="yyyy-mm-dd" to catalogue the date wrapped.
-<persName> wraps persons names, if you can find the wikidata entry referring to that person, you can include the element ref="" and the link to the page in the quotations.
-<placeName> wraps place names, ref="" can be used similarly to that of <persName>.

The three below will mostly be used for letters and notices:
-<dateline> wraps the line in which the date that the piece was written on appears. Can include more information than just the date. The date itself should be wrapped in the <date> tag.
-<docAuthor> wraps the line in which the author of the document appears, author should be wrapped in <persName> as well.
-<signed> includes the entire ending salutation of the letter including the signature.

Here are some finer details associated with the paragraph:
-<l> wraps verse lines (for poetry).
-<lb> creates a line break (formatted the same way as column break).
-<lg> wraps a line group, or stanza (for poetry).
-<q> wraps a quotation.
-<said> wraps dialogue.
-<hi> (can also be used in headings) uses the element rend="" with "italic" or "bold" to alter the font of the words.

Here are some other scopes and characteristics that can be used:
-scope= is used with type= in the <div> tag to categorize the content wrapped. I found the following scopes useful for the paper: advertisement, announcements (notices, etc. use at your discretion), calendar, financial (generally, this will be in the tag of the financial templates copied from the site, so you don't have to worry much about it), international, letters, local, social, sporting, weather.
-n= number (commonly used with column break and type="page")
