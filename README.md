# CRUD-operation-Laravel-

## About

  This is a simple laravel 8 CRUD app.
  If you are new in Laravel 8 and looking for a step by step project for Laravel 8 CRUD projectapp 
  then this project will help you to learn how to make a complete CRUD application using Laravel 8. 
  Before starting we have to check our system requirement is okay to use Laravel 8. 
  The Laravel 8 minimum requirements are listed below so that you can confirm 
  either your system is okay or not to install Laravel 8 project for making a Laravel 8 CRUD application.

  CRUD stands for Create, Read, Update and Delete which are operations needed in most data-driven apps that access and work with data from a database. 
  In this example, we'll see how to impelement the CRUD operations in Laravel 8/7 against a MySQL database.


---

There some couple of things you need to have on your system before installing laravel 8

- PHP
- Composer
- Server (WAMP, LAMP, XAMPP etc)

---

## Steps for making Laravel 8 CRUD ( For beginners )

- Step 01: Install Laravel 8 (Composer-Setup.exe)
- Step 02: Server (WAMP, LAMP, XAMPP etc)
- Step 03: Create project with composer ( Run: Composer create-project laravel/laravel (project name) )
- Step 04: Run cd projectname
- Step 05: Database Configuration ( Set db in .env nd mysql )
- Step 06: Make model & migration ( Run: php artisan make:migration create_(table name)_table --create=(table name) )
- Step 07: Make controller (Ex: Run- php artisan make:controller ProjectController --resource --model=Project)
- Step 08: Define routes
- Step 09: Make views (Like: Layouts and Projects folder. In layouts create; app.blade.php. 
                       In projects folder create index.blade.php, create.blade.php, edit.blade.php, show.blade.php)
- Step 10: Run: php artisan serve

---

## How to install and run my project on your local system

