# Code Hawk Meeting Minutes 10/28 #

**Goal of the Meeting:** Run OBD-II script, debug any issues, start filling database with info

The backend team convenend in the one of our cars (a Dodge Charger) to test the 
[OBD python](https://python-obd.readthedocs.io/en/latest/) library directly with the OBD-II. 
We ran into some errors that had to do with inserting the read-in data into our database. 
After creating a new database and lengthening the varchar values for the data and description variables, 
the python script ran without any errors, and live data was sent into the database `car` to be stored in a 
table called `car_info`. This was a major milestone in our process thus far; we can now confirm that we can 
read in the data from the OBD-II, parse it appropriately, and save it to our database. And we have the ability 
to provide data for ~200 conditions, including (but not limited to) engine health, air health, pressure levels, 
and fuel related information. 

**Future Work:** 
We'd like each user to have at least two tables associated with their ID - one that contains the history of data 
they've already collected, and one that contains live data. We'd also like to explore the option of having an 
asynchronous table for the live data. Furthermore, we'd like another table that holds the all the user information 
for every single user - their specific ID, username, password, and car model. These will be asked for in the login 
page and stored in the car database.

Our next steps are to create and fill these tables within our database, and then begin to integrate our front-end 
and back-end with node.js. 
