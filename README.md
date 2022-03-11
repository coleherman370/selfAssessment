# Assessment

## Tl;Dr
I had an amazing team and felt that we made great product.

## Self Assessment

My role in the project was primarily ETL. I found the original datasets that were used. I did not perform the data cleaning on our sets. Instead what I focused on was the transformations of the data so that it could be used within our site. This means that I wrote the first draft of our machine learning and wrote the functions that were used to transform the cleaned dataframes into the csv and json files that were called on for our recommendation engine and charts. I did this by writing a library of sorts titled chart_data_cleaning.py which contained functions that were called upon in our data cleaning notebook titled databases.ipynb (I did not write this notebook).

In addition to that I performed the role of director for project that identified what we needed to accomplish next and task assignment. While I did not write any of the HTML or JavaScript, I helped troubleshoot errors or troubles our group ran into here and assisted with the logical process of the data cleanup.

My greatest challenge in the course of this project was getting the genre data tables pulled together in the correct format. The first struggle I came across here was that the column of data we had for this in our datasets was stored as a string that appeared to a list. At first I thought it'd be easy since it looked like a list but was actually stored as string. When I found that wrapping it with list() created a list with the string split by character. So I tackled this string with the following steps. 

- Removed brackets and apostrophes from the string
- Created list from the string with the split at the comma

But what I really needed was a count of how often each genre showed up in each list. So it was time to write up a nested for loop within the string conversion for loop.

- Loop through each list
- Create a column on the dataframe for each genre if it did not exist
- Apply a counter value of 1 if genre was in list
- Identify the top 5 genres in our Anime dataframe
- Normalize the genres across the different platforms
- Group by genre and count values
- Merge all platform dataframes into one

The ironic thing about this particular csv is that going in I thought it would be a cake walk. But between the handling of the string and identifying/handling all of the different genre titles (like Netflix having Action split into TV Action and Action), this csv proved to be way more challenging and mentally exhausting than any other piece I worked on.

## Team Assessment

I will start off by saying every team member was amazing. This was not one of those projects where any individual didn't carry their fair share of the weight. I would honestly say that it felt as though every individual carried the 25% share.

### Adam

Adam wrote the cleaning notebook script for our project in it's entirety. Within the first week he had written the core of the data cleaning, normalization, and merging of our data. This was huge because it gave the entire team a strong place to work from on everything else. As each member worked on their piecces Adam incorporated new elements into his notebook and reproduce fresh datasets for every need we found as the project went on. When we found we needed to remove stop words from descriptions, Adam incorporated this into his script flawlessly. When we discussed data exploration and charts, Adam broke the data down and produced charts that gave us a jumping off point for what ended up on the site. Possibly most important, Adam found the most popular anime genre that we needed to remove from the set.

### Diana

Diana organized our github for the project and did most of our development and formatting of our HTML code. We did not know exactly what the project's final project would look like in the beginning and then one Sunday we saw that Diana had pushed some HTML to github. We took a look to see what she had pushed. To say we were excited and blown away would be a bit of an understatement. It practically looked like a finished product and had us all convinced we could really pull this off. She did not stop there. Diana figured out and incorporated possibly one of the most most important pieces of the site which was our search engine piece. We were really weren't sure how to do this part but to see it done solidified that we could pull our project together.

### Elena

Elena literally had her hand in just about everything. While I wrote the proof of concept of our sentence embedding ML, Elena took that and fully fledged it out to make it worth something. She completely scripted the ML out so that it took our data in, found the top five anime matches for all of our live action shows/movies, and produced the json we used to display the data on the site. She built the JavaScript charts in our site and helped with the formatting in the HTML. She assisted Adam with parts of the data cleaning whenever he struggled with some of the weird Python issues. To sum up Elena's role in the project, she was an every trick pony that glued everything together.

### Project

I am very proud of our project. Are there things I wish were better? Of course. But seeing what we pulled together in a month is more than what I initially thought my project would end up being by the end. So on to the summary:

Our project is a recommendation engine and data presentation with the goal of assisting people find their way into watching Anime. We started with idea of exploring how Anime presence has grown over the last few years. The evolved into tackling the challenge of taking shows that people watch on the major platforms to find animes that would be a good entry for them. We decided to do this by finding Animes by the description of a show they select. There's some improvements I intend to make to take this further. But our model does make seemingly accurate suggestions and that was our goal.

In addition to the recommendation engine, we provided various data charts to help viewers explore and see more data that may raise their interest in anime or even just find a one they want to start watching with the scatter plot.
