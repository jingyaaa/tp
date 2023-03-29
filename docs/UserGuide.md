# User Guide

## Introduction
Hey there! Thanks for choosing Meal Companion, your one-stop solution to handling meal prep, ingredient tracking and cookbook! This guide will show you how to get started, and take control of your own meal planning!

Meal Companion is designed by computing students, for computing students, especially those staying in hostels on campus, as a means to track ingredients and get started on their cooking and meal prep journey! Meal Companion provides recipes, as well as the ability to filter those recipes based on the ingredients you have, and many more features!

# Table of Contents
1. [Using this Guide](#using-this-guide)
1. [Getting Started](#getting-started)
2. [Features](#features)
   1. [Ingredients](#ingredients)
      - [Add Ingredients](#add-ingredients)
      - [Remove Ingredients](#remove-ingredients)
      - [List Ingredients](#list-ingredients)
      - [Search Ingredients](#search-ingredients)
      - [Clear Ingredients](#clear-ingredients)
   2. [Recipes](#recipes)
       - [Default Recipes](#default-recipes)
       - [All Recipes](#all-recipes)
       - [Recipe Details](#recipe-details)
       - [Possible Recipes](#possible-recipes)
       - [Random Recipe](#random-recipe)
       - [Check Ingredients for Recipe](#check-ingredients-for-recipe)
       - [Almost Completed Recipe](#almost-completed-recipe)
   3. [Saving Data](#saving-data)
       - [Transferring Saved Data to other devices](#transferring-saved-data-to-other-devices) 
   5. [Help](#help)
   6. [Command List](#command-list)
3. [Conclusion](#conclusion)

# Using this Guide

This guide will introduce you to the basics of using Meal Companion and its current set of features. Here we will briefly explain the types of icons and text you can expect to see, and how to interpret them. 

`Markdown text` like this indicates a command you can input, or a file name. For example, `this is a command you can enter` or `this_is_a_file.exe`. 

Within the `markdown text` you may see segments of text wrapped in `<chevrons>`. These chevrons indicate that this field in the command is a placeholder, to be replaced with your input. For example, a command `add <ingredient>` means you should enter the command `add apples`. 

#### [Back to table of contents](#table-of-contents)

# Getting Started

1. Java 11 is required for Meal Companion to function properly, please make sure your device has Java 11 installed. If not, you may download it [here](https://www.oracle.com/sg/java/technologies/downloads/#java11). If you need further asssistance installing Java 11, you may refer to the [Installation Guide](https://docs.oracle.com/en/java/javase/11/install/installation-jdk-microsoft-windows-platforms.html).

2. Once you have ascertained that your device has Java 11 installed, you may download the `.jar file` [here](https://github.com/AY2223S2-CS2113T-T09-3/tp/releases/tag/v1.0). 

![jar.png](images/jar.png)
<sub>Fig 1: Version release page with download links for Meal Companion.</sub>

Click on `mealcompanion.jar` to automatically download the file. Place the file in a folder of your choice.

3. Open the command terminal and navigate to the folder where you downloaded `mealcompanion.jar` using `cd <file_path>` commands as necessary.
4. Ensure the terminal is within the correct folder.
5. Use the command `java -jar mealcompanion.jar` to launch Meal Companion.
6. When you are finished using Meal Companion, use the `bye` command to terminate the application. This will ensure your stored data is saved correctly for future access.

![startup.png](images/startup.png)  
<sub>Fig 2: Command to start using Meal Companion.</sub>

Meal Companion uses a Command Line Interface (CLI), as the current version is just a proof of concept. We have plans to further develop Meal Companion to include a Graphical User Interface (GUI), or even to a mobile application platform. However as we have not yet reached that stage in our development, the CLI will suffice as the input method to operate Meal Companion. We apologize for any inconvenience caused.

#### [Back to table of contents](#table-of-contents)

# Features
This section will focus on some of the key features of Meal Companion and explain their usage.

## Ingredients
Meal Companion will assist you in tracking the items in your refrigerator, and is capable of adding new ingredients, removing used ingredients, as well as listing the available ingredients in your refrigerator. This guide will detail these features below.

### Add Ingredients
To add an ingredient of a certain quantity to Meal Companion's storage, use the command `add <ingredient> /qty <quantity>`.
The `/qty` portion of the command is necessary for Meal Companion to distinguish between the sections of the command. 
For example, `add ground chicken /qty 300`.

![add1.png](images/add1.png)  
<sub>Fig 3: Sample of Add Ingredients command with user input highlighted.</sub>

### Remove Ingredients
To remove an ingredient of a certain quantity from Meal Companion's storage, use the command `remove <ingredient> /qty <quantity>`. The `/qty` portion of the command is necessary for Meal Companion to distinguish between the sections of the command.
For example, `remove ground chicken /qty 100`.

![remove1.png](images/remove1.png)  
<sub>Fig 4: Sample of Remove Ingredients command with user input highlighted.</sub>

### List Ingredients
In order to show a list of all ingredients currently stored in Meal Companion, use the command `ingredients list`.

![ingredientlist1.png](images/ingredientlist1.png)  
<sub>Fig 5: Sample of Ingredients List command with user input highlighted.</sub>

### Search Ingredients
If you would like to search for a specific ingredient that Meal Companion recognizes as valid, use the command `ingredients search <keyword>`.

![search11.png](images/search11.png)  
<sub>Fig 6: Sample of Ingredients Search command with user input highlighted.</sub>

Omitting the keyword will return a list of all valid ingredients.

![search22.png](images/search22.png)  
<sub>Fig 7: Sample of Ingredients Search command with keyword omitted and user input highlighted.</sub>

### Clear Ingredients
To remove all ingredients from Meal Companion's storage, use the `clear` command.
 
#### [Back to table of contents](#table-of-contents)
 
## Recipes
This segment will go into detail about the recipe features that Meal Companion contains, and the usage of these features.
 
### Default Recipes
 Meal Companion comes included with a list of default recipes already initialized. The list of default recipes are found here:
 1. Beef Burger
 2. Cup of Water
 3. Chicken Burger
 4. Fish Burger
 5. Pasta (Tomato Sauce)
 6. Hainanese Chicken Rice
 7. Mee Goreng

### All Recipes
To display all stored recipes including default recipes, you may use the command `recipe all` to list them.

![recipeall1.png](images/recipeall1.png)  
<sub>Fig 8: Sample of Recipe All command with user input highlighted.</sub>

### Recipe Details
To go into details about a certain recipe, use the command `recipe <index_number>`, using the `<index_number>` from the generated list. 

For example, to view the recipe for Hainanese Chicken Rice, use the command `recipe 6`.

![recipedetails1.png](images/recipedetails1.png)  
<sub>Fig 9: Sample of Recipe Details command showing the output of</sub> `recipe 6` <sub>, the recipe for Hainanese Chicken Rice, with user input highlighted.</sub>

### Possible Recipes
Meal Companion includes the functionality to suggest recipes based on ingredient availability. Simply use the command `recipe possible`, and Meal Companion will list out the recipes that can be made with the ingredients you currently have.

![recipepossible1.png](images/recipepossible1.png)  
<sub>Fig 10: Sample of Recipe Possible command showing the list of ingredients and the recipes that can be made with those ingredients, with user input highlighted.</sub>

### Random Recipe
Meal Companion allows you to get a random recipe as suggestion for your next meal using the command `recipe random`.

### Check Ingredients for Recipe
To check if you have sufficient ingredients to make a recipe, you can run the command `recipe need <recipe_number>`. Ingredients that you are missing will be listed along with the quantity needed.

### Almost Completed Recipe
To check for recipes that you almost can make, you can run the command `recipe almost`. Such recipes have at most 3 lacking ingredients.

#### [Back to table of contents](#table-of-contents)

## Saving Data
Meal Companion automatically saves the ingredients you add to a text file named `ingredients.txt`. This text file can be accessed from the same folder where you downloaded the original `mealcompanion.jar` file. 

![save1.png](images/save1.png)  
<sub>Fig 11: Location of saved file containing all user-entered ingredients, within the same folder that</sub> `mealcompanion.jar` <sub>is stored.</sub>

### Transferring Saved Data to Other Devices
If you would like to access your saved ingredients list on a new instance of Meal Companion on a different device, it is as simple as copying and pasting the `ingredients.txt` text file to the new device. As long as it is saved in the same folder, Meal Companion will be able to detect it and utilize the existing data. 

#### [Back to table of contents](#table-of-contents)

## Help
If you are unsure of which commands to use, the `help` command will display a list of available commands for you to use.

![help1.png](images/help1.png)  
<sub>Fig 12: Sample of Help command with listed output of in-built commands.</sub>

#### [Back to table of contents](#table-of-contents)

## Command List
Please see the below table for the list of available commands.

| Feature | Command | Examples |
| ------- | ------- | -------- |
| Add ingredients to your list | `add <ingredient> /qty <quantity>` | `add apple /qty 3` |
| Remove ingredients from your list | `remove <ingredient> /qty <quantity>` | `remove ground chicken /qty 100` |
| List all stored ingredients | `ingredients list` | `ingredients list` |
| Search for a valid ingredient | `ingredients search <keyword>` | `ingredients search salt` |
| Return all valid ingredients | `ingredients search` | `ingredients search` |
| List all stored recipes | `recipe all` | `recipe all` |
| List details of a specific recipe | `recipe <index of recipe>` | `recipe 6` (recipe for Hainanese Chicken Rice) |
| List recipes that can be made with current list of stored ingredients | `recipe possible` | `recipe possible` |

#### [Back to table of contents](#table-of-contents)

# Conclusion
Congratulations! You have reached the end of this user guide, which means you are ready to make full use of Meal Companion! Of course, you may refer to this guide at any time, and if you have any further questions, feel free to reach out to the Meal Companion team at any of our contact links at the top of the page! Have a good time, and we hope you enjoy using Meal Companion!

#### [Back to top](#user-guide)
