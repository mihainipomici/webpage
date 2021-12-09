---
title: "Reveal the Stick of Truth! And DataFrame stats!"
date: 2021-11-26T18:30:01+01:00
draft: false
description: 
    "This is the home page to reveal the most awesome networks and stats about South Park!"
---
Purpose:
---
This section will present some DataFrame visualizations. 
For further information regarding how this DataFrame was compiled, one can check the notebook provided in this [GitHub repository](https://github.com/TeoAndB/SouthPark_NetworkAnalysis) - Part_A_Data_Mining (Section: DataFrame).

The Data:
---
The information in the table above is a sneak-peak into the DataFrame object we have created using the API content of the Wiki pages of the South Park Archives (the Data Source hyperlink on the sidebar will take you to the landing page).
The name of the characters, as well as the attributes presented below, were retrieved using the APIs of the Wiki archives.

![South Park Network - in and out degree distribution](/dataframe_img/SocialGraphs_DataFrame_2.png)
The DataFrame object contains:
- Name of each South Park character (but the URL name containing special characters)
- Real Name of each South Park character (as it appears on the Wiki page)
- Game Role in the 'Stick of Truth' Game: Playable Characters, Enemies, Land of Zaron, Merchants or Not in the Game
- Series Role, which refers to the role categories in the whole series (main character, major-supportive character, or other if not specified)
- Gender: Male, Female or Unknown
- Race: race of each South Park character (all 136 of them!)
- Appearance: Episode appearance

Data Visualization!
---
Let's count the character role categories of the entire SP Series:

![South Park Network - in and out degree distribution](/dataframe_img/DF_series_categories_count.png)
The bar chart above shows, that while most of the South Park characters remain uncategorized, there is yet a wide range of about 19 character categories for the SP series. It seems that one of the largest categories are the 4th Graders and the Monsters. This is expected, as the main SP characters are 4th graders, and there are a lot of weird monsters and talking animals in the series. Another noticeable category is the Political Celebrities, which South Park loves to make fun of.


Now let's take a look at the gender distribution:
![South Park Network - in and out degree distribution](/dataframe_img/DF_gender_count.png)

The bar chart on gender attributes of the DataFrame object reveals that most of the SouthPark characters are male. Less than half of the characters are female and a small amount of the characters' gender is unknown (including the non-binary gender). Considering the character categories discussed above, this is somewhat expected as some SP characters are not human.

We have 136 races (!!), so let's count the occurencies of the top 5:

![South Park Network - in and out degree distribution](/dataframe_img/DF_topraces_count.png)

The counts of the top races of the SP characters is displayed in the bar plot above. Unfortunately most of the SP characters did not have assigned a race or it was not properly retrieved from the TXT files. But as far as the TXT files were looked through, the first reason seems more plausible. The most frequent revealed race of the South Park characters is Caucasian. It is expected that most of the SP characters are caucasian, as the series action takes place in the fictional South Park town which is supposedly located in the Colorado state in the US. Following this, it is also explainable why the second most-frequent race in the series is African-American.

Last but not least, which characters are worthy to be in the Stick of Truth game?

![South Park Network - in and out degree distribution](/dataframe_img/DF_count_game.png)

The counts above regarding the Stick of Truth Game is entirely different. Since the South Park universe is huge, it is expected that most of the characters are not in the Stick of Truth Game.

Referring to the characters' categories in the game, the most frequent one is 'Other characters', followed by the 'Land of Zaron' and 'Enemies'. Playing the game, one can confirm that yes, a lot of the game characters belong to the 'Land of Zaron', which is the ally land assigned to find the stick of truth. However, most of the other characters make only a small appearance in the game (but you can still battle them!), so it makes sense why they are not categorized. 

In the game, one can battle with most characters, however they are not considered the main enemies of the story. This explains why the 'Enemies' category is not as large as the 'Other characters' category.

#### What a nice DataFrame we have... So many attributes, which ones should be displayed in the graphs? Go 'Home' and find out by clicking on the next section: Graphs! Series vs. the Game! 