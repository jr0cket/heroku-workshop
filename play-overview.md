


## Routes 
routes are mapped to controllers and are all type safe 


## starting the play app

compiling the app, downloading the dependencies, 

runs in development mode 

uses SBT to manage the build and run cycle 

activator & play are based on SBT, they are tasks for SBT


## Evolution 

if you get an evolution error on the web page when first run you should see a button to fix the issue.


*.scala.html is compiled 

your templates are compiled so they are type safe 


## reverse routing 

we give a method and do a reverse lookup and come up with the url path 

so if you change your routes file, you dont need to change your code.

so play framework uses the classic press a button and navigate to a new page (compared to a 1-page app with Angular)


## forms

userReservationForm is inside a case class in Scala, mapped using apply and unapply 

field level evaluation 
form level evaluation

## Slick - typesafe orm

## application.conf 
secret used for session managment 

## evolution 
managing database migrations and schema changes 
- using sql to manage the database schema within the codebase 

java - flyweight 
