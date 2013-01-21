PHP-MySQLi-Wrapper
==================

Introduction
------------

This is a Singleton PHP wrapper that utilizes the PHP [MySQLi] class. It is meant to be non persistant, e.g., You must connect, perform the queries you need and then disconnect when you're finished.

API Methods
-----------

`Database::connect()` - Connects to the database
`Database::disconnect()` - Disconnects from the database
`Database::query()` - Performs an "advanced" query and gets the results if needed
`Database::get()` - Gets information from the database
`Database::where()` - Specifies a where clause for the action you perform.
`Database::update()` - Updates information from the database
`Database::delete()` - Deletes information from the database
`Database::insert()` - Inserts information into the database
`Database::instance()` - Gets the once-instantiated instance of this class
`Database::num_rows()` - Gets the number of rows for `Database::get()` command without actually returning the data

Example Usages
--------------

Adding some data into a table.
    $data = array( 'foo' => 'bar' );
    Database::connect();
    Database::where( 'foobar', true );
    Database::insert( 'my_table', $data );
    Database::disconnect();

[MySQLi]: http://php.net/mysqli