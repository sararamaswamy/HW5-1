# SI 364 - Final Project questions

## Overall

* **What's a one-two sentence description of what your app will do?**
This application will store data, including movie characteristics like name, genre, directors, and actors that a user enters into a form. It is an application meant to help a user save movies that he or she wants to see. 

## The Data

* **What data will your app use? From where will you get it? (e.g. scraping a site? what site? -- careful not to run it too much. An API? Which API?)**
My app will use data from the omdb API to get data about movies.

* **What data will a user need to enter into a form?**
A user will enter a movie name, year, director, genre, and list of actors, separated by commas. 

* **How many fields will your form have? What's an example of some data user might enter into it?**
It will contain 6 fields, which are the following: movie name, year, director, genre, and list of actors, each separated by commas.

* **After a user enters data into the form, what happens? Does that data help a user search for more data? Does that data get saved in a database? Does that determine what already-saved data the user should see?**
After a user enters data into the form, the data gets saved into the database called sararamaFinalProject. The user should then see a list of movie names, along with directors.

* **What models will you have in your application?**
There will be a Movie model, a Director model, and an Actor model.

* **What fields will each model have?**
The Movie model will have the following fields: primary key id, name, year, genre, foreign key to Director key model id, year, and relationsihp table with the Actor model.

* **What uniqueness constraints will there be on each table? (e.g. can't add a song with the same title as an existing song)**
A user canot add a movie, actor, or director that exists in the database.

* **What relationships will exist between the tables? What's a 1:many relationship between? What about a many:many relationship?**
One to many relationship: Director table and Movie table.
Many to many relationship: Actor table to Movie table. These will need a relationship table. 

* **How many get_or_create functions will you need? In what order will you invoke them? Which one will need to invoke at least one of the others?**
I will need 3 get_or_create functions, which are the following: get_or_create_movie, get_or_create_director, get_or_create_actor. I will invoke get_or_create_movie first, get_or_create_director second, and get_or_create_actor second for each actor listed.

## The Pages

* **How many pages (routes) will your application have?**
My application will have eight routes, which are the following: see_all_movies, see_all_directors, see_all_actors, the initial form, 400 error page, 500 error page. 
The see_all_movies route will allow a user to see a list of movies in the database, along with movie characteristics of each movie, like year, genre, and director.
The see_all_directors page will show a list of directors in the database, along with the number of movies they have directed that are in the database.
The see_all_actors route will show the actors in the database.
There will be a route called movie_links that will show links to movies that are coming out; a user could click on these to see a preview of the movie in another view that calls on a dynamic route.

* **How many different views will a user be able to see, NOT counting errors?**
There will be six views. The first will allow a user to see a list of movies in the database, along with movie characteristics of each movie, like year, genre, and director. The second will how a list of directors in the database, along with the number of movies they have directed that are in the database. The third will show the actors in the database. The fourth will be a route called movie_links that will show links to movies that are coming out; a user could click on these to see a preview of the movie in another view that calls on a dynamic route.

* **Basically, what will a user see on each page / at each route? Will it change depending on something else -- e.g. they see a form if they haven't submitted anything, but they see a list of things if they have?**

## Extras

* **Why might your application send email?**
My application will send an email to a user with the information entered into the form to help them keep track of a movie they want to see as a "reminder."

* **If you plan to have user accounts, what information will be specific to a user account? What can you only see if you're logged in? What will you see if you're not logged in -- anything?**
I may want to use user authentication, but I have clarifying questions about it to ask in class on Monday.

* **What are your biggest concerns about the process of building this application?**
Can my two dynamic links be the following: the one I am using to show recommended movies and information about them, just using "return redirect(url_for((function for see_all_movies))" at any place in the application? 

Since my application is based around a user keeping a list of movies "to-watch," is there are way to implement a "remove from database" option to make it more realistic?

I think mapping out data will help me keep everything organized and the big picture clear in my head. 
