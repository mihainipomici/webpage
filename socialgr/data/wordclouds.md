---
title: "Word Clouds: All PC down here.. (maybe?)"
date: 2021-12-08T18:30:01+01:00
draft: false
description:
    "This is the home page to reveal the most awesome Wordclouds generated from the characters of South Park!"
---
Purpose:
---
This is the home page to reveal the most awesome Wordclouds generated from the characters of South Park!

We have generated wordclouds for a few categories.


Note: this section is rather meant to be engaging and **informal**. For a more formal in-depth analysis and the source code, one can check the notebook provided in
this [GitHub repository](https://github.com/TeoAndB/SouthPark_NetworkAnalysis) - Part_B_Data_Analysis (Section:
Networks and Visualization)


Wordclouds - Really good insight from just a cloud of words
---

By analysing the SP characters and attributes, we came up to the conclusion to generate insights from generating a few wordclouds for different categories

These include:
  - WordClouds for each gender category
  - Wordclouds for the top five generated communities
  - Wordcloud for the main male and female character respectively

#### So, are you excited to see the magic Wordclouds? Hmm, you are silent, then I will take it as a Yes.

Let's dive in. 

In order to reach from plain text from a website there is a very long and cumbersome process that is described more in depth in the explainer notebook.
However, I will quickly pass you through the steps. 
<ol>
  <li>We need to start with indepth web scraping in order to obtain characters data in a good format.</li>
  <li>Cleaning/refining the text for further processing
   <ul>
      <li>Applying regex functions</li>
      <li>Manual data cleaning</li>
     <li>Saving to text files</li>
    <li>Applying NLP tools like removing stopwords, lower-casing, lemmetization</li>
    </ul>
    </li>
  <li></li>
  <li>Applying TF-IDF Vectorization on the freshly cleaned text</li>
</ol>

### Genders 

We have identified three categories:
 - Male
 - Female
 - Unknown

Let us take a look at the resulting word clouds. 

![Word Cloud for each gender](/wordcloud_img/wordcloud_gender.png)

#### Comments

In these three wordcoulds you can see the most frequent words used by each gender from the biggest font displaying the most pronounced word to other less frequent. It is very interesting to observ what are women talking about in comparison to men. The third category encapsulates all other characters which do not have gender information. Thus, the last category is less informative but still interesting to observe. 

As we can see, men have different topics n comparison to women as seen from the word cloud. A lot of description is centered around hair in words like **mustache, beard, goatee** being some of the most used. Also, in male description we can see  **working** a lot as well as **friday** since we believe a lot of talking is about friday especially after working. There are also other words distinct to men as **hell, wrong, balding, angry, poor**. We can also observe the word **jr** which is self explanatory since South Park is about kids who are in school.

For female characters descriptions we can observe very female specific things as **cheerleading, bathroom, dating..."**. In both males and females we can see anger since there is a lot of tension in the series. Also, in both genders there is discussion about election. We can observe that they are also interested in politics. Surprisingly there is not so much talking about **shopping**.

In general, we can observe that the word clouds are a good indicator of main topics and mainstream words that describe each gender in this case. It is always interesting to analyze and discuss about the findings that show the specific features of each category. 

### Communities

After applying the Louvaine Algorithm we have identified 17 communities. Thus, out of those we decided to focus on five biggest and create wordclouds.

So, let's check what have we got in here. 

![Word Cloud for top five communities](/wordcloud_img/wordcloud_community.png)

#### Comments 

Above, we can see a wordcloud for each of the top five identified communities. From the images we can conclude that each community has certainly different predominant words meaning that the algorithm worked well. Taking a look into each word cloud separately we cannot see from the start any correlation between words. However, in **Community nr 7** we can probably deduct the main topic being in school as we can see words like **hallway, cafeteria, lunch, classroom...**

Rest of the words in the communities come from the characters who are more linked to each other. However, they might not have as many things in common and the words are not as informative. Also, one would need to have a lot pf prior knowledge about the characters and South Park in general to better understand and draw insights from it. 

### Two main characters

Here we will present you two word clouds of the lines from the South Park series of the two main characters from male gender and female gender .At the start we wanted to do analysis only on Eric Cartman, but then we thought, isn't that a bit sexist privileging just the male character?
Considering that we live in a world where we are all equal it is fair to do some analysis on the female character as well. So, she is Wendy Tastaburger.
The analysis was completed like in the previous steps, from web scraping from the very first episode till the last of the last season. A lot of lines, yeah, There are 27 seasons, so imagine. 
Enough talking, images speak a thousand words. In our case ot os literal and in the very direct sense.
Let's take a look.

![Word Cloud for Eric Cartman lines](/wordcloud_img/eric_wc.png)

![Word Cloud for Wendy Tastaburger lines](/wordcloud_img/wendy_wc.png)

#### Comments

Interesting findings. Here we can see the most frequent words said by both characters. We can observe that the characters are using a lot of short words and mostly to express a sentiment at the moment like **oh, yeah, okay, right, na**. We all know that Wendy is in love with Stan Marsh and this can be also seen in the wordcloud as she is pronouncing his name the most. 

This is all my friends. on this I am finishing the wordcloud section. Enjoy! Ah yeah, do not forget the popcorn!

