# Alice Giliarini
Hi, welcome to my data analysis portfolio!

## Project 1: Webtoon  
[![lore_olympus](images/Screen%20Shot%202022-02-15%20at%2010.55.10%20PM.png)](https://www.webtoons.com/en/romance/lore-olympus/list?title_no=1320)

Webtoon is a company that produces comics which are available for the public to read both online and via a phone app. Each comic has information attached to it such as a single genre tag, a summary, average rating out of 10, total likes across episodes, and the amount of subscribed readers. Such data was collected in the dataset used in this project, taken from [Kaggle](https://www.kaggle.com/swarnimrai/webtoon-comics-dataset). The dataset looks at 569 "Original" Webtoon comics, or comics that are sponsored by Webtoon, and does not include comics available in Webtoon's "Canvas" section where anyone can post.

For this project I:
- Used SQL to sift through Webtoon's summaries of comics, find most used words, and pull-out keywords
- Used Superset to create a dashboard with charts and tables to visualize outcomes 

### Linguistic Data Analysis of Webtoon's Summaries 

To get readers to discover new comics, Webtoon advertises several comics on their homepage that change about once every week. However, if a user would like to discover a new comics on their own, they must look through long lists; these lists are sorted by either most popular, genre (each comic is given one genre), alphabet, or day of the week it's published. A user can also search up comics they know of by title or author. If a user types in "school" in the search bar, Webtoon will show a ist of comics that contain "school" in their title. However comics that are about school, can be given the tag "school," and mention "school" in their summaries, do not show up. As you can see, only 6 comics that have school "school" in their title show up while I found that "school" was mentioned in the summaries of 67 comics. A person interested in reading a comic about school misses out on 61 comics when using Webtoon's current system. As part of this project I've created a list of suggested keywords taken from summaries. If Webtoon opens up the ability to find comics by keywords found in summaries rather than only by keywords found in the comic titles, users will have an easier time finding comics of interest. 

![school](images/Screen%20Shot%202022-02-16%20at%2012.42.33%20AM.png)

As a user, most of the comics I've found have been about entities such as vampires, fairies, and witches; so, my hypothesis was that after breaking down the summaries into a list of single words and after taking away function words, verbs, and adjectives, the remaining list would include non-human entities at the top of the list. This was not the case but some other interesting discoveries were made through out the process. 

![words_barchart](images/Screen%20Shot%202022-02-15%20at%208.10.43%20PM.png)
