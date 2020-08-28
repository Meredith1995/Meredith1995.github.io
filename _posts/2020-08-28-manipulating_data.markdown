---
layout: post
title:      "Manipulating Data "
date:       2020-08-28 17:31:12 +0000
permalink:  manipulating_data
---


My first project for Flatiron school provided its fair share of challenges. As a novice coder, it was intimidating to begin the process of cleaning the data and creating visualizations through Python. One particular problem that I faced was parsing out the genres for each movie and connecting them to the popularity of that movie. I wanted to see what genres were included in movies with the highest popularity score. 

The first challenge I faced with the data that was provided, was pulling out each individual genre from the genres-id column and making it into its own column. I had no idea where to begin. However, through some googling I found a function that made sense to me and I thought could work. The function iterates through the genres column, splits each genre-id at the comma, and creates a dictionary with the key being the movie id and the value being the genre-id. This dictionary is appended to a dataframe and then grouped by id, sliced by the value and counted using value-counts. Finally it is unstacked and null values are filled with 0. This results in a dataframe where each genre-id is a column with 0 or 1, depending on if it is present in a particular movie. 

With the first hurdle overcome, I moved onto making the dataframe readable and combining it with the original dataframe. All of the genres were as numbers and I had to rename each genre-id with its correlating genre. I deleted the genre column from the original dataframe and then combined both dataframes using an outer join on their indexes (which I made sure were both the id column). Finally I had a completed dataframe with each genre as its own column, with either a 1 or a 0 depending on its presence in a movie, along with a correlating popularity column. Next I had to move onto visualizing the data. 

As I moved onto thinking about how to visualize the data, I decided I wanted to make a boxplot for each genre that showed the distribution of popularity scores correlated with that genre. I realized that I would have to make an individual dataframe for each genre because I did not want to include the value of 0 in the boxplot, so I made dataframes for each genre where the only rows present were those with a value of 1. Then I created side-by-side boxplots to compare each genre. I made sure that they all shared the y-axis so that the scale would be the same for each. Through my visualization I could see that the Action and Adventure genres had the best distributions of popularity scores. 

Throughout this process there was a lot of frustration and a lot of googling. As I go back and write it down the process seems straightforward and simple, but in the moment it was complex and often very difficult. As my skills and understanding improve, I hope to be able to face challenges with more confidence and tools in my pocket. I’m satisfied with what I accomplished, but I hope that in the future I can accomplish more with more beautiful code and thoughtful visuals. 

