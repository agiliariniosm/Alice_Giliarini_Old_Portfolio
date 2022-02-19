# Alice Giliarini
Hi, welcome to my data analysis portfolio!

## Project 1: Webtoon  

[![lore_olympus](images/Screen%20Shot%202022-02-15%20at%2010.55.10%20PM.png)](https://www.webtoons.com/en/romance/lore-olympus/list?title_no=1320)

Webtoon is a company that produces comics which are available for the public to read both online and via a phone app. Each comic has information attached to it such as a single genre tag, a summary, average rating out of 10, total likes across episodes, and the amount of subscribed readers. Such data was collected in the dataset used in this project, taken from [Kaggle](https://www.kaggle.com/swarnimrai/webtoon-comics-dataset). The dataset looks at 569 "Original" Webtoon comics, or comics that are sponsored by Webtoon, and does not include comics available in Webtoon's "Canvas" section where anyone can post.

### Linguistic Data Analysis of Webtoon's Summaries 

- Used SQL to sift through Webtoon's summaries of comics, find most used words, and pull-out keywords
- Used Superset to create a dashboard with charts and tables to visualize outcomes

#### Most Commonly Used Words

As a user, most of the comics I've found have been about entities such as vampires, fairies, and witches; so, my hypothesis was that after breaking down the summaries into a list of single words and after taking away function words (grammar words), verbs, and adjectives, the remaining list would include fictional entities at the top of the list. This was not the case. 

**Top 10 Specific Nouns**
![top10_specificnouns](images/Screen%20Shot%202022-02-18%20at%202.35.12%20PM.png)

Specific nouns are all nouns that contain semantical meaning and provide a reader with information. While specific nouns do not include non-specific nouns such as "everything" or "everyone," they do include words such as "hats" or "humans". 

This is the process I went throught to get the resuls shown in the bar chart:
1. Split summaries into single words and removed punctuation marks as well as capitalization.
2. Removed function words, adjectives, and verbs. Function words are "grammar words" or words that do not add meaning to a text; they only play a grammatical role. For example, articles such as "the" and "a", conjunctions such as "and", and pronouns such as "she", "he", "it," or "they" are all function words.
3. Replaced plural forms of words with singular forms of words in cases where both forms have the same meaning.
4. Counted how many comics use the remaining words and ranked them in order of most used to least used.
5. Found the percentage of comics containing the words. 

#### Improving User's Discovery of New Comics

**The Problem**

To get readers to discover new comics, Webtoon advertises several comics on their homepage that change about once every week. However, if a user would like to discover a new comic on their own, they must look through long lists; these lists are sorted by either most popular comics, genre (each comic is given one genre), alphabet, or day of the week it's published. A user can also search up comics they know of by title or author. If a user types in "school" in the search bar, Webtoon will show a list of comics that contain "school" in their title. However comics that are about school, could be given the tag "school," and mention "school" in their summaries, do not show up. As you can see, only 6 comics that have "school" in their title show up while "school" was actually mentioned in the summaries of 67 comics. A person interested in reading a comic about school misses out on 61 comics when using Webtoon's current system.

[![school](images/Screen%20Shot%202022-02-16%20at%2012.42.33%20AM.png)](https://www.webtoons.com/en/search?keyword=school)

Another example of users missing out on comics of interest, is when looking for comics about love. While the Romance section has the most occurances of "love," at 29 comics, the genre sections "Drama," "Comedy," "Slice of Life," and "Horror" have multiple comics with "love" found in their summaries. A total of 24 comics outside of the Romance section contain the word "love" in their summary. Since every comic is given only one genre tag, a user will miss all of the comics about love that are not found in the Romance section.

![lovetable](images/Screen%20Shot%202022-02-18%20at%2011.08.05%20PM.png)

**The Solution**

If Webtoon opens up the ability to find comics by tags or keywords found in summaries rather than only by keywords found in the comic titles, users will have an easier time finding comics of interest. I've created a sample list of suggested keywords that Webtoon could use. 

**Suggested Keywords** 
![keywords_barchart](images/Screen%20Shot%202022-02-17%20at%204.07.10%20PM.png)

In making this list I only looked at specific nouns because such words can be used as topics. I considered what percent of comics mentioned the word in their summary, whether the word provides information about the comic, and whether a user would be likely to look up this word to find comics of interest. The keywords in the suggested list appear in atleast 1.58% of comics. Words like "life" and "world" were excluded because they are too vague; all comics are about a "world" and "life" so these words do not provide any information about a comic. In order to decide on how likely a user would look up a keyword, a small sample of people was given a list of keywords and was asked to assign each keyword a number 1-3. One being "this is not a useful keyowrd", two being "I'm not interested in this keyword but others are likely to be interested," and three being "I would use this keyword to find comics of interest." All words with an average score below 1.5 were removed from the list. 

#### Other Discoveries

Here are some other linguistic data points that were looked at and some discoveries that were made.

**Fictional Humanoid Entities**
![fictional_entities](images/Screen%20Shot%202022-02-18%20at%202.19.06%20PM.png)

This barchart shows how frequently the names of some common fictional humanoid entities appear in the summaries of comics.

**Journey, Adventure, Quest**
![journey_adventure_quest](images/Screen%20Shot%202022-02-18%20at%202.22.11%20PM.png)

A preference for "journey" was found over it's two synonyms "adventure" and "quest"

**Girl, Boy, Man, Woman**
![girl_boy_man_woman](images/Screen%20Shot%202022-02-18%20at%2012.51.21%20PM.png)

"Girl" and "Boy," referring to children, were both used more frequently than the words "man" and "woman," referring to adults. While "girl" was used more frequently than "boy," "man" was used more frequently than "woman." 
