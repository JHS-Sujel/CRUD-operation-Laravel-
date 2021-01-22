# CRUD-operation-Laravel-

This is a simple laravel 8 CRUD app.
If you are new in Laravel 8 and looking for a step by step project for Laravel 8 CRUD projectapp 
then this project will help you to learn how to make a complete CRUD application using Laravel 8. 
Before starting we have to check our system requirement is okay to use Laravel 8. 
The Laravel 8 minimum requirements are listed below so that you can confirm 
either your system is okay or not to install Laravel 8 project for making a Laravel 8 CRUD application.

CRUD stands for Create, Read, Update and Delete which are operations needed in most data-driven apps that access and work with data from a database. 
In this example, we'll see how to impelement the CRUD operations in Laravel 8/7 against a MySQL database.


---


# Steps for making Laravel 8 CRUD

- Step 01: Install Laravel 8
- Step 02: Database Configuration
- Step 03: Make model & migration
- Step 04: Make controller
- Step 05: Define routes
- Step 06: Make views


---



# How to install and run on your local system

- Clone the repository with git clone https://github.com/JHS-Sujel/CRUD-operation-Laravel-
- cd projectapp
- Run composer install or update 
- Add your database config in the .env file
- Create a new database in your localhost 
- Table create: Run php artisan migrate
- Create default user for system with: php artisan db:seed.    --seed__ (it has some seeded data for your testing)
- Run php artisan key:generate
- Run php artisan config:clear

---

# Or Step by Step to create a project (Using cmd). Screenshot given below:

![Screenshot (165)](https://user-images.githubusercontent.com/73945266/104888746-5bcc9500-5997-11eb-8519-77ca5e5f7cb2.png)
---

![Screenshot (166)](https://user-images.githubusercontent.com/73945266/104888884-933b4180-5997-11eb-849d-308ad4d23de2.png)
---

- php artisan serve (if the server opens up, http://127.0.0.1:8000,  then we are good to go)

![Screenshot (164)](https://user-images.githubusercontent.com/73945266/104888559-19a35380-5997-11eb-813b-a60512b9ccf5.png)
---

--- DONE


- Navigate to http://127.0.0.1:8000/projects

![Screenshot (229)](https://user-images.githubusercontent.com/73945266/105512827-c9f8bb00-5cfb-11eb-8c2a-095a10be2291.png)



---


# CRUD Operations

- Create a project

create() - This method has been used for load create.blade.php file. In this file user can find form for insert new records and 
filling data insert data request will be send to store() method of ProjectController.php controller class.

![Screenshot (220)](https://user-images.githubusercontent.com/73945266/105512412-42ab4780-5cfb-11eb-91d5-c03ad1c501ba.png)

![Screenshot (221)](https://user-images.githubusercontent.com/73945266/105512382-3cb56680-5cfb-11eb-8060-93f35cb7b57b.png)

![Screenshot (222)](https://user-images.githubusercontent.com/73945266/105512387-3e7f2a00-5cfb-11eb-9977-46a73b445c00.png)

---

- View a project

show() - This method in Crud controller has been used for fetch single data details based on on value of $id argument. 
For this it has been used findOrFail() method. After fetch details it will send to view.blade.php file.

![Screenshot (223)](https://user-images.githubusercontent.com/73945266/105512391-3f17c080-5cfb-11eb-8ae1-88b437e60e19.png)

---

- Edit a project

edit() - This method main function is fetch single data from Mysql database and load into edit or update form for make required changes.

![Screenshot (224)](https://user-images.githubusercontent.com/73945266/105512392-3fb05700-5cfb-11eb-83ae-d7e677b3c094.png)

![Screenshot (225)](https://user-images.githubusercontent.com/73945266/105512396-4048ed80-5cfb-11eb-9390-b8d66b45e71d.png)

![Screenshot (226)](https://user-images.githubusercontent.com/73945266/105512400-40e18400-5cfb-11eb-824c-34d09410713a.png)

---

- Delete a project

delete() - Delete() method mainly used for remove single or multiple data from Mysql Database. This is last operation Crud Operation in Laravel 8 Crud tutorial series.

![Screenshot (227)](https://user-images.githubusercontent.com/73945266/105512404-40e18400-5cfb-11eb-8702-920423b0d5ac.png)

---

- View all projects

![Screenshot (228)](https://user-images.githubusercontent.com/73945266/105512406-417a1a80-5cfb-11eb-912c-a0e6da215755.png)

---


# License

Basically, feel free to use and re-use any way you want


