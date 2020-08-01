# quizapp_webapplication
springboot web_application
-----------------------ZONIX QUIZAPP-------------------------

Finally our first SpringBoot real world application is here. 
This is a basic quiz app where you can register as an user and login as a user or admin.
User can attend several quizes provided by admin.
Admin can add quizes questions within the quiz and also can update them.

----------------------DEVELOPERS INVOLVED----------------------
1. ANIK CHATTERJEE (github link : https://github.com/starboi2000)
2. CHANDRACHUR CHATTERJEE (github link : https://github.com/chandrachur-chatterjee)
3. ANIK CHAKRABORTY (github link : https://github.com/anik2131)


----------SOFTWARES / TOOLS REQUIRED TO RUN THIS WEBAPP--------
1. SPRING STS 4.7.0 RELEASE.
2. MY SQL AND MY SQL WORKBENCH.
3. ANY WEB BROWSER.

----------STEPS TO RUN THIS WEBAPP----------
1. Set the username of mysql-workbench as:"root" and password as :"1234"
2. Go to MySql Workbench and write the following query : "CREATE DATABASE quizproject;"
3. DOWNLOAD THE RAR FILE FROM THE GITHUB AND EXTRACT IN ANY LOCAL STORAGE.
4. OPEN SPRING STS , GO TO FILE > IMPORT > EXISTING MAVEN PROJECTS . SELECT THE FOLDER IN WHICH YOU HAVE EXTRACTED THE FILES.
5. ONCE THE PROJECT IS LOADED , IN THE PACKAGE EXPLORER (LEFT HAND SIDE OF THE STS SOFTWARE) CLICK ON "ZONIX-QUIZAPP" , 
          GO TO src/main/java > com.anik.springboot , Right Click on ZonixQuizappApplication.java and select Run As > Java Application.

6. Once the project is successfully started , Go to your browser and type the url "http://localhost:8080/home" and your application will start working.
7. To access the admin portal the userid is ADMIN-007 and password is ANIK-CHANA.s

---------------IF ERRORS EXISTS--------------

IF YOU ARE FACING ANY ERROR LIKE "TABLE NOT CREATED" THEN  COPY THE BELOW QUERY AND PASTE IT INTO THE MYSQL WORKBENCH:

QUERY:
USE quizproject;
CREATE TABLE quiz(quizid varchar(50) primary key , quizname varchar(100) , quizdetails varchar(950)); 
CREATE TABLE question(id bigint primary key , quizid varchar(50) , questionid varchar(50) , questiondetails longtext , correctanswer varchar(150));
CREATE TABLE options(quizid varchar(50) , questionid varchar(50) , optionid bigint primary key , option value varchar(150));
CREATE TABLE userdetails(userid varchar(50) primary key , username varchar(50) , useremail varchar(50) , userphone bigint , userpassword varchar(150), logintoken);
CREATE TABLE previousattempts(userid varchar(50) , quizid varchar(50) primary key , date varchar(950) , score varchar(50));
