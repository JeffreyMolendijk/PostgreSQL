# PostgreSQL in R
A tutorial on using PostgreSQL in R. Includes database setup, table creation and extracting information using SQL queries.

## PostgreSQL and pgAdmin
![pgAdmin Logo](/img/welcome_logo.svg){:height="50%" width="50%"}

PostgreSQL is described as "The World's Most Advanced Open Source Relational Database". 
To get started with this tutorial you will need to install PostgreSQL on your computer. Please follow the detailed instruction on https://www.postgresql.org/ to get started. 
*During the installation process you will be asked for a password for the PostgreSQL root user account, which you will need to remember to connect to your databases later. 

The software "pgAdmin" will be installed as part of the installation process, which is the GUI used to monitor your databases. 

## Getting started with pgAdmin
Once you open the pgAdmin software, a new browser window will open showing your existing PostgreSQL servers, and a dashboard of your current server sessions.
To create a new database, open the servers tab and select your default server. Right click on the Databases tab and select Create > Database. In the Create-Database window that pops up enter a database name (AUSNUT in our example) and hit save. You will now see a new local database in the Databases tab.

![Database creation](/img/tutorial_1.PNG){:height="50%" width="50%"}

## Creating PostgreSQL databases using R
Creating databases using pgAdmin can be a lengthy process, where the columns and corresponding datatypes of your new database need to be entered one by one. Instead we will use R to create the structure of our new database, and send it to PostgreSQL. 
