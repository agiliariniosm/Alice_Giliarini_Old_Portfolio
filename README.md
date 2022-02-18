# Alice Giliarini
Hi, welcome to my data analysis portfolio!
It is a work in progress.

## Project 1: Webtoon  
[![lore_olympus](images/Screen%20Shot%202022-02-15%20at%2010.55.10%20PM.png)](https://www.webtoons.com/en/romance/lore-olympus/list?title_no=1320)

Webtoon is a company that produces comics which are available for the public to read both online and via a phone app. Each comic has information attached to it such as a single genre tag, a summary, average rating out of 10, total likes across episodes, and the amount of subscribed readers. Such data was collected in the dataset used in this project, taken from [Kaggle](https://www.kaggle.com/swarnimrai/webtoon-comics-dataset). The dataset looks at 569 "Original" Webtoon comics, or comics that are sponsored by Webtoon, and does not include comics available in Webtoon's "Canvas" section where anyone can post.

For this project I:
- Used SQL to sift through Webtoon's summaries of comics, find most used words, and pull-out keywords
- Used Superset to create a dashboard with charts and tables to visualize outcomes 

### Linguistic Data Analysis of Webtoon's Summaries 

As a user, most of the comics I've found have been about entities such as vampires, fairies, and witches; so, my hypothesis was that after breaking down the summaries into a list of single words and after taking away function words, verbs, and adjectives, the remaining list would include non-human entities at the top of the list. This was not the case but some other interesting discoveries were made through out the process. 

[![school](images/Screen%20Shot%202022-02-16%20at%2012.42.33%20AM.png)](https://www.webtoons.com/en/search?keyword=school)

To get readers to discover new comics, Webtoon advertises several comics on their homepage that change about once every week. However, if a user would like to discover a new comics on their own, they must look through long lists; these lists are sorted by either most popular, genre (each comic is given one genre), alphabet, or day of the week it's published. A user can also search up comics they know of by title or author. If a user types in "school" in the search bar, Webtoon will show a list of comics that contain "school" in their title. However comics that are about school, can be given the tag "school," and mention "school" in their summaries, do not show up. As you can see, only 6 comics that have school "school" in their title show up while I found that "school" was mentioned in the summaries of 67 comics. A person interested in reading a comic about school misses out on 61 comics when using Webtoon's current system. If Webtoon opens up the ability to find comics by tags or keywords found in summaries rather than only by keywords found in the comic titles, users will have an easier time finding comics of interest. As part of this project I've created a sample list of suggested keywords.

In making this list I only looked at specific nouns and considered what percent of comics mentioned the word in their summary, whether the word provides information about the comic, and whether a user would be likely to look-up this word to find similar comics. The keywords in the suggested list appear in atleast 1.58% of comics. Words like "life" and "world" were excluded because they are too vague on their own; all comics are about a "world" and "life" so these words do not provide information on the comic. In order to decide on how likely-hood a user would look-up a keyword, a small sample of people was given a list of keywords and was asked to assign each keyword a number 1-3, 1 being "this is not a useful keyowrd", 2 being "I'm not interested in this keyword but others are likely to be interested," and 3 being "I would use this keyword to find comics of interest." All words with an average score below 1.5 were removed from the list. 

**Suggested Keywords** 
![keywords_barchart](images/Screen%20Shot%202022-02-17%20at%204.07.10%20PM.png)

![fictional_entities](images/Screen%20Shot%202022-02-18%20at%202.19.06%20PM.png)

![journey_adventure_quest](images/Screen%20Shot%202022-02-18%20at%202.22.11%20PM.png)

![girl_boy_man_woman](images/Screen%20Shot%202022-02-18%20at%2012.51.21%20PM.png)


