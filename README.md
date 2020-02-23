# Your-Accountant
The Your Accountant application is developed by using android studio. Android Studio is the official Integrated Development Environment (IDE) for Android app development, based on IntelliJ IDEA. And some java techniques also had to use. make database with SQLite.


Minimum Requirement
 Android Version: 6.0 Android Marshmallow
 Minimum Screen Density: not important.

Required Permissions
 Not need internet


SQLiteOpenHelper

 It is a subclass which is used to create database. 
 In the constructor, it is called through super,
providing it with the name of the database and the current version. 
 There is requirement of overriding two methods : 

1. OnCreate() – Which is called by the system if the database does not exists. 
2. OnUpgrade()– Called when the version number changes. 

 Access to the database is obtained through two methods: 

1. getReadableDatabase : Accesses the database in the read – only mode.
2. getWritableDatabase : Accesses the database in the writable mode.
3. Both methods return a SQLite Database instance. SQLiteDatabase 

 Once the database is created or connected to ,we can use the instance of SQLiteDatabase to access it. 
 It also provides the method to open , query , update and close the database.
 We can execute any SQL statement using execSQL(String query). 
 There are also insert( ) , update( ) , delete( ) methods.
 It also provides rawQuery( ) and query( ) :

1. rawQuery accepts a raw SQL query with replacement parameters.
2. query provides a structured interface.



Queries return an object of type Cursor :

1. getCount( ) – returns the number of rows. 
2. moveToFirst( ) , moveToNext() – to navigate the rows. 
3. isAfterLast( ) – to find the last row.
4. get(column index) : getString , for example : the column index is the number of the column. 
5. Close( ) – Cursor objects must always closed.

CursorAdapter 

1. It is a convenience class to allow the use of a database cursor as a ListAdapter. 
2. It allows to set a layout for the rows of a ListView. 
3. It maps the columns in the SQL table to the views in the list item layout.
Fragments A Fragment represents a behavior or a portion of user interface in a FragmentActivity. You can combine multiple fragments in a single activity to build a multi-pane UI and reuse a fragment in multiple activities. You can think of a fragment as a modular section of an activity, which has its own lifecycle, receives its own input events, and which you can add or remove while the activity is running (sort of like a "sub activity" that you can reuse in different activities).


