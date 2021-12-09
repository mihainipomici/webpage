---
title:  "Graphs! Series vs. the Game!"
date: 2021-12-04T18:30:01+01:00
draft: false
description: 
    "This is the home page to reveal the most awesome networks and stats about South Park!"
---
Purpose:
---
This section reveals the most awesome network visualizations and network analysis for South Park!


Networks are presented based on the characters from the whole SP series and the characters only present in the 'Stick of Truth' game. Let's see what can we discover!

Note: this section is rather meant to be engaging and **informal**. For a more formal in-depth analysis and the source code, one can check the notebook provided in
this [GitHub repository](https://github.com/TeoAndB/SouthPark_NetworkAnalysis) - Part_B_Data_Analysis (Section:
Networks and Visualization).

South Park Network - for the whole Series!
---
Let us visualize the network of the whole South Park Series. This is how the network was built:

- **Nodes**: SP characters
- **Node Attributes**:
  - real name: character name as it appears on the Wiki page
  - game role: Playable Characters, Enemies, Land of Zaron, Merchants or Not in the Game
  - series role: characters' role in the series (main character, major-supportive character, other (if not specified))
  - gender: Male, Female or Unknown
  - race
  - episode appearance

- **Edges**: each character will be linked to the other characters based on their interactions given by the Wiki pages

{{< figure  src="/networks_img/SPGraph_gendercolor3.png" width="1000">}}

That is a huge network!
It has 1639 nodes and 5736 edges! The nodes and edges are colored based on gender:
- Male: blue 
- Female: pink
- Unknown: green

It seems that most of the SP characters are predominantly male (what a surprise!). This is according to the data analysis of the DataFrame object that was created (see: Stick of Truth - Reveal the Stats!)

Let us do more Network Analysis and plot the in- and out- degree distributions:

![South Park Network - in and out degree distribution](/networks_img/in_out_degree_distr.png)

Could this be? It seems that both the in- and the out- degree histograms follow a power-law distribution!
In order to confirm, let's bin again the degree (in and out degrees combined) using the log-log scale:

![South Park Network - degree distribution](/networks_img/degree_bining.png)


So it is true, it's all in the data! 
As the degree bining follows a power-law distribtuion, the SP network is a scale-free network. This means that the network follows the preferrential attachment law: newly emerged nodes are more likely to connect to the nodes with higher degree (also called as 'the-rich-get-richer' phenoenon). 

Node Kelly ("Rainforest Schmainforest") has the minimum the degree value of 1
Node Eric Cartman has the maximum the degree value of 358.
So if the network keeps evolving (South Park is an on-going series), Cartman will get most connections!

![Evil Cartman likes having lots of connections so he can backstab everyone](/networks_img/cartman_evil.jpg)

The Stick of Truth Network - let's dig in the game!
---

Now that we have the whole SP network, let's color the nodes according to the role of each character in the 'Stick of Truth' game.
The source code can be found again in the [GitHub repository](https://github.com/TeoAndB/SouthPark_NetworkAnalysis) - Part B, section: Stick of Truth Network!.

For those of you who do not know, this game is the first politically correct game made for children, which is based on the South Park Series.
Reveal the truth! How many characters are actually in the game?

![South Park Network - game color](/networks_img/SPGraph_gamecolor3.png)

Now we can see the nodes much more clearly! The names are displayed for the top 7 most connected nodes. 
The coloring of the nodes and edges are based on the game roles:
- Playable Characters: green
- Land of Zaron: lime green
- Enemies: red
- Merchants: azure blue
- Not in the Game: gray

Only 126 nodes are colored. That means only 7.7% of the series characters are in the game. 
This is not a lot, considering how long the gameplay is... Then you can only imagine how long the series is! Happy binging!

Let us extract the Game Network only:

![South Park Game Network](/networks_img/SPGameGraph.png)

So pretty! The characters in the images are the main SP and game characters: Eric Cartman, The New Kid, Stan Marsh, Wendy Testaburger (we had to show one female at least!), Kenny and Kyle. 
The Stick of Truth network has 126 nodes and 708 links.

Node Jessica Rodriguez has the minimum the degree value of 1. Node Eric Cartman (again!?) has the maximum the degree value of 60. And he is not even the main game character!
The New Kid, the guy you play with in the game, has only 54 links! And if that's not sad enough, in the graph drawing above he is obstructed by fat Cartman... poor him :(

![South Park Network - cartman talk](/networks_img/cartman_stick_of_truth.jpg)

**More network stats!**
Let's do bining of the degree distribution:

![South Park Network - degree distribution](/networks_img/SPGameGraph_bining_degree.png)

It seems that the node degrees tend to follow a power-law distribution, but the graph is too small for this to be certain. More data would be needed to confirm this 

#### Oh well, that's it for the Network Visualization and Analysis. Click on 'Home' on the sidebar and check out the other sections for more fun!



