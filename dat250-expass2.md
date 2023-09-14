# Expass 2

1. Technical problems that I encountered during installation and use of Java Persistence Architecture (JPA) and how I resolved them:
   I did not encounter any problems during installation. The only problem I encountered during the experiment was that when creating getters for the objects I did not realize that the JPA would return Objects
   of class PersistanceBag. Because of this the tests did not pass because they expected an Immutable collection set. To fix this I simply returned a hash set in the getters.

2. Link to code for experiment 2:
   [https://github.com/Maloha7/dat250-jpa-tutorial](https://github.com/Maloha7/dat250-jpa-tutorial)

3. Answer to questions and how I inspected the database tables.
   - Where is the database? Explain the used database and how/when it runs.
     - The database is an embedded h2 database that runs locally. It runs when the main function of the application is running and stores the data to a local file on my computer.
   - The SQL used to create the table Customer. To find this I enabled thow SQL in persistence.xml
       - ```SQL
         create table Customer (
         id bigint generated by default as identity,
         name varchar(255),
         primary key (id)
         )
         ```
4. I found no easy way to inspect the database tables because the provided template used a short-lived locally embedded h2 database.
   When looking online all of the solutions I could find suggested that I needed to connect to the database either from the terminal or from the h2 web console.
   However since the database was short-lived I could not find a way to connect to the the database from an external source.

   My solution to this was to copy all the SQL statements made by hibernate and convert them to a MySQL syntax. Then I could paste the SQL statements into [dbdiagram.io](https://dbdiagram.io/d)

   Screenshot:
   ![Screenshot of database schema](/public/database.jpg?raw=true)

   The created tables did correspond to my initial thoughts regarding the exercise. I did anticipate there being coupling tables to dissolve the manyToMany relationships between the tables.

6. I do not have any pending issues with this assignment that I did not manage to solve.