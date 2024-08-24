# Do NICE's recommended questions get answered

## What is this about?

In the comments of Experimental History, I made a [bold claim](https://open.substack.com/pub/experimentalhistory/p/whos-got-the-guts-to-go-to-the-moon?utm_campaign=comment-list-share-cta&utm_medium=web&comments=true&commentId=62272451):

> > Meta-analyses come out all the time that are like, “Unfortunately, all of the studies that try to answer this important question are so bad that we can’t learn anything from them.” Instead of running another 500 piddling, confounded little studies, someone with guts, taste, and money could run the actually good study.
> 
> The National Institute of Health and Care Excellence (NICE) is a UK body that determines clinical guidelines. When they publish their clinical guidelines, they also publish a list of research questions they would like to see prioritized. These questions are tightly focused on clinical relevance, they are well-defined and they are currently unanswered in the clinical literature.
> 
> Every few years NICE reviews the clinical literature, checks if their recommended studies have been run and, normally, move on disappointed.
> 
> It's not hard to design studies that answer NICE's research priorities. These studies wouldn't be unusually difficult to do. But somehow the studies which NICE claim would affect the clinical care they recommend UK hospitals provide do not get ran.

My claims were based on having read through a few of NICE's guidelines and having compiled some of their recommendations for research into a post. But, this basis was anecdote not data.

The claim I maked in my comment was empirical. There is no need for guess work; we can simply check how often NICE's recommended questions actually get answered by looking at the numbers.

This repo is my quick attempt to get a sense of how often NICE's recommended questions have been answered.

## Where did this data come from?

I went to these urls:
- https://www.nice.org.uk/about/what-we-do/science-policy-research/research-recommendations
- https://web.archive.org/web/20170716190227/https://www.nice.org.uk/about/what-we-do/science-policy-research/research-recommendations

At each respective webpage, I selected everything and then pasted it into VSCode.

Using VSCode I performed the following operations:
1. Removed preamble and postamble. I only wanted the relevant data.
2. Removed the text that follows the tab character. These instances were found using the regex '\t.*\$'
3. Removed the lines that didn't contain the regex '[a-zA-Z]\*\d\*/\d\*'. These were found using the regex '^((?!^[a-zA-Z]\*\d\*/\d\*).)\*\$\n'

The data was then ready for automated processing.

## What are the results?

Of the 1067 unique recommendations given in 2017, only 90 are no longer recommended.

Questions can be un-recommended for many reasons including both that the question has been answered and that the question is not longer interesting. If we assume that all of the questions NICE recommended in 2017 and no longer recommended now were removed because the appropriate research was performed, then that still would suggest only 11.6 percent of the questions have been answered.
