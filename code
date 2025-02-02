# Importing pandas and matplotlib
import pandas as pd
import matplotlib.pyplot as plt

# Read in the Netflix CSV as a DataFrame
netflix_df = pd.read_csv("netflix_data.csv")

print(netflix_df)

# Step 1: Filter the data for movies released in 1990s Release year should be >= 1990 and <= 1999

movies_all = netflix_df[netflix_df["type"] == "Movie"]

movies_decade = movies_all[movies_all["release_year"] >= 1990]
movies_decade = movies_decade[movies_decade["release_year"] < 2000]

print(movies_decade)

#Step 2: Find the most frequent movie duration

plt.hist(movies_decade["duration"])
plt.show()

duration = 100

# Step 3: Count the number of short action movies from the 1990s

movie_genre = movies_decade[movies_decade["genre"]=="Action"]

short_movie_count = 0

for index, movie in movie_genre.iterrows():
    if movie["duration"] < 90:
         short_movie_count = short_movie_count + 1

print(short_movie_count)
