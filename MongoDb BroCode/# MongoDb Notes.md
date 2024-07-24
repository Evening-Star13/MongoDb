# MongoDb Notes

<hr>

## Opening MongoDb

mongosh => this will open mongo shell in the terminal
open Compass from Desktop => this will open Compass
<hr>

## Create Database

use.name of folder => this will create a folder if one is not there(use.students)
<hr>

## Show Data List

db.students.find() => this will list all data in database
<hr>

## Create Data

db.student.insertOne({}) => this will add one item to database ({Name:"Chris Barranger", Age:52, Profession:"Software Engineer"})
db.students.insertMany({},{},{}) => this will add many items to database ({Name:"Rebecca Harris", Age:43, Profession:'Marketing Administration'},{Name:"Jaide Barranger", Age:20, Profession:"Surgeon"},{Name:"Ethan Barranger", Age:17, Profession:"Gamer"})
<hr>    

## Sort & Limit

db.students.find().sort() => this will sort ascending or descending => db.students.find().sort(Name:1) (ascending) or (Name:-1(descending))
db.students.find().limit() => this will limit the number of items returned => db.students.find().limit(5)
db.students.find().sort().limit => this will sort and limit the items returned
<hr>

## Projection

db.students.find({Name:"Chris Barranger"}) => this will tighten up the search in the database
db.students.find({},{_id:false,Name:true,Occupation:true}) => this will return the list with just Name and Occupation
db.students.find({},{_id:false,Name:true}) => this will return the list with just Name
the same is done in Compass as above in "Options" and then "Project"
<hr>
