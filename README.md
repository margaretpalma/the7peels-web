# 🍌 The 7 Peels - Video Game Store 🍌 

Welcome to my third and final capstone project for Year Up United LTCA Program. 
This project is a full-stack inspired web application focused on secure backend API development, database persistence, and testing through Insomnia. 

## 🍌 Organization🍌

<img width="1897" height="899" alt="Jira_Board" src="https://github.com/user-attachments/assets/c7fb43a5-a62a-42c1-8aa5-1cc7f7a89c2d" />


## 🍌 Tech 🍌
```
-Java
-Spring Boot
-MySql
-JDBC Dao
-Insomnia as an automated test runner
-HTML
```

## 🍌 What Can The User Do? 🍌
```
-Register for a new account
-Log in using JWT Authentication
-Browse all available video games and products
-View products by category
-Log in as either user or admin
```

## 🍌Optional Phase 3 - Shopping Cart 🍌
```
Endpoints Implemented

| Method | Endpoint                     | Description             |
| ------ | ---------------------------- | ----------------------- |
| GET    | `/cart`                      | Get current user’s cart |
| POST   | `/cart/products/{productId}` | Add product to cart     |
| PUT    | `/cart/products/{productId}` | Update quantity         |
| DELETE | `/cart`                      | Clear cart              |
```

## 🍌 Phase 1 🍌
```The CategoriesController class was provided, but I had to complete the methods. To complete this phase I had to: 
-Implement the REST endpoints - Get, Post, Put, Delete
-Add @RestController, @RequestMapping, and @CrossOrigin
-Restricted Category Creation, updates, and deletions to administrators using @PreAuthorized
-Implemented the required DAO logic inside of MySqlCategoriesDao
```
## 🍌 Phase 2 - Bug Fixes 🍌
🐸Bug #1: Incorrect Product Search Results
<img width="961" height="272" alt="image" src="https://github.com/user-attachments/assets/ee487180-25c9-4252-93e2-01573871662e" />
Users reported that product search results were inaccurate when filtering by category, price range, or subcategory.
The fix I applied was ensuring price range filters(min and max), and category filters worked together correctly. 
Corrected the search logic to properly apply filters when parameters were present. 


## 🐸Bug #2: Duplicate Error
<img width="944" height="586" alt="Database" src="https://github.com/user-attachments/assets/827ea9a7-b8c3-4fcf-b057-34b1d7d925cf" />
<img width="949" height="746" alt="Delete_Extra_Controllers" src="https://github.com/user-attachments/assets/ea8ecb01-edb5-4644-b8ed-724e094020c4" />
<img width="741" height="407" alt="image" src="https://github.com/user-attachments/assets/c749bd54-40b5-4574-9192-295c643fe026" />

Originally, there was "create" (INSERT) instead of update operation. The result of this was sending a PUT request would create a duplicate
product into the database instead of updating the existing one. This issue was resolved by updating the controller to call the update method.

## 🐸Bug #3: Product Count Test Error
While testing in Insomnia, a product search expected to return 1 actually returned all of the products. It was caused by the same search filter logic
issue described in bug 1. 
<img width="645" height="67" alt="Screenshot 2025-12-18 233704" src="https://github.com/user-attachments/assets/e5c65852-b172-4e8c-83fa-0dc5b758e793" />


##  🐸Bug #4: Front End Error 
Small Fix! Just a quick HTML error. 

<img width="516" height="737" alt="Screenshot 2025-12-15 145058" src="https://github.com/user-attachments/assets/4dc3b50a-01e1-4b17-af74-1b15e267b72c" />

# 🍌 Reflection + Growth🍌 
In Capstone 1, my focus was on understanding basic structure. Learning how controllers, models, and databases communicate. 
I was still becoming comfortable reading error messages, understanding application flow, and figuring out where bugs lived.

By Capstone 2, I became more confident navigating backend logic, working with databases, and testing endpoints.
I started to recognize patterns, understand how security and roles affect behavior, and debug with more intention rather than trial and error.

Capstone 3 challenged me to bring all of those skills together into a full application.
I encountered real-world bugs, including authorization issues, database constraints, and endpoint mismatches 
and learned how to systematically test, isolate, and resolve them using tools like Insomnia, MySQL Workbench, and IntelliJ.



# 🍌 Why The 7 Peels?🍌 
The name represents the idea that every layer of an application works together - authentication, database, controllers, security and testing.
These components all have to work together in order for the system to function properly. 

It also represents the people who supported me throughout the entirety of LTCA:
Mohammed K, Muhammed M, Hunbal, Shewit, John, and Dalis. Each one of them played a role in helping me learn, troubleshoot, and stay motivated.
Every peel matters, and this bunch wouldn’t be the same without any one of them 🍌

# 🍌 A Special Thanks🍌 
A special thank you to my instructor, Matt, for being a constant source of knowledge and patience over the last 12 weeks.
His ability to explain complex topics clearly, answer questions thoughtfully, and guide us without discouraging experimentation made a huge impact on my learning experience.
This project reflects many lessons learned through his instruction.





