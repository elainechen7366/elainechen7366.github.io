---
layout: single
title:  "Website Style Test Post"
excerpt: "This post is for a quick check of most of the styles that may appear in an article"
header:
  teaser: assets/images/thumbnails/color.png
date:   2023-06-08
toc: true
toc_label: "CONTENT"
toc_icon: "columns"
toc_sticky: true
categories: blog
tags: Jekyll
---
## What Is This Post For? 
When I tried to create my own skin with the minimal-mistakes Jekyll theme, I found out that I have to collect posts from others to ensure the inclusion of all styles. At the moment, I really hope there's a post for me to conveniently review the configuration of the new skin. That's why I create this post.

>Since this article is used for checking the look of skin mainly, I extract articles about Adelie Penguin in Wikipedia.

My personal favoriate is Adelie!
{: .notice}

[Original Ariticle](https://en.wikipedia.org/wiki/Ad%C3%A9lie_penguin){: .btn .btn--info}
[Original Ariticle](https://en.wikipedia.org/wiki/Ad%C3%A9lie_penguin){: .btn .btn--primary}
[Original Ariticle](https://en.wikipedia.org/wiki/Ad%C3%A9lie_penguin){: .btn .btn--success}
[Original Ariticle](https://en.wikipedia.org/wiki/Ad%C3%A9lie_penguin){: .btn .btn--warning}
[Original Ariticle](https://en.wikipedia.org/wiki/Ad%C3%A9lie_penguin){: .btn .btn--danger}


## The Adelie Penguin
The **Adélie penguin** ***(Pygoscelis adeliae)*** is a species of penguin common along the entire coast of the Antarctic continent, which is the only place where it is found. It is *the most widespread penguin species*, and, along with the [emperor penguin](https://en.wikipedia.org/wiki/Emperor_penguin), is the most southerly distributed of all penguins. 

It is named after Adélie Land, in turn, named for Adèle Dumont d'Urville, who was married to French explorer Jules Dumont d'Urville, who first discovered this penguin in 1840. 
{: .notice--primary}

Adélie penguins obtain their food by both predation and foraging, `with a diet of mainly krill and fish`.

![Adélie](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e3/Hope_Bay-2016-Trinity_Peninsula%E2%80%93Ad%C3%A9lie_penguin_%28Pygoscelis_adeliae%29_04.jpg/1280px-Hope_Bay-2016-Trinity_Peninsula%E2%80%93Ad%C3%A9lie_penguin_%28Pygoscelis_adeliae%29_04.jpg)

### Taxonomy And Systematics
The first Adélie penguin specimens were collected by crew members of French explorer Jules Dumont d'Urville on his expedition to Antarctica in the late 1830s and early 1840s. Jacques Bernard Hombron and Honoré Jacquinot, two French surgeons who doubled as naturalists on the journey, described the bird for science in 1841, giving it the scientific name Catarrhactes adeliæ.[^1]

[^1]: [Hombron & Jacquinot 1841](https://en.wikipedia.org/wiki/Ad%C3%A9lie_penguin#CITEREFHombronJacquinot1841), p. 320.

### Behaviour And Ecology
Despite their size, Adélie penguins are known for their **bold and boisterous personality** and will challenge other animals, including predators far larger than them.[^2]
{: .notice--success}

[^2]:  ["Top 10 facts about Adélie penguins"](https://www.wwf.org.uk/learn/fascinating-facts/adelie-penguins). WWF. Retrieved 29 July 2021.

In footage shot for the 2018 BBC Earth documentary Spy in the Snow, the boisterous behaviour of Adélie penguins was made especially apparent when an individual arrived to chase off a Southern giant petrel that had landed to threaten a group of emperor penguin chicks, in spite of the species difference between them.

#### Food And Feeding
The Adélie penguin is known to feed mainly on Antarctic krill, ice krill, Antarctic silverfish, lanternfish, amphipods, sea krill, glacial squid and other cephalopods (diet varies depending on geographic location) during the chick-rearing season.

#### Breeding
Adélie penguins breed from October to February on shores around the Antarctic continent. Adélies build rough nests of stones. Two eggs are laid; these are incubated for <mark>32 to 34 days</mark> by the parents taking turns (shifts typically last for 12 days). The chicks remain in the nest for 22 days before joining crèches. The chicks moult into their juvenile plumage and go out to sea after 50 to 60 days.

**Threats**\
Kelp gulls and snowy sheathbills also prey on chicks and eggs.
{: .notice--warning}


## Status
A comprehensive census of the global Adélie penguin population was carried out in 2014 using analysis of high-resolution satellite images in combination with actual field surveys. The researchers looked for guano-discoloured coastal areas (red/brown patches in areas with no snow) in the satellite images, and augmented their findings with field surveys in areas where no good satellite images were available or where the presence of multiple penguins species was suspected. The results of field surveys were only used if they had been done within the previous four years.


## Code Block

<i class="fas fa-exclamation-triangle"></i> This part is only for testing the display of different kinds of code. The code below is not executable mostly.
{: .notice--danger}

### C++
```c++
#include <iostream>
#include <fstream>
using namespace std;

int main() {
  int a = 0, b = 1;
  a = a + b;
  // Create and open a text file
  ofstream MyFile("filename.txt");

  // Write to the file
  MyFile << "Files can be tricky, but it is fun enough!";

  // Close the file
  MyFile.close();
}
```
### JAVA
```java
public class Main {
  public static void main(String[] args) {
    String name = "John";
    System.out.println("Hello " + name);
  }
}
```
### PYTHON
```python
# python is case sensitive language
import dowhy.api
import dowhy.datasets

data = dowhy.datasets.linear_dataset(beta=5,
    num_common_causes=1,
    num_instruments = 0,
    num_samples=1000,
    treatment_is_binary=True)

# data['df'] is just a regular pandas.DataFrame
data['df'].causal.do(x='v0', # name of treatment variable
                     variable_types={'v0': 'b', 'y': 'c', 'W0': 'c'},
                     outcome='y',
                     common_causes=['W0']).groupby('v0').mean().plot(y='y', kind='bar')
```
### R
```R
# --- Install packages
install.packages("dplyr")
install.packages("readxl")

# --- Load libraries
library("dplyr")
library("readxl")

print("---------------- daily_activity ----------------")
glimpse(daily_activity)

names(daily_calories)[names(daily_calories) == "Id"] <- "id"

if (sum(is.na(minute_intensities_narrow)) != 0) {
    print("Position of missing values:")
    which(is.na(minute_intensities_narrow))
} else {
    print("No missing value")
}

```
### JSON
```json
{
  "firstName": "John",
  "lastName": "Smith",
  "age": 25
}
```
### HTML
```html
<section class="page__share">
  {% if site.data.ui-text[site.locale].share_on_label %}
    <h4 class="page__share-title">{{ site.data.ui-text[site.locale].share_on_label | default: "Share on" }}</h4>
  {% endif %}
</section>
```
### CSS
```css
.grid-container {
  display: grid;
  grid-template-columns: repeat(6, 1fr);
  grid-template-rows: repeat(3, auto);
}
```
### SCSS
```scss
p > code,
a > code,
li > code,
td > code {
  padding-top: 0.1rem;
  padding-bottom: 0.1rem;
  font-size: 0.9em;
}
@include breakpoint($x-large) {
    max-width: $max-width;
}
```
## Others

| Name        | Contact           | Note  |
| :---        |    :----:         |  ---: |
| Amy         | <amy@email.com>   | 30y   |
| Brian       | <brian@email.com> | 25y   |


---
I will continue to update this post as I discover something new.
{: .notice--info}
