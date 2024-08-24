# Do NICE's recommended questions get answered

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
