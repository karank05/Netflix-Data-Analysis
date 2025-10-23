# Movie Database Analysis


This is a personal project where I explored a movie dataset (mymoviedb.csv) with over 9,800 entries. The main goal was to practice my data cleaning and analysis skills using Jupyter Notebook. I cleaned up the raw data, transformed a few columns, and then used visualizations to find some interesting trends.


# Tech I Used

Jupyter Notebook, 
Pandas (for all the data cleaning and manipulation), 
NumPy, 
Matplotlib & Seaborn (for making the charts)


# The Data Cleaning Process
  
The original data was a good starting point, but I had to do a few key things to make it ready for analysis:
Loaded the Data: Pulled the mymoviedb.csv into a Pandas DataFrame.
Dropped Unused Columns: I removed Overview, Original_Language, and Poster_Url to keep the dataset focused on what I wanted to analyze.
Fixed the Dates: The Release_Date column had full dates (YYYY-MM-DD). I converted this and extracted just the year since I was more interested in year-over-year trends.
Handled Genres: This was the most important step. The Genre column had multiple genres in one string (e.g., "Action, Adventure, Science Fiction"). I split these strings and then used the explode() function to create a new row for each genre associated with a movie. This lets me accurately count how many times each genre appears.
Categorized Votes: The Vote_Average was a number, but I wanted to see broader categories. I used pd.cut() to group all movies into four bins based on their ratings: not_popular, below_avg, average, and popular.
Final Cleanup: After exploding the genres, I dropped any new NaN values to make sure the dataset was clean for visualization.


# Key Findings

After cleaning the data, I made a few plots to answer some questions:
01: What's the most frequent genre?
Drama is the most common genre by a wide margin. It appeared over 14% of the time.
02: What do the vote averages look like?
The data was split pretty evenly, but 25.5% of the movies fell into the top 'popular' category.
Digging deeper, Drama was also the most common genre within that 'popular' group, accounting for over 18.5% of the top-rated films.
03: What are the most and least popular movies?
Highest Popularity: "Spider-Man: No Way Home" (Action, Adventure, Science Fiction)
Lowest Popularity: "The united states, thread" (Music, Drama, War, Sci-Fi, History)
04: Which year had the most movie releases?
According to the data, 2020 was the year with the most movie releases.


# How to Run This Project

Make sure you have Python, Jupyter, pandas, matplotlib, and seaborn installed.
Place the mymoviedb.csv file in the same folder as the Jupyter Notebook.
Run the notebook cells to see the full analysis!
