---
layout: post
title:  "2. Creating my CLI app WeatherWear"
date:   2017-06-05 22:29:43 -0400
---

![](http://i.imgur.com/iHoWVbc.png)


These past few days I have been focusing a lot of attention on finishing up my WeatherWear CLI app. Today it is in a condition that I am currently satisfied with.
My original intentions were to create a CLI app that would retrieve the current schedule, scores, standings, and team player roster for any team in the NHL or NBA. However, I grew disinterested in the idea as it seemed rather repetitive work. I then settled on the idea of creating an app which would retrieve today's weather and recommend an outfit for you. (Upon further later research, there's actually a site called 'dailydressme.com' which does this - and more, but oh well!)

So, though I finally set to work on this about just about 10 days ago(?), I only really came upon my first issue on the URL scraping from weather.com. I had trouble passing an argument into a url that was retrieved from the user's input into the CLI and stored in the variable 'zipcode'. Zipcode would be passed into https://weather.com/weather/hourbyhour/l/(zipcode):4:US. I tried to directly pass it into the open_uri through string interpolation but this did not work. I then split the URL into four different parts, set them equal to an array, converted the array to a string, and utilized it in opening and scraping the webpage. However, as I am writing this I figure it would have been much easier to just use string interpolation to store the user's desired zipcode into a variable which would be scraped with open_uri. Logically, I assume it would but definitely will have to revise that. In any case, this hurdle was passed and I was successfully able to retrieve the current temperature, precipitation percentage, and wind for any given URL that was input by a user. 

After this, I worked on cleaning up the variables between classes, setting class inheritance to assure that the proper information was available, and finalizing the flow of the program between different files. Intially I had a very simple flow which went from the CLI.rb file in which the user was inputting the zipcode and then into the scraping file - so as to retrieve the current weather for a particular zipcode and display it to the user. 

From here, I built up the interactive portion between the program and the user. I fixed the logics for the if/else weather recommendation statements. The if/else statements went from temperature (as the outermost layer) into precipitation and finally wind. Based on this, I input some statements that had fabric, color, and layer recommendations based on the weather. This is something that, in the future, I could make very intricate and interactive. Ideally a weather clothing recommendation program would allow the user to answer some quick questions and formulate a few outfit recommendations - this might even go a step further than that of 'dailydressme.com'! In any case, for my purposes this was working appropriately.

I then decided to actually make specific suggestions to a user and built another level into the scraping / program. Users would be able to see, if they responded yes, to specific pieces of clothing (curated by yours truly). 
Options included tops, bottoms, dresses, shorts, and outerwear (which was only displayed if the temperature was under 50 degrees F). I chose J. Crew from which to display both men's and women's clothing. (Side note: would love to somehow launch the URL for the user or display the image of the product upon selection).
I scraped the specific product pages and returned the name and URL of the product for the user. 
Building this component was terrific! (Basically because I just got to online shop for a few hours =) )


The last parts of this I worked on was to essentially clean up the CLI, see if I could restructure any methods, fix any loops, and run through different variations of the program to ascertain that everything was, indeed, displaying properly.

The few things I would like to improve on in the future *regarding this project*:
1. Add in more interactive CLI
2. Restructure if/else statements for temperature, wind, precipitation, to more appropriately make a recommendation.
3. Scrape different websites and display more elements of the product description.

The few things I would like to improve on in the future *regarding projects such as this in general*:
1. Plan out more carefully the progression of the program prior to starting the project.
2. Refactor methods as I go to make the code more tight.
3. Commit to GitHub more...

- YK
