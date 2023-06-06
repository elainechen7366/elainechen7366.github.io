---
layout: single
title:  "Highlight Specific Bars in A Bar Chart in Tableau"
date:   2023-06-03
toc: true
toc_label: "CONTENT"
toc_icon: "columns"
toc_sticky: true
categories: 
tags: Tableau
---

Before getting into the article, I would like to present you with the following diagram. If this could be the effect you expect, let’s get started!

![](/../assets/2023-06-03-Highlight-Specific-Bars-in-A-Bar-Chart-in-Tableau/example-diagram.png) 

**Environment**\
Tool: Tableau Public\
Data: [Link](https://github.com/elainechen7366/who_accessible/blob/master/WHO/Data/DisabilityPrevalence.xlsx)\
Note: The data is from World Health Organization, and there is a detailed explanation of every parameter in the first sheet of the Excel.
{: .notice}

**Tips**: You can directly jump to Step3 & Step4 to check how to apply the calculation for marking specific bars.
{: .notice--info}


## Step1: Create Data Source
In this article, I use the income sheet, one of the sheets in DisabilityPrevalence.xlsx, as the data source.

![](/../assets/2023-06-03-Highlight-Specific-Bars-in-A-Bar-Chart-in-Tableau/income-sheet.png) 

![](/../assets/2023-06-03-Highlight-Specific-Bars-in-A-Bar-Chart-in-Tableau/data-source.png) 

## Step2: Create A Worksheet
Drag parameters Cause Name and Mean from the Data pane to the Columns and the Rows respectively.

![](/../assets/2023-06-03-Highlight-Specific-Bars-in-A-Bar-Chart-in-Tableau/drag-parameters.png) 

## Step3: Create A Calculation
In this example, I managed to filter the bars that contain the word “musculoskeletal”.
Select **Analysis > Create Calculated Field**
You can design a calculation as shown, or design one for your use.

![](/../assets/2023-06-03-Highlight-Specific-Bars-in-A-Bar-Chart-in-Tableau/calculation.png)

## Step4: Drag Calculation to the Color Block in Marks Pane
Then, we can drag the calculation from the Data pane and drop it into the Color block in the Marks pane.

![](/../assets/2023-06-03-Highlight-Specific-Bars-in-A-Bar-Chart-in-Tableau/drag-color.png)

From the image above, the bars are divided into two types, one is ‘Null’ and the other is ‘Highlight’. Since I didn’t name the Cause Name without ‘Musculoskeletal’ word in the calculation, the blue ones are named ‘Null’ in the filter block.

If you prefer other color settings, you can change the color of both types of bars via “Edit Colors…” in the color block.

![](/../assets/2023-06-03-Highlight-Specific-Bars-in-A-Bar-Chart-in-Tableau/edit-color.png)

Like the presented chart below.

![](/../assets/2023-06-03-Highlight-Specific-Bars-in-A-Bar-Chart-in-Tableau/new-color.png)

Hope this article is helpful to you. If you know any alternative tricks that are more efficient, I’d love to hear about them! Any feedback is appreciated!

