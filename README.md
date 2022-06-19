# Table of content
1. Professional Self-Assessment
2. Artifact Introduction
3. Refinement Plan
4. Code Review
5. Enhancement One - Software design and engineering
6. Enhancement Two - Algorithms and data structure
7. Enhancement Three - Databases          


# Professional Self-Assessment
-------------------------------------------------------



# Artifact Introduction
-------------------------------------------------------

I aim to focus on a single artifact that will allow me to showcase my knowledge and skills in three categories: Software Design/Engineering, Algorithms and Data Structures, and Databases. I started working on this project while taking the CS-360 Mobile Architect & Programming class, which required the development of a fully functional application as a final project. I created an android inventory app using android studio and the Java language that implements a fully functional sign-in/sign-up feature. Furthermore, this application consists of three major components, inbound, outbound, and display. The inbound enables the user to add a new product, the outbound allows the user the remove a product, and the display allows the user to view a list of all products. Additionally, I implemented a database that holds all the data within the application, allowing the user to interact with this data by adding, deleting, updating, and reading items in the database.

# Refinement Plan
-------------------------------------------------------

### Category One: Software Engineering/Design
I plan to enhance the application's overall design by adding more features to provide the user with a better experience. The original design consists of four activities limiting the user's actions. I will add new screens where the user can perform additional steps such as creating a sales order or adding a new customer. Additionally, I intend to expand the complexity of the design to mimic actual warehouse operations, including picking orders, displaying inventory, shipping products, and performing other regular warehouse activities. Lastly, I will update the overall look of the application to make it more visually appealing by changing the app User-Interface (UI), such as color, text, and the way data is displayed. Also, I will work on the user experience (UX) to focus on the application's usability, objective, and engagement. With this enhancement, I will demonstrate my skills and understanding of the java language, android application development, User-Experience (UX), and User interface (UI). Additionally, this will showcase skills beyond just writing code since I can display mastery in understanding the user's needs and translate those needs into a working application.

### Category Two: Algorithms and Data Structures
I plan to implement a series of algorithms in my application that will allow me to perform certain operations more effectively. For example, the data retrieved from the database must be handled in a specific way before it can adequately be displayed to the user. As a result, I will have to create an algorithm that can execute this action efficiently. I will also improve my use of arrays and implement additional data structures such as ArrayList and HashMaps. ArrayList is essential because, contrary to Array, they don't have a fixed size. Since the amount of data we will handle will vary based on what is being retrieved from the database, it is crucial to use the proper data structure. These enhancements will allow me to display my skills in working with the data structure and my understanding of when is the right time to implement them to accomplish a task efficiently. Also, I will demonstrate my ability to develop and implement an algorithm that works and completes a task efficiently.

### Category Three: Databases
This application uses an SQLite database to store data locally on the android device. I plan to add more tables to give the user access to additional data based on the new features I will implement. Additionally, I intend to improve how the applications interact with the database by creating methods to handle all the queries needed to operate the application. As a result, I will use the concept of CRUD when creating the required methods to interact with the database. By accomplishing this, I will demonstrate my understanding of SQLite and how it works on an android application. Also, I will show my SQL skill by showcasing my ability to use statements to interact with the database correctly, such as SELECT and UPDATE. 

