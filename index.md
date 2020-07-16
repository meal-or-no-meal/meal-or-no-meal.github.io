---
title: Meal Or No Meal
description: The Meal Planner / Grocery Lister Extraordinaire!
layout: default
---
## Team Members
#### Paul Cutter
#### Mickie Morlang
#### Levi Sanchez
#### Ambar Rodriguez


## Summary

Meal planning is the best way to create healthier meals on an ongoing basis. 
It can also help to save money and reduce food waste. The trade-offs are often the time it takes to create
 shopping lists, frequent trips to the store, or eating the same meals over and over. Meal Or No Meal helps 
 make the process of meal planning easier and, dare we say it, fun! The application allows users to choose from 
 a wide variety of meals, share meals they've created, and add them to a calendar. For the indecisive eaters, 
 Meal Or No Meal can also randomly populate the user's calendar with meals. Say _"So long!"_ to that pesky
  task of creating a shopping list by using our Generate Shopping List feature based on the user's planned meals.
   Users can welcome food-planning back into their life and take it to the next level with Meal Or No Meal. 
 


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
