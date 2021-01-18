# CRUD-operation-Laravel-

This is a simple laravel 8 CRUD app.
CRUD stands for Create, Read, Update and Delete which are operations needed in most data-driven apps that access and work with data from a database. 
In this example, we'll see how to impelement the CRUD operations in Laravel 8/7 against a MySQL database.


---



## How to install and run on your local system

- Clone the repository with __git clone__ https://github.com/JHS-Sujel/CRUD-operation-Laravel-
- cd projectapp/
- Run __composer install__
- Copy __.env.example__ file to __.env__
![Screenshot (165)](https://user-images.githubusercontent.com/73945266/104888746-5bcc9500-5997-11eb-8519-77ca5e5f7cb2.png)
- Run __php artisan key:generate__
- Add your database config in the .env file
- Run __php artisan migrate --seed__ (it has some seeded data for your testing)
![Screenshot (166)](https://user-images.githubusercontent.com/73945266/104888884-933b4180-5997-11eb-849d-308ad4d23de2.png)
- php artisan serve (if the server opens up, http://127.0.0.1:8000,  then we are good to go)
![Screenshot (164)](https://user-images.githubusercontent.com/73945266/104888559-19a35380-5997-11eb-813b-a60512b9ccf5.png)
- Navigate to http://127.0.0.1:8000/projects
![Screenshot (163)](https://user-images.githubusercontent.com/73945266/104888312-c3ceab80-5996-11eb-9de7-4a81efe21dce.png)



---


## Operations
- Create a project
![Screenshot (163)](https://user-images.githubusercontent.com/73945266/104889413-663b5e80-5998-11eb-918f-889dde0c6d19.png)
![Screenshot (168)](https://user-images.githubusercontent.com/73945266/104889693-c6320500-5998-11eb-8148-cd9ba5df42dc.png)
![Screenshot (167)](https://user-images.githubusercontent.com/73945266/104889821-eb267800-5998-11eb-9ee9-ad53dddf7e2e.png)
- View a project
- Edit a project
- Delete a project
![Screenshot (167)](https://user-images.githubusercontent.com/73945266/104889015-c1208600-5997-11eb-85b2-c9582b2bed60.png)
- View all projects


---


## License

Basically, feel free to use and re-use any way you want


