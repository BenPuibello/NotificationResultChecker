# NotificationResultChecker
Program to check for failed notifications in a OnBase system.  Against the OnBase Database

This application polls the hsi.distributionhist table, specifically looking for a -1 value in the requeststatus.  Once it finds that it will be printed on the text file.  What you choose to do with the text file is up to you.  Program can modified to output the data in different formats.

Program variables stored in app.config:

1) 'StartingDistNum' = this is the row the application starts with checking.  It will continue ascending up the rows on the table until it hits the last row.  The program then ends and stores that most recent row to continue excution where it left off next time it is started.

2) 'FileOutputLocation' = This is the file directory where the output file will be produced.  It is this file that displays failed notifications.  When the program runs, if a file is already located there it will append the data.  If there isn't a file then it will create a new one.  No data will be overwritten. 

3) 'Filename' = the name of the output file produced.

4) 'dbConnection' = This is the connection to the database.

You must cconfigure 1, 2, 4 for your system.    

