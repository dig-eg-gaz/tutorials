---
layout: page
subheadline: "Jackson Boucher"
title: "Data Visualization on Atom and Excel"
teaser: ""
date: 2017-05-04
categories:
  - tutorial
author: jacksonboucher
tags:
  - tag
header: no
image:
  title: blog-images/image-name.png
  thumb: blog-images/image-name.png
  homepage: blog-images/image-name.png
  caption:
  caption_url:
---

1.
Begin by selecting the table in which you want to pull information from on Oxygen via X-path query. Make sure that the cells on the table are unique to it and not found in other sections or pages of the newspaper.


2.
Use the string: “//table//cell[contains(.,’Augment.’)]/following-sibling::cell[1]/string()” to generate data on X-Path. Replace the “Augment” with the cell that you wish to query. This string of data will select the numbers following the cell you selected.


3.
Once X-Path has generated quality results with few errors, copy the entire list of results and paste them into a blank Atom file.

4.
From there, use the “find” feature and the “replace” feature to look up and get rid of unnecessary text. Press “COMMAND + F” to bring up the find and replace menu. If you wish to get rid of text, type the specific text into the “find” line and nothing in the replace line.

5.
Once your Atom document is rid of unwanted text and only contains dates and cell values, type “\n\n” in the “find” line and nothing the “replace” line to format the data for processing.

6.
Copy and paste all of the data from Atom into a blank Excel spreadsheet.

7.
In order to graph the data, select the entire two columns of dates and values and select “Insert” then “Insert Graph” in the menu of Excel. Chose the one most appropriate for your data and then place it in the spreadsheet.

8.
Remove any special characters like fractions by using Excel’s find and replace feature as well. “COMMAND + F” brings up Excels find menu where you can copy fraction signs and other unrecognizable characters and replace them with simpler numbers.
