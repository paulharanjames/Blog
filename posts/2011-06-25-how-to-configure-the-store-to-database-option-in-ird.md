
Here is what to do:

1. Run Sql script against configuration Database. [ird\_create\_tables_sql](http://ctiworld.files.wordpress.com/2011/06/ird_create_tables_sql.doc)

2. Created a New DBServer Application in CME

3. Installed DB Server (As a Client of Configuration server)

4. Created New Database Access Point, which uses new DBServer

5. In IR Designer I made a connection to the Database Access Point

6. Database access Point needs to point to the Configuration Database (Or where you ran the Script)

NOTE:

You do not have to create a New DBServer, you can use the existing one.