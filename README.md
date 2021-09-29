# privacy
Mini project involving performing a text analysis on 11 website privacy policies.

Excerpt from a paper I wrote about this project. Read it in full [here](http://blogs.harvard.edu/veronicanutting/category/privacy-and-technology/privacy-policies-analysis/).


##An Analysis of the Privacy Policies of “Back to School” Websites 

#Aim:
To compare the privacy policies of various websites I used in the first two weeks of school to purchase back to school supplies or otherwise use a related service.

#Methods: 
I made a list of the websites I had visited for “back to school” reasons. I chose this subset of websites because (1) I have recently visited them, (2) I had a particular non-entertainment-related reason or need to visit them, and (3) I think my peers may have visited similar sites. Then I searched for their Privacy Policies, copied the policy texts into .txt  files, and saved them locally on my computer. Links to all the Privacy Policies are available in the Appendix and all the .txt  files are available on the GitHub repo linked below.

Originally, I intended to build a tool that would take in a link or PDF file and scrape the text directly from there. However, I discovered that there was significant variation in the page structures which would make such scraping for different websites difficult. Since I did not want to limit the scope of my analysis only to websites with policies structured in a way I could easily scrape, I opted to copy and paste the texts into .txt  files. This step can be reproduced by visiting the linked privacy policies and copy-pasting their main bodies of text into .txt files

I then wrote some Python code to process the text of each policy. I used a Jupyter Notebook to facilitate the text analysis. First, I calculated overall metrics of each text like its line count, total words, and total unique words. Then I calculated various readability and time metrics using textstat.

In the second part of my analysis, I “cleaned” each text. This cleaning allowed for a more rigorous analysis of the frequencies and counts of words. For each policy, I removed punctuation marks and made all the words lowercase. Then I used a lemmatizer to remove plural suffixes from words. Lastly, I remove “stop words,” which are commonly used words in English like “the” and “and.” I got a list of such “stop words” from the nltk  library I used. 

After cleaning the text, I conducted my overall analysis on it. I also found the longest and the most common words in each policy. The “cleaning” allowed me to find the most common words that aren’t “the” or other “stop words.” 