<!-- This is the markdown template for the final project of the Building AI course, 
created by Reaktor Innovations and University of Helsinki. 
Copy the template, paste it to your GitHub README and edit! -->

# Dinner Recommendation Finder

Final project for the Building AI course

## Summary

The goal is to get recommendation for dinner recipies based on food you have at home. It should give recommendations based on liked recipies and, for variation, recommend new dishes as well.


## Background

Which problems does your idea solve? - It should solve the problem of always buying new food, before using the things we already have at home, and also help deciding what to eat (especially after a long day at work)
How common or frequent is this problem? - This is a daily problem, as people need to eat everyday. Also wasting food is a common problem nowadays.
What is your personal motivation? - My personal motivation is, that I never know what to cook and how to use limited ingredients, without going grocery shopping everyday
Why is this topic important or interesting? - Personally it would be an important topic for me, but would be an interesting topic in general


## How is it used?

The app should be be able to get input about the available ingredients. Based on this, the application should recommend recipies to the user. The app should also learn what preferences the user has, and should take that into account when recommending something (but should not be limited to only the preferences). Ideally, the app should recommend around 5 dishes with at least one new dish (meaning it is not in the prefered category). It is also important that the user is able to give "no-go"-ingredients, to filter out any recipies with disliked or allergic food. 
In case the available ingredients list is not matching any recipe, the application should recommend recipies with the least amount of ingredients to buy.


## Data sources and AI methods

There are three kind of data which the application uses.
1. User Data: which mainly include available ingredients and preference. Both of these must be able to be updated any time
2. Recipe API Data (with ingredients list): This is for searching the recipe which has an ingredients list closest to the available ingredients and includes the preferences of the user
      --> recipies can be taken from recipe websites (i.e. [Chefkoch-API](https://github.com/VinzSpring/Chefkoch-API) by [VinzSpring](https://github.com/VinzSpring)
3. Additional Recipe Data: This includes recipe the user created themself.

As for the AI methods, I would suggest that a combination of nearest neighbour and TF-IDF should be used. Recommended dishes based on preferences should use both and an additional recommendation outside of preferences (not food preferences, but more like type of food, i.e. italian, indian etc.) should only use TF-IDF to find the closest ingredients list

## Challenges

The application does not include the utensils one might need for cooking a recipe. It could also be a challenge, that the chosen ingredients by the user do most likely not include "common" ingredients (i.e. Salt, Water, Flour etc.), but are included in recipies. This could distort the actual output.

## What next?

Using API and implementing everything into an functional application is a challenge in itself, for someone that does not programm on regular bases. This means, that I have to first study about the basics of creating an application and the use the learned AI methods in the newly created environment


## Acknowledgments

* [VinzSpring](https://github.com/VinzSpring) for Chefkoch-API
