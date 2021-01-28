# Predicting Actors Future Success in the Industry

This project is based around a single question: **Can you predict an actor's industry success based on the films they appear in early in their career?**. It would be benificial to be able to advise actor's new to the industry on what type of jobs to look for to maximize their potential for success.

This repo contains presentation slides as a PDF, as well as the notebooks I used to web-scape data and build my model. Data was gathered from IMDB and IMDB-Pro.

### The Notebooks

This project consists of two jupyter notebooks. **actor_generator.ipynb** was used to web-scrape a list of actors and **Modeling.ipynb** was used to web-scrape the film features for my model as well as create the model and my charts.

### Strategy

I defined industry success (my target variable) as their total number of film credits over their career (up to 2020). I only used features from their first three films to try and predict this value.

First, I generated a list of thousands of actors from casts of films from the year 2000. This was to try and get a balance between famous and unknown actors. To be kept on the list the actors must have been in at least three films. The features I gathered were release year, size of cast, and genre.

Next, I trained a linear regression model to predict my target variable from these features.

### Results

The R-squared for this model was ~0.3. This is a relatively low value, showing the high variability and non-linearity between the early films an actor appears in and their ultimate success. Interestingly, the genres most inversely correlated with success were documentary and musical (both genres that are more likely to use non-actors), as well as sci-fi and horror (both less mainstream genres). Animation was most correlated with success, which could be due to the voice-acting industry being harder to break into and that voice-actors tend to have more acting credits than film actors over their career.
