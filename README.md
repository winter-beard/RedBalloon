/* # RedBalloon
Data analysis of scraped job listings from "anti-woke" job search engine RedBalloon

This was my first attempt at scraping beyond the class homeworks and it took me a while to figure out that the bulk of the part of the site I was interested in was coded in JavaScript - not HTML. With help from Harsha and Jeremy Singer-Vine I was able to pull the contents of all 830 ads on RedBalloon and then get them from JSON into a dataframe. This required using regex to pull html terms out of the columns and the json.normalize function as well. I was also able to change the framework I used to loop through all 83 web-pages and pull every ad - initially my code was just pulling one per page. The dataset I got from this was rich with good data but from here I think I struggled a bit going in with only a fascination of the concept of a conservative job website instead of an angle. 
#Analysis/Methods 

#1
I first focussed on how few of the jobs were not remote - a sharp contrast to a Pew Research study I found on the general US workforce, I used Datawrapper. To finish the comparison to the US workforce overall I looked at how salary levels compared overall to the median wage. For this I used Figma2HTML but not sure I loved every second. 

#2
DeSantis' Super PAC

For this I installed Python's nltk package and the scikit-learn as well. I got the idea of how to do this from a GitHub repo that analyzed most common words on Democratic and Republican subbreddits. I used a pre-installed package of stop-words and also added weird number patterns I found in my first running of the program later. I used the CountVectorizer function to pair words that were found together 80% of the time and showed up a minimum of 8 times. I initially thought this output would be good for a word cloud or bar graph but it was actually a bit boring. For here I scrolled through the words and tried to find ones I thought I could pair in a list to then identify a subset of different types of businesses. My initial takeaway was how interesting that Ron Desantis was mentioned lots but Trump only once. So I created a df of all the jobs that mentioned Ron Desantis and the one that mentioned Trump (which was actually for a media org that Donald Trump Jr co-founded(MxM). This lead me to hone in on ads placed by DeSantis' super PAC 'Never Back Down'. Upon researching I realized that the ads themselves might be newsworthy in the context of the increasingly fuzzy line of what constitutes coordinating with a campaign directly - prohibited by the FEC but seemingly unenforced. I created a graphic in ai2html and several maps using techniques Aaron taught us to get coordinates into geojson and then onto Datawrapper. I had wanted to place the points on a premade map of the 2020 election results to see if conservatives were posting from liberal places out of isolation or if they were in largely conservative areas. Unfortunately I could not get DataWrapper to accept either a geojson file I built in the command line or one I downloaded from the NYT github. I would still love to figure out why because I think it would have tied together everything together but alas. In comparing DeSantis' job postings to Republican Jobs' a GOP stalwart organization less linked to any one candidate - it's clear DeSantis' focus is on South Carolina and New Hampshire both early primary states that are his only real chance in gaining momentum against Trump, who is not advertising on the site and perhaps either more focussed on his legal battles and less on campaign organizing or just not using RedBalloon for canvasers. 

#3. 

Christian businesses. 

Because I had interviewed one man who advertised on the site for someone to work at his Texas cable business on how he had heard about it and why he advertised, I wanted to include the site's strong Christian business component. He was definitely weirded out by my call but it was clear he thought Christians like him were hard-workers and he was really short-staffed and willing to give it a try. He had yet to hear from anyone because of the ad but said he had only posted a week earlier. I wanted to map all the Christian businesses to see if they fell along the historic Bible. Compared to the overall map of businesses it represented a large proportion of of the non-coastal job postings A decent percent of businesses on the site identified as "faith-based" or had "Christian values" mentioned in their job summary and I pooled them together using the same analysis technique as I did for the political candidates and it's clear that the evangelical and conservative identies are deeply intertwined. I worry my three areas of focus are somewhat unrelated and I probably should have just picked one of the three but I have a habit of getting a bit carried away with large datasets. 


Sources:
-Scraped site: https://www.redballoon.work
-Pew Research: https://www.pewresearch.org/social-trends/2023/03/30/culture-of-work-methodology/
-Median Wage value: https://www.nationwidevisas.com/usa-immigration/average-salary-in-usa/#:~:text=The%20median%20salary%20is%20%2489%2C000,earn%20more%20than%20the%20median.

Analysis sources:
-Map I made but could not use: https://github.com/tonmcg/US_County_Level_Election_Results_08-20/blob/master/README.md
-Map I wanted to use: https://www.nytimes.com/interactive/2021/upshot/2020-election-map.html
-Text analysis: https://github.com/jreynolds999/NLP-Reddit-Classification

New skills:
-regex data cleaning
-WebScraping esp pagination
-Figma2html
-ai2html
-Mapping on Datawrapper using MyMaps on Google to create coordinates
-pd.to_csv
-text analysis using CountVectorizer and nltk <3

/*

