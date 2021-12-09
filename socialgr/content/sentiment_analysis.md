---
title: "Sentiment Analysis - how do our characters feel?"
date: 2021-12-08T18:30:01+01:00
draft: false
description: 
    "This is the home page to reveal the most awesome networks and stats about South Park!"
# description
description: "This is meta description"
---
While we wanted to do a sentiment analysis, much like with the Zelda project, we unfortunately did not have any appropriate data. Wiki pages tend to be written in very neutral language, which means that while methodologies like the LabMT do work, they do produce strange results. Essentially, instead of analysing and finding the sentiment of each character, one could only find the sentiment of the character’s Wiki page itself. As will be shown by the examples below, the associated sentiment does not match with the actual character’s personality.

Sometimes, one could have been lucky enough to find some trivia or quotes on some Wikis, but unfortunately this was not the case. If this was true for our Wiki, it would have been possible to extract only the quotes, like we did with the attributes, and analyse those.  

We even tried to get data from sources like this: https://github.com/deankeinan/SouthPark-rnn/blob/master/samples/sample-big.txt , which is someone's project where they fed a neural network 19 seasons of South Park. Unfortunately, when looking at the samples of the text, a lot of the created sentences did not make sense and thus would have probably provided an even worse base for the sentiment analysis. Especially because these quotes are not real, but generated.

We still analysed sentiment of 14 major characters, including the main characters. The variations are visible when looking at a character like Kenny. In the show, Kenny is a very happy character, and mostly positive, however, he does die a LOT. This means that his character’s Wiki page has the most negative sentiment, out the tested characters. Kenny scored 0.324.

Whereas, when looking at a person like Liane Cartman, Cartman’s mother, one would expect her sentiment to be negative, because she has quite a tough life in the show. However, she scored the happiest on the sentiment rating, at 0.677.

Furthermore, 8 out of the characters had scores of 0.5, excluding Kenny and Liane, that is 2/3, which is strange when examining the characters themselves. Among these were Jimmy Valmer, Mr Mackey, Shelly Marsh, and Kyle. All of these characters have an extremely different outlook on life, and thus it did not make much sense to analyse all of the 1870 characters, especially because this would take around 3 hours to run.