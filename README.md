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

![Screenshot (218)](https://user-images.githubusercontent.com/73945266/105503475-d4618780-5cf0-11eb-964d-ed70740af31c.png)



---


# CRUD Operations

- Create a project

create() - This method has been used for load create.blade.php file. In this file user can find form for insert new records and 
filling data insert data request will be send to store() method of ProjectController.php controller class.

![Screenshot (163)](https://user-images.githubusercontent.com/73945266/104889413-663b5e80-5998-11eb-918f-889dde0c6d19.png)

![Screenshot (168)](https://user-images.githubusercontent.com/73945266/104889693-c6320500-5998-11eb-8148-cd9ba5df42dc.png)

![Screenshot (167)](https://user-images.githubusercontent.com/73945266/104889821-eb267800-5998-11eb-9ee9-ad53dddf7e2e.png)
---

- View a project

show() - This method in Crud controller has been used for fetch single data details based on on value of $id argument. 
For this it has been used findOrFail() method. After fetch details it will send to view.blade.php file.

![Screenshot (154)](https://user-images.githubusercontent.com/73945266/104890388-b36c0000-5999-11eb-8df8-45e9449ea245.png)
---

- Edit a project

edit() - This method main function is fetch single data from Mysql database and load into edit or update form for make required changes.

![Screenshot (164)](https://user-images.githubusercontent.com/73945266/104890141-57a17700-5999-11eb-8a37-5a4df7b997f2.png)

![Screenshot (165)](https://user-images.githubusercontent.com/73945266/104890224-7a339000-5999-11eb-949d-e197f72b5bd6.png)
---

- Delete a project

delete() - Delete() method mainly used for remove single or multiple data from Mysql Database. This is last operation Crud Operation in Laravel 8 Crud tutorial series.

![Screenshot (167)](https://user-images.githubusercontent.com/73945266/104889015-c1208600-5997-11eb-85b2-c9582b2bed60.png)
---

- View all projects

![Screenshot (169)](https://user-images.githubusercontent.com/73945266/104890649-0e055c00-599a-11eb-8a4c-9c213d6413bf.png)


---


# License

Basically, feel free to use and re-use any way you want


