### **Recipes Application - Project Idea**



##### **Description**



This project represents a mobile application that allows users to share their meal recipes with other users. Each user can upload, modify or delete their own recipes and can see and vote (like/dislike) posts. When pressing a recipe, the user will be redirected to the page of it.



**Recipes** will have the following information stored

* Id (pk) - unique identifier
* Name - the name of the meal prepared
* Owner Id (fk) - the one who published the recipe 
* Category - can be a dessert, a main dish, a salad etc.
* Ingredients - stored as an json object containing ingredient and quantity for each product
* Instructions - a description on how should the recipe be prepared
* Duration - an approximate duration of how long should the recipe take
* Last modification - last time when the recipe was updated



**Users** table will contain the following information:

* Id (pk) - unique identifier
* Username - is unique and displayed for other users
* Hashed password - password stored in a secure state
* Creation date - date when the account was created



There will also be a table that stores the information related to the **votes**, containing

* Id
* Recipe id - post where the voter has reacted
* user id - user who performed the vote
* vote type (positive or negative)



##### **CRUD operations**



Each user should be able to see other's recipes, but only change or their own. Also, the user should be able to add new ones, by filling all the info related to that one.



When viewing the page of a recipe, if it belongs to the current user, they will see 2 additional buttons for update and delete. For delete, an additional verification is required.



When going through the list of recipes, the user can also see a button on the screen that allows adding a new recipe for it, or they can click on one of them to see the details related to it.

##### 

##### **Persistence and offline access**



All the crud operations should be persistent on the local db and, as soon as the app is online, the server should be updated as well. While the user doesn't have internet connection, they should be able to see the last recipes they saw while being online, be able to update/delete theirs and create new ones. The info will be changed in the db as soon as the device goes back online. 



<img width="767" height="611" alt="image" src="https://github.com/user-attachments/assets/9fce13d8-990d-43d2-ac76-47918d9ab8c1" />


