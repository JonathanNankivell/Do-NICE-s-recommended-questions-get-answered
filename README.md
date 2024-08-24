# Do NICE's recommended questions get answered

## What is this about?

In the comments of Experimental History, I made a bold claim:

> > Meta-analyses come out all the time that are like, “Unfortunately, all of the studies that try to answer this important question are so bad that we can’t learn anything from them.” Instead of running another 500 piddling, confounded little studies, someone with guts, taste, and money could run the actually good study.
> 
> The National Institute of Health and Care Excellence (NICE) is a UK body that determines clinical guidelines. When they publish their clinical guidelines, they also publish a list of research questions they would like to see prioritized. These questions are tightly focused on clinical relevance, they are well-defined and they are currently unanswered in the clinical literature.
> 
> Every few years NICE reviews the clinical literature, checks if their recommended studies have been run and, normally, move on disappointed.
> 
> It's not hard to design studies that answer NICE's research priorities. These studies wouldn't be unusually difficult to do. But somehow the studies which NICE claim would affect the clinical care they recommend UK hospitals provide do not get ran.

Seeing as my acusation rests on an empirical question - how often do NICE's recommended questions actually get answered? - I thought it best to look into this rigorously.

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
