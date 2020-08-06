---
title: Meal Or No Meal
description: The Meal Planner / Grocery Lister Extraordinaire!
layout: default
---
## Team Members
#### Paul Cutter
_Meal Creation, Scheduling, Wireframes_
* [Email](pcutter@gmail.com)
* [Github](https://github.com/pcutter1)
* [LinkedIn](https://www.linkedin.com/in/pqcutter/)
#### Mickie Morlang 
_Calendar Component and SignIn/Auth_
* [Email](mickiemorlang@gmail.com)
* [Github](https://github.com/mmorlang)
* [LinkedIn](https://www.linkedin.com/in/mickie-morlang-78a243185)
#### Levi Sanchez
_Back End, Ingredients, Styling_
* [Email](levijames@gmail.com)
* [Github](https://github.com/levisanchez)
* [LinkedIn](https://www.linkedin.com/in/levi-james)
#### Ambar Rodriguez
_Navigation, User Entity, Styling_
* [Email](rodriguez.ambar1@yahoo.com)
* [Github](https://github.com/amberrz)
* [LinkedIn](https://www.linkedin.com/in/ambar-rodriguez-9014571ab/)

## Summary

Meal planning is the best way to create healthier meals on an ongoing basis. 
It can also help to save money and reduce food waste. The trade-offs are often the time it takes to create
 shopping lists, frequent trips to the store, or eating the same meals over and over. Meal Or No Meal helps 
 make the process of meal planning easier and, dare we say it, fun! The application allows users to choose from 
 a wide variety of meals, share meals they've created, and add them to a calendar. For the indecisive eaters, 
 Meal Or No Meal can also randomly populate the user's calendar with meals. Say _"So long!"_ to that pesky
  task of creating a shopping list by using our Generate Shopping List feature based on the user's planned meals.
   Users can welcome food-planning back into their life and take it to the next level with Meal Or No Meal. 
 
## The Motive

The base motive behind the want or need for a meal planning application is universally human. 
We don't believe there's a single person out there who hasn't at some point in their life wondered
what they were going to eat for their next meal. Beyond that, this application has the potential to
expand to a robust suite of features that can help improve many different aspects of life such as
physical health, financial health, and even emotional health - all of which are in some way connected to
the meals we eat. Spending too much money on eating out? Spending too much time meal-planning? Eating 
too many unhealthy options because of last-minute decisions when you were already hungry?
This app (and what it aims to be) can help with all of that.  

## Key Functional Aspects

There are 3 Key Functional Aspects to Meal or No Meal

First - there's the ability to create/edit/delete a meal and store/retrieve that information from the database.
This will include details such as the Name, Recipe, Ingredients, and Prep Time (in minutes).

Next there's the ability to save a meal to a Breakfast, Lunch, or Dinner slot on the calendar. You can 
select a day on the calendar and view the meals scheduled for that day. Then you can select one of those
scheduled meals and view the details (recipe, ingredients, etc.) of that meal.

And lastly there's the shopping list generator which does - well - exactly what it sounds like it does.
It will generate a list of ingredients based on the meals you currently have scheduled in a certain date
range. This list display will allow the user to check/uncheck ingredients as a visual cue for whether or not
they need to acquire that ingredient. 

## Current State of Meal or No Meal

The current state of Meal or No Meal can be best described as "tween" - that is to say:
It's mature enough to do some chores. It does some chores well, it won't do some chores at all. And if
you ask it in the wrong way- it might give you some sass. 

#### What It Does
What the app is currently able to do:
  * User can create a meal with a Name, Recipe, Equipment Needed, and Prep Time in minutes.
  * Meals can be edited and deleted by the User. 
  * Meals can be stored and retrieved from the database.
  * Meals can be scheduled to a Meal Slot on the calendar.
  * Navigate between Meals, Calendar, and Shopping List with bottom navigation.
    
    
#### Improvements
What we would like to improve:
* High Priority Items

    * INCOMPLETE - Ingredients are not currently being stored or retrieved. They also need to be
    parsed from Strings to Lists of ingredient items.
    * INCOMPLETE - Shopping List does is not currently wired to retreive ingredients and needs date-range
    logic in the query
    * INCOMPLETE - Selecting a meal from a meal slot on the Calendar fragment does not yet display the details of the selected
    meal.
    * INCOMPLETE - Calendar does not currently display the 
    
    
* Medium Priority Items

    * INCOMPLETE - Layout needs to be locked into a vertical mode.
    * BUG - Issue scheduling two meals in the same meal slot needs to be resolved.
    * INCOMPLETE - Unable to remove meals from a scheduled slot
    * INCOMPLETE - Replace EditTexts for Meal Details input with a text popup to improve
    visual aesthetic and user functionality
    
    

## Intended users

* Health Coaches / Dieticians
    > Part of my job is to build customized meal plans for my clients. Having a shareable calendar will help them adhere to their diet and make sure they only buy healthy foods when they shop.

* Busy Parents
    > Planning and prepping meals for the week can be very time consuming. Between raising my kids and my job, I hardly have the time to think a week or two out. I could really use an app that would help take at least one thing off my mental plate.

* The Indecisive Eater(s)
    > My roommate and I can never make up our minds what we want to eat and often put off coming up with a dinner plan until we're already hungry, so we default to eating out. If we knew what we were going to cook ahead of time, we could save a lot of money by cooking for ourselves.

## Client component

* **Functionality**

    User will be able to:
    * Input a name, ingredients and cook time information to 'Create a Meal' that they can then drop onto a calendar in a Breakfast, Lunch, or Dinner slot for any given day.
    * Tag meals as adhering to specific dietary categories such as Gluten Free, Dairy Free, Vegetarian, and Vegan.
    * Upload Meals and Calendars online to share with family and friends.
    * Plan up to a month of meals in advance and see information such as total calorie count for the day based on the planned meals added to the calendar.
    * Generate a shopping list of the ingredients from the meals on their calendar.
    * Save multiple shopping lists
    * Randomly populate meals to their calendar for a specified number of days.
    * Search an online database for Meals or Calendars.

* **Persistent data**

    Persistent data will include:
    * Meals (both downloaded and created)
    * User's calendar(s) (both downloaded and created)
    * Shopping lists
   
   
  
## Server component


* **Functionality**

  The server will be able to allow users to store and retrieve customized meal calendars. It will also allow user to store and retrieve meals and meal information.

* **Persistent data**

    Server side content will include:
    
    * monthly and weekly pre-made meal calendars uploaded by users
      
    * meal profiles which include their ingredients, cook time, health data and tags for dietary restrictions

* **User Instructions**

    * [How to use Meal or no Meal](user-instructions.md)
    *[The Build Instruction](build-instructions.md)

* **External services**

* Google Calendar
   
    * [Google Calendar API](https://developers.google.com/calendar)
    * User will be able to schedule meals for specific dates. 
    
 
 * Spoontacular API
   
    * [Spoontacular API](https://spoonacular.com/food-api/docs)
    * Data interface for recipe and ingredient lists


 * **Entities**
 
   [Entity Relationship Diagram](erd.md)
 
   * [Project Calendar Entity](https://github.com/meal-or-no-meal/meal-or-no-meal/blob/master/src/main/java/edu/cnm/deepdive/mealornomeal/model/entity/Calendar.java)
   * [Project Ingredient Entity](https://github.com/meal-or-no-meal/meal-or-no-meal/blob/master/src/main/java/edu/cnm/deepdive/mealornomeal/model/entity/Ingredient.java)
   * [Project Meal Entity](https://github.com/meal-or-no-meal/meal-or-no-meal/blob/master/src/main/java/edu/cnm/deepdive/mealornomeal/model/entity/Meal.java)
   * [Project User Entity](https://github.com/meal-or-no-meal/meal-or-no-meal/blob/master/src/main/java/edu/cnm/deepdive/mealornomeal/model/entity/User.java)   
   * [Project List Item Entity](https://github.com/meal-or-no-meal/meal-or-no-meal/blob/master/src/main/java/edu/cnm/deepdive/mealornomeal/model/entity/ListItem.java)   

*  **REST Controllers**

   * [Calendar Controller](https://github.com/meal-or-no-meal/meal-or-no-meal/blob/master/src/main/java/edu/cnm/deepdive/mealornomeal/controller/CalendarController.java)
   * [Ingredient Controller](https://github.com/meal-or-no-meal/meal-or-no-meal/blob/master/src/main/java/edu/cnm/deepdive/mealornomeal/controller/IngredientController.java)
   * [List Item Controller](https://github.com/meal-or-no-meal/meal-or-no-meal/blob/master/src/main/java/edu/cnm/deepdive/mealornomeal/controller/ListItemController.java)
   * [Meal Controller](https://github.com/meal-or-no-meal/meal-or-no-meal/blob/master/src/main/java/edu/cnm/deepdive/mealornomeal/controller/MealController.java)
   * [User Controller](https://github.com/meal-or-no-meal/meal-or-no-meal/blob/master/src/main/java/edu/cnm/deepdive/mealornomeal/controller/UserController.java)

* **WIREFRAMES**

    [Wireframes](wireframe.md)
    
* **DDL**
   
   [ddl.md](https://github.com/meal-or-no-meal/meal-or-no-meal/blob/master/docs/ddl.md)   


## Stretch goals/possible enhancements

* Added functionality where you can list the ingredients you have and it will return a list of meals you can cook

* Added functionality which allocates meals with shorter cooking times based on parameters set by user (.e.g. I only have an hour for lunch, so I only want lunch meals to be ones that take 30 min or less to cook)

* Added information about health data (e.g. calories, % daily fiber, etc.)

* Added customization for dietary restrictions (e.g. gluten free meals only, dairy free meals only)

* Link cooking tutorial videos to meals
