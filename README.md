# Software Development 

Repo for the IA

1. [Planning](#Planning)
2. [Design](#Design)
3. [Development](#Development)
4. [Evaluation](#Evaluation)

# Planning 

### Defining the Problem 
My client is currently facing a problem of having to think of what to cook for every meal; breakfast, lunch and dinner, for her family, everyday. Especially in the current situtation of covid-19 pandemic, everyone in her family members now stay in thier house for the whole day, therefore she needs to cook three meals for the whole family member. My client is in need for something that can help her with coming up with different menus for every meal. She doesn't want to cook the same thing everyday, although she is having trouble coming up with non-repetitive menus. Furthermore, she also wants her family to eat healthily, with balanced nutrition. In short, my client is in need of a way to come up with different but healthy menus for every meal, every day, without having to experience any stress.

### Solution Proposed
The solution for the problem stated, is the "Menu Search App". This software should allow my client as well as other people who have the same problem, to live a better, stress free life by eliminating the job of thinking of a menu. This software basically shows different menus depending on different information the user inputs into the app. The user can type in keywords, select a theme, etc. to search for the menu they want, and that software should return different list of menus that correlate with their requirements. When the user selects a menu they prefer, it should show the recipe along with the nutrition information, and in that way, they don't have to go to another platform to search what ingredients they need or how much of what they need and so on. Also another objective of this app is to allow people to cook different menus every time, therefore it has to have a system where it tells the user that the menu was used the day before, to prevent from cooking the same meal. This is the general idea of the app, and in addition to all of this, the app needs to be easy to use, since my client is not computer fluent. The app should be simple enough for the users, that once they open app they should immediately know how to use the app. 

### Success Criteria 

1. User can search for a menu by typing keywords (ex. chicken, tomoato, etc.)
2. User can search for a menu by selcting the theme (ex. Japanese, Chinese, etc.)
3. It should show several different menus as a search result
4. It should show the name, photo and a small description of the menu
6. Users should be able to see the nutrition information of the menu (ex. kcal)
7. It should show the recipe of the menu 
8. When the same menu has been selected it should tell the user that the menu has been used recently
9. The app has a secure login system

### Justification of tool

Pycharm will be used throughout the entire process of the development. IDE makes the development of the app easier and more efficient than the online platform. The reason for this is because IDE allows us to create multiple files unlike the online platforms. This helps the developers keep track of the program development, especially when creating less simple programs. The programming language that will be used mainly throughout the development is python. Python offers a more simple syntax comparing to other languages, and it is developer friendly. In addition to this, because of its less strict syntax, the process of debugging may not be as difficult as others. For these reasons, these tools will be used to develop this app. 

# Design 

### Skecth of the app
![Appsketch1](appendix/MenuAppSketch.png)

This is the very first sketch of the app. It has the login page, registration page, home page (including search box, buttons), results page, and a description page. These are the main pages that consists the app. All the arrows the image indicate which button redirects the user to which page. For example the "create account" button on the login page, would redirect the user to the sign up (registration) page. In the registration page, the user will have to type in their email address, username, and password twice, just to make sure that the user has no mistake in their information. In the login page, it requires email address, and password. If they type in the valid information for both, they will have access to the search page. In the search page, there are two types of user inputs the app can take: keywords or buttons. In the search box, the user can type in keywords, and the app should show the results of the menus that is related to the keyword. Also another way of looking for the desired menu is by tapping or pressing on the button which says "Japanese", "Chinese", etc. If the user wants to cook a Japanese menu, they can go to the "Japanese" button, and see what menus there are. On the results page it will show a list all the menus that corresponds to what the user is looking for. On the list it should show the name, photo, and a brief description of the menu, so that the user has a better idea of what the menu is. Finally in the description page, it should show all the nutrition information, and the recipe of the menu. The recipe should be very easy to follow, even for people who don't know how to cook. It should include everything: how much of what ingredients they need, and the procedures to cook them. This is the first sketch of the app, and the sketch will be updated as I have a meeting with my client to confirm and improve any components of the sketch.

### Update of the sketch 


# Development 

## Secure Login System 

 In this app, the users will need to be able to log into there own page. One of the function of this app is that it should remember what the user searched before. Therefore there needs to be a page that is dedicated only to the user themselves. This is why the app needs a secure login system; to make sure that other users don't mess with other people's accounts.
 One of the requirements for the secure login system is that it is very clear for the user. There are few boxes for the users to type in their personal information, and these boxes should indicate very clearly which information should be entered where. This is what the login and sign up page look like: 
 

## Creating a database

The most crucial part of this software is the searching function. One of the main purpose of this software is for the user to search random menus, to give them ideas of what they can make for their meals. To restate the requirement, when the users types in keywords, they should be able to access menus corresponding to those keywords. In order to create such search engine, first we need data. The data in this case would be the necessary information about the menus.
The method of this "search" procedure should be something like this:

1. When search button is pressed, it reads the keyword the user typed in
2. At the same time, access the csv file with prestored data 
3. Look for matches in menu names, and ingredients
4. Show the results 
5. If no match show "no match" on screen 

### Creating a csv file 

Creating new informations about the menus are very time consuming, since in this case, we need to have many range of menus, so that the user has something to choose upon. Therfore instead of creating a new database by myself, I decided to get data from different websites. In this way it is more time efficient, and I will able to load many different menus very quickly. For this, I used a method called Webscraping. Webscraping is basically the skill of skimming through different websites and getting the only informations you desire. To do this we use the html of the website, and indicate which tags we want to extract from the website. This is the basic for accessing a website in python:
```
import requests

allRecipes = requests.get("https://www.allrecipes.com/recipes/1947/everyday-cooking/quick-and-easy/?page=" + str(page))
```
This code is essentially requesting access to the website. If we print this result it would give codes such as `Request[403]` or `Request[200]`. 403 is an HTML status code, which basically means "forbidden". If it returns 403, this means that the website has denied access, because of some reason. On the other hand, 200 is another HTML status code, which means "Request successful". The code aboce sucessfully returns 200, which means that access permission was granted. If this is okay, then the next step is extracting the desired information using html tags. 