- Clone the repository with git clone https://github.com/JHS-Sujel/CRUD-operation-Laravel-
- cd projectapp
- Run composer install or update 
- Add your database config in the .env file
- Create a new database in your localhost 
- Table create: Run php artisan migrate
- Create default user for system with: php artisan db:seed.    --seed__ (it has some seeded data for your testing)
- Run php artisan key:generate
- Run php artisan config:clear
- Run php artisan serve (if the server opens up, http://127.0.0.1:8000, then we are good to go)

---

## Or Step by Step to create a project (Using cmd). Screenshot given below:

- Create a project in htdocs

  ![104888746-5bcc9500-5997-11eb-8519-77ca5e5f7cb2 (2)](https://user-images.githubusercontent.com/73945266/105570965-a58df480-5d76-11eb-962f-2b19e89604bb.png)
 
---

- DB connect 
  
  ![Screenshot (247)](https://user-images.githubusercontent.com/73945266/105571147-c4d95180-5d77-11eb-98e3-27c292905df9.png)
  
---

- Create Migration 
  
  First cd into the project app: cd projectapp
  
  php artisan make:migration create_projects_table --create=projects
  
  ![104888884-933b4180-5997-11eb-849d-308ad4d23de2 (2)](https://user-images.githubusercontent.com/73945266/105570961-a3c43100-5d76-11eb-920a-4f537c6fce99.png)
  
---
  
  A migration file will be created in the database/migrations folder, and we need to create our schema, 
  I added name (string), introduction (string), location (string), cost of  the project (float), date created, and date updated.
  
  ![Screenshot (248)](https://user-images.githubusercontent.com/73945266/105571142-c276f780-5d77-11eb-9f2e-8a4ef1df8568.png)
  
---
  
  Before we run our migration command, we need to specify the default string length, else, we are going to run into errors
  So go to app/Providers/AppServiceProvider.php and add

  Schema::defaultstringLength(191);

  to the boot function, also add

  use Illuminate\Support\Facades\Schema;

  to the top
  
  ![Screenshot (249)](https://user-images.githubusercontent.com/73945266/105571144-c3a82480-5d77-11eb-8f76-c7ce0d818f47.png)
  
---
  
  Finally, we run our migration command
  
  ![104888884-933b4180-5997-11eb-849d-308ad4d23de2 (3)](https://user-images.githubusercontent.com/73945266/105570962-a4f55e00-5d76-11eb-8d3c-902d5c135093.png)
  
---

- Add Resource Route
  
  We need to add routes for our CRUD operations, Laravel provides a resource route for us that will take care of the CRUD, 
  that is a route to Create, another route to Retrieve, a separate route to Update, and finally a route to Delete.
  So head up to routes\web.php and add our resource route

  Route::resource(‘projects’, ProjectController::class);

  Also, add the ProjectController class at the top, this was introduced in this version, Laravel 8 does not know where to call the function from

  use App\Http\Controllers\ProjectController;
  
  ![Screenshot (250)](https://user-images.githubusercontent.com/73945266/105571145-c440bb00-5d77-11eb-94fc-dbee65bea430.png)
  
---
  
-  Model & Controller Create

   Previously, in Add Resource Route, the second parameter for the resource is ProjectController, so we need to create the controller 
   and we need to specify the resource model by add --model

   Php artisan make:controller ProjectController --resource --model=Project

   It will ask a question if you want to create the model because it does not exist. Type yes and it will create the model and controller

  ![104888884-933b4180-5997-11eb-849d-308ad4d23de2 (4)](https://user-images.githubusercontent.com/73945266/105570964-a58df480-5d76-11eb-8020-e45714f51058.png)
  
---
  
  A controller for project has been created for us with the following methods in the controller folder app/Http/Controllers/ProjectController.php

  - index()
  - create()
  - store(Request, $request)
  - show(Project, $project)
  - edit(Project, $project)
  - update(Request, $request, Project, $project)
  - destroy( Project, $project)
  
  app/Models/Project.php, add the following functions and the fillable, the fillable are the fields in the database that a user can fill.
  
  ![Screenshot (251)](https://user-images.githubusercontent.com/73945266/105571146-c440bb00-5d77-11eb-9d92-e8d7839f8c38.png)
  
---

- Add your views
  Laravel view files are is called the blade files, we are going to add those blade files, so a user can be able to interact with our app
  I like arranging my views according to the models, so I am going to create two folders in the resources/views folder

  - Layouts
  - app.blade.php
  - Projects
  - Index.blade.php
  - Create.blade.php
  - Edit.blade.php
  - show.blade.php

---

# Everything is now set

- php artisan serve (if the server opens up, http://127.0.0.1:8000,  then we are good to go)

  ![Screenshot (164)](https://user-images.githubusercontent.com/73945266/104888559-19a35380-5997-11eb-813b-a60512b9ccf5.png)
  
---

--- DONE

- My Welcome Page http://127.0.0.1:8000

  ![Screenshot (257)](https://user-images.githubusercontent.com/73945266/105634959-ca738c00-5e8a-11eb-8206-6cbaacb2583b.png)

  
---

- Navigate to http://127.0.0.1:8000/projects

  ![Screenshot (237)](https://user-images.githubusercontent.com/73945266/105517372-29a59500-5d01-11eb-9398-3403d05d8b99.png)

---


## My CRUD Operations Features 

- Create a project

  create() - This method has been used for load create.blade.php file. In this file user can find form for insert new records and 
  filling data insert data request will be send to store() method of ProjectController.php controller class.

  ![Screenshot (240)](https://user-images.githubusercontent.com/73945266/105517374-2a3e2b80-5d01-11eb-99a0-f7a471ae00ed.png)

  ![Screenshot (248)](https://user-images.githubusercontent.com/73945266/105517369-290cfe80-5d01-11eb-9d93-c8b3fd9e0126.png)

  ![Screenshot (241)](https://user-images.githubusercontent.com/73945266/105517344-23171d80-5d01-11eb-8244-8b6b76625c9c.png)

---

- View a project

  show() - This method in Crud controller has been used for fetch single data details based on on value of $id argument. 
  For this it has been used findOrFail() method. After fetch details it will send to view.blade.php file.

  ![Screenshot (242)](https://user-images.githubusercontent.com/73945266/105517353-25797780-5d01-11eb-968a-677b7658e37d.png)

---

- Edit a project

  edit() - This method main function is fetch single data from Mysql database and load into edit or update form for make required changes.

  ![Screenshot (243)](https://user-images.githubusercontent.com/73945266/105517354-26120e00-5d01-11eb-9c57-d3fc388c6b47.png)

  ![Screenshot (244)](https://user-images.githubusercontent.com/73945266/105517356-26aaa480-5d01-11eb-8c2c-291153a10b68.png)

---

- Delete a project

  delete() - Delete() method mainly used for remove single or multiple data from Mysql Database. This is last operation Crud Operation in Laravel 8 Crud tutorial series.

  ![Screenshot (246)](https://user-images.githubusercontent.com/73945266/105517365-28746800-5d01-11eb-9d3d-6e023bbd855a.png)

---

- View all projects

  ![Screenshot (245)](https://user-images.githubusercontent.com/73945266/105517361-27dbd180-5d01-11eb-87d6-fbf3b97375fc.png)

---


## License

   Basically, feel free to use and re-use any way you want


