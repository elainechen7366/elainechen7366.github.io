---
layout: single
title:  "Highlight Specific Bars in A Bar Chart in Tableau"
excerpt: "How to highlight any bar you want in a bar chart"
header:
  teaser: assets/images/thumbnails/tableau.png
date:   2023-06-03
toc: true
toc_label: "CONTENT"
toc_icon: "columns"
toc_sticky: true
categories: blog
tags: Tableau
page_author: true
---

<!-- #pic: a0001-->

Before getting into the article, I would like to present you with the following diagram. If this could be the effect you expect, let’s get started!

![](https://live.staticflickr.com/65535/52954971940_03a5f1a3ea_h.jpg) 

**Environment**\
Tool: Tableau Public\
Data: [Link](https://github.com/elainechen7366/who_accessible/blob/master/WHO/Data/DisabilityPrevalence.xlsx)\
Note: The data is from World Health Organization, and there is a detailed explanation of every parameter in the first sheet of the Excel.
{: .notice}

**Tips**: You can directly jump to Step3 & Step4 to check how to apply the calculation for marking specific bars.
{: .notice--info}


## Step1: Create Data Source
In this article, I use the income sheet, one of the sheets in DisabilityPrevalence.xlsx, as the data source.

![](https://live.staticflickr.com/65535/52953994772_8050417ec4_h.jpg) 

![](https://live.staticflickr.com/65535/52953994802_bcb9df098e_h.jpg) 

## Step2: Create A Worksheet
Drag parameters Cause Name and Mean from the Data pane to the Columns and the Rows respectively.

![](https://live.staticflickr.com/65535/52955040118_74689b3249_h.jpg) 


## Step3: Create A Calculation
In this example, I managed to filter the bars that contain the word “musculoskeletal”.
Select **Analysis > Create Calculated Field**
You can design a calculation as shown, or design one for your use.

![](https://live.staticflickr.com/65535/52954971980_6f345cece0_h.jpg)

## Step4: Drag Calculation to the Color Block in Marks Pane
Then, we can drag the calculation from the Data pane and drop it into the Color block in the Marks pane.

![](https://live.staticflickr.com/65535/52953994807_fd90de18b8_h.jpg)

From the image above, the bars are divided into two types, one is ‘Null’ and the other is ‘Highlight’. Since I didn’t name the Cause Name without ‘Musculoskeletal’ word in the calculation, the blue ones are named ‘Null’ in the filter block.

If you prefer other color settings, you can change the color of both types of bars via “Edit Colors…” in the color block.

![](https://live.staticflickr.com/65535/52954971930_7b5a7975e6_h.jpg)

Like the presented chart below.

![](https://live.staticflickr.com/65535/52954971935_d59918be51_h.jpg)

Hope this article is helpful to you. If you know any alternative tricks that are more efficient, I’d love to hear about them! Any feedback is appreciated!

