---
title: "Next Word - Capstone Project JHU"
author: "Saurabh gupta"
date: "4/18/2020"
output:
  ioslides_presentation: 
    keep_md: yes
  slidy_presentation: default
---



## Objective

This presentation pitches the Next Word app including an introduction and use to the application user interface and details about the prediction algorithm.
The Next Word Predict app is located at:

<https://bodhi1606.shinyapps.io/capstone/>
The source code files can be found on GitHub:

<https://github.com/bodhi1606/Capstone-Data-Science-JHU>

The purpose behind the app is to make typing, user friendly and fast by giving suggestions to the user about the next word. The app is made by using natural language programming alogorithem.

## Next Word Application

- Next Word is a Shiny app that uses a text prediction algorithm to predict the next word(s) based on text entered by a user.
The application will suggest the next word in a sentence using an n-gram algorithm. An n-gram is a contiguous sequence of n words from a given sequence of text.
- The text used to build the predictive text model came from a large corpus of blogs, news and twitter data. N-grams were extracted from the corpus and then used to build the predictive text model.
- Various methods were explored to improve speed and accuracy using natural language processing and text mining techniques.

## Prediction Model
- The predictive text model was built from a sample of 800,000 lines extracted from the large corpus of blogs, news and twitter data.
- The sample data was then tokenized and cleaned using the tm package and a number of regular expressions using the gsub function. 
- As part of the cleaning process the data was converted to lowercase, removed all non-ascii characters, URLs, email addresses, Twitter handles, hash tags, ordinal numbers, profane words, punctuation and whitespace. 
-  The data was then split into tokens (n-grams).
- As text is entered by the user, the algorithm iterates from longest n-gram (4-gram) to shortest (2-gram) to detect a match. The predicted next word is considered using the longest, most frequent matching n-gram. The algorithm makes use of a simple back-off strategy.

## User Interface

The predicted next word will be shown when the app detects that you have finished typing one or more words. When entering text, please allow a few seconds for the output to appear. Use the slider tool to select up to three next word predictions. The top prediction will be shown first followed by the second and third likely next words

![User interface](E:/JHU Data Science/Capstone/Presentation/Screenshot (3951).png)
