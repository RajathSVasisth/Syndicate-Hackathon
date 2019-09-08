# Syndicate-Hackathon
>This repository contains all encryption as well as flask web- app files required for hosting and running a web url.		
>The website is already hosted on rajathsv.pythonanywhere.com along with an active database.
>But for recognising the internal structure of how the encrytion scheme encrypts passwords and how the web-app
 and the encryption schemes are inter-connected, the following is to be done to run the app on a local-host.
 >First of all make sure you have the latest python running on your system. (3.5 and above)
 >pip install the following libraries to run the app:-
              >pip install PyCrypto
              >pip install flask
              >pip install flask-bootstrap
              >pip install flask-sqlalchemy
              >pip install flask-wtf
              >pip install flask-login
 >After downloading the above folder, in the app.py file change the sqlite database storage location to
  where ever the user had downloaded the web app folder and save it. Specific instructions have been given
  as comments in the app.py file itself.
 >Next step is to create a database to store encrypted user information. Go to terminal and type in the following commands:-
              >cd "path of whichever directory the files are in"
              >sqlite3 database.db
              >.tables      
              >.exit    /*To exit from the database*/
              /*Now go to python in your terminal*/
              >python
              >from app import db
              >db.create_all()     /*to create a user table for storing user signup info*/
              >exit()
 >Now the database is created. The next step is to run the web application on a local host:-
              /*go to terminal in the specific directory*/
              >python app.py
 >Now copy the url of the local-host server and paste in google chrome or any other web browser.
 >Now in the website Sign Up with suitable username, email and password.
 >The Sign-up data has now been sucessfully stored in database in aes-ecc + hashed (256 bit) encrypted format.
  To see how it is stored:-
              /*quit from the running server in Terminal and type in the following*/
              >sqlite3 database.db
              >select * from user;
              /*The encrypted login information will be displayed*/
              >.exit
 >Now run the app back and go to the url and try logging in with previous signup details after which you
  will be sucessfully guided to the dashboard containing a demo of netbanking options will be displayed.
  Thus generating a very secure method for making internet banking transactions.
