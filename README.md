# ETL-Project

## Overview
Timeline: 1 week
Number of participants: 3

Goal: To demonstrate ETL processes commonly used in data science, specifically in data warehousing.

## Proposal

We found two datasets based on the popular show "The Office" which we decided to use for this project. Our goal was to see if IMDB ratings were more popular because of certain characters having more lines.

## Steps
# Extraction
The Office IMDB Per Episode data set has the following columns: season, title, air date, rating, number of votes, description of the episode, directed by, and written by.
* From this, we only extracted season, title, and rating.

The Office Lines data set has the following columns: season, episode, title, speaker, and line.
* From this, we only extracted season, title, episode, and speaker.

# Transformation
At face value, we thought the data looked clean and we could easily join the tables. However, once we studied the data a little further, we found that there were a lot of character names that were repeated or spelled incorrectly (meaning duplicates). The titles also had differences in the way they were written out.
* We corrected the differences in Jupyter Notebook and then moved on to the load process.

# Load
In MongoDB, we created the appropriate tables and then did a left join. We completed a few queries and found that there really wasn't any real correlation with a character having more lines and the IMDB rating of that episode.