# Code Review
-------------------------------------------------------
In this code review, I dive more into the details of how I plan to enhance this artifact in all three categories required for this project.
[Code Review](https://www.youtube.com/watch?v=14hq23RkpcU)

# Enhancement One - Software design and engineering
-------------------------------------------------------
The original design I had for this application was minimal as I only aimed to accomplished what was required for the assignment. This consisted of four Activities:
1. Dashboard – Is the main point of navigation between the main screen and other activities.
2. Add Item – Allow the user to add new item into inventory
3. Pick Product – Allows the user to pick time and remove it from inventory
4. Inventory – Display all the item in inventory

![Original Degign](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/Inventory%20App%20Original%20Design.png)

As I have mentioned before my goal is to expand the application to perform more task that can be found within a warehouse management system. This will be connected through various activities that will offer the user an easy user experience and interaction. The application will be driven by three key activities: Inbound, outbound, monitor.



# Enhancement Two - Algorithms and data structure 
-------------------------------------------------------

I Included this artifact for my ePorfolio because I’m able to showcase a more broad and diverse use of my abilities and everything I have learned throughout the program. Since, I'm trying to create an entire application that contains many classes, rather than a piece of code that sit on a single class, there are many instances where I make use of data structures and algorithms. For this enhancement, I will focus on three specific parts that show my use and thought process of Array, ArrayList, and Maps.

### Array

![Array.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/Array.png)

In this case, I decided to make use of a simple Array because I already have prior knowledge of the number of elements and values each array will have. Knowing this information, I’m able to declare and initialize the array in a single line of code, making the code less clustered. The Array "table_name" is empty because it will hold the value depending on the user selection. The users, customers, and vendors array hold the column names for the tables in the database, and using a conditional statement the 'table_name' will be equal to a copy of the table the user wants to interact with. 

### ArrayList

![ArrayLIst.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/ArrayLIst.png)

In this case, a simple array would not be effective since we don’t know how many elements will be entered in the ArrayList. This ArrayList holds Textviews that are created based on the number of entries that exist in the customer's table in the database, which could be 10 or 1000. I created a query that retrieves all the data in the Customer table and stores it as a cursor that will then be read using a while loop. Within the while loop, a text view is created holding all the data from each row, later adding it to the ArrayList. Finally, the ArrayList is read and every element within the array is added to a linear layout and displayed to the user.

### Map

![Map.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/Map.png)

The last example I want to cover is the use of a map, which stores information as a key and value pair. When updating the database, one must specify the column and value that needs to be updated and a map is the best implementation for this scenario. I could achieve the same result by creating two arrays of passing multiple sting values to the method, but this would be counterproductive as it will require a lot of unnecessary code. The update method is implemented, the key serves as the Colum that need to be updated, and the value serves as the new value for the column. The row is specified in the SQL statement using the WHERE clause.

### Skills

I believe I met the course objective I planned for this enhancement, using the different types of data structures I can demonstrate my ability to know when is necessary to use each data structure and how to properly implement them. I did not face any challenges as I have used this data structure before in previous work, so I have a good understanding of how they should be used.

# Enhancement Three - Databases  
-------------------------------------------------------
When I first created the DBHandler class, which handles all interaction with the database, I created methods that became repetitive as they performed similar actions. This is very counterproductive as hundreds of queries would be executed in the application, meaning the same code would have to be repeated many times, affecting the application's overall performance.

![OldCodeExample.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/OldCodeExample.png)
 
### Enhancement intro

For my enhancement, my goal was to create different methods to handle all the other queries needed from a single method. As a result, I made three methods to accomplish that task for all cases.

### Insert data into the database method

![DatabaseTableArrays.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/DatabaseTableArrays.png)

![InsertDataMethod.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/InsertDataMethod.png)

The method accepts two parameters, a table name as a string and an array of values that will be entered into the database. Since there are many tables in the database and each table contains a different number of columns, it is not practical to directly pass the name of each column in a table as a parameter. Instead, I will use the table name to determine which table needs to be accessed. To accomplish this, I created multiple arrays named after each of the existing tables in the database, and each variety contains the column names of each table.

How is the suitable array selected? When determining what array to use, I use the “tableName” String to create a copy of the correct array and assign it to an empty array called “table_name.” Lastly, I use a contentValue instance to put each value in the corresponding table. For example, if the user creates a new account, they will pass the following parameters to the insertData() method.
1. tableName = Users
2. String [] values = {“00000”, Joe”, “Joe@hotmail.com”, “Joe03”, “no” , “no”}

#### Obtaining Data
The values passed to the array will be obtained in different ways.

1. A new user ID will be automatically generated using the generateUserId() method;

![GenerateUserIdMethod.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/GenerateUserIdMethod.png)

2. The username, email, and password will be acquired from the user input, by getting the string values of the textInputEditText within the activity.

![CreateAccountActivity.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/CreateAccountActivity.png)

3. Remember me, and Email validation are set to “no” by default and are updated when the necessary action is performed.

#### Adding data to table in database

When the insertData() method is executed, it will first determine what array needs to be used, so the conditional statement runs. Since the user passed "Users" as the tableName, the first statement is true, making table_name equal to the array user.

![TableSelectionConditionalStatement.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/TableSelectionConditionalStatement.png)

Which means that now:

![SelectedTableArray.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/SelectedTableArray.png)

![InitializeEmptyArray.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/InitializeEmptyArray.png)

Next, a for loop iterate through the table_name array matching each index and putting the information in the contentValues instance as a key: value pair, where the key is the column name specified by the index in table_name and the value is specified by the index in the array of values passed as a parameter.

![LoopToAddDataToContentValue.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/LoopToAddDataToContentValue.png)

The for loop above executes the same amount of time as the values that exist in the array. Below is a visual presentation of how this would have been completed by directly passing the key: value pair to the contentValues.

![ExampleOfDirectImput.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/ExampleOfDirectImput.png)

If we only have one table to interact with, this approach would be ideal as the keys will never change, but since we have multiple tables, this approach would not work since the keys will change based on what table is being used.

Finally, All the data in contentValues is read and entered into its respective table.

![LoopAddDataToDatabase.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/LoopAddDataToDatabase.png)

### Get data from the database method

![GetDataMethod.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/GetDataMethod.png)

To retrieve data from the database, I created a simple method that takes a string as a parameter, the string that is passed is an SQL statement that calls for the specific data. For example:

This query gets the username and password from the Username table in the database where the username is Carlos.

![GetDataQueryExample.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/GetDataQueryExample.png)

This query selects all the data from the Vendors database

![GetDataQueryExample2.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/GetDataQueryExample2.png)

The retrieved data is return as a Cursor which than can be accessed using a while loop to manipulate the rawData it contains.

![SaveDataInCursor.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/SaveDataInCursor.png)

![LoopThrougthTheDataAndPerformAction.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/LoopThrougthTheDataAndPerformAction.png)

### Update data on the database method
To update a value in the database I created an update method that takes in four parameters.
1.	A table name as a String (Specifies what table will be updated)
2.	A set of key and values as a HashMap (Specifies the column names that will be updated and the new value)
3.	A columnName as a String (specifies the column that will serve as the identifier)
4.	A rowName as a String (specifies which row will be updated)

Each parameter is essential in updating the correct information in the database.

![UpdateDataMathod.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/UpdateDataMathod.png)

When the user data is originally entered is look as follow:

![OriginalDataInDatabase.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/OriginalDataInDatabase.png)

The bellow code updates the data using the code below. 

![InplementsUpdateDataMethod.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/InplementsUpdateDataMethod.png)

How this work? I created a map that contains one input, a key = “RememberMe” whis is the name of the table that will be updated, and a value = currentCheckBoxStatus which is updated based on the status of a checkbox.

![RemenberMe.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/RemenberMe.png)

![GetRemenberMe.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/GetRemenberMe.png)

Once I determined the column I want to update and the new value, I can call the update method from the DBHandler and pass the necessary parameters. 
Update table name Users changing the value of Column RememberMe to the current value of currentCheckBoxStatus. Use the column name Username as the referencing column and withing that column update the rowName with the value of Carlos. 
This will update a specific cell withing an specified table.

![UpdatedDataInDatabase.png](https://raw.githubusercontent.com/ramirez0307/ramirez0307.github.io/main/UpdatedDataInDatabase.png)

Why use a HashMap? When dealing with a pair of values, maps provide the easiest implementations. I could accomplish something similar using an array, but that will require the creation of two arrays, one that holds the column to be updated and another one to hold the value. Both arrays will have to be iterated, and this could increase the chances of errors. A HashMap makes it simple, as it makes it clear to the developer what values will be updated without worrying about the indexes on an array. 

### Skills 

Through the course of this enhancement, the skills that I can demonstrate are how I can create effective methods that interact with all the tables in the database. These methods work for all possible scenarios that require adding, reading, and updating data. Additionally, I can showcase my ability to create an SQLite database for an android application and perform specific actions based on the user request. Lastly, aside from source code, I'm also able to demonstrate a basic understanding of creating database schema to display a visual representation of the database and how each table interacts with one another.







