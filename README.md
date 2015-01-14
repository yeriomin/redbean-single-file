RedBeanPHP 4 Single File
========================

In this package there is only one file - rb.php. The one you would get by clicking [Download RedBeanPHP](http://redbeanphp.com/downloadredbean.php) on the redbean download page.

Unfortunately the composer workaround provided there does not allow creating composer packades with redbean dependency, it only allows adding redbean to your project locally.

Also, the package gabordemooij/redbean created from [the redbean github repo](https://github.com/gabordemooij/redbean) only provides a way to get the source and does not let you just require it and use. For example after `$ composer require gabordemooij/redbean` You will not be able to run the following file:

```
<?php
require 'vendor/autoload.php';
R::setup();
```

This package lets you do it.

`$ composer require yeriomin/redbean-single-file`



...Original readme:

RedBeanPHP 4 KickStart
======================

Current Build Status:
[![Build Status](https://secure.travis-ci.org/gabordemooij/RedBeanPHPKS.png)](http://travis-ci.org/gabordemooij/RedBeanPHPKS)

RedBeanPHP 4 KS is an easy to use ORM tool that stores beans directly in the
database and creates all tables and columns required on the fly.
On the other hand it allows plain SQL to search the database. In fact
RedBeanPHP is some sort of combination between document oriented database
tools like mongoDB or couchDB and traditional relational database systems
like MySQL. It offers the best of both worlds: SQL and no-SQL. You work
with no-SQL if you interact with objects will you simply turn the switch
and work with SQL if you want to do some typical database tasks like
searching or quickly grabbing something out of the data store with
specially crafted SQL. RedBean also has excellent performance because it
can freeze the database schema which means it no longer scans schemas.

The KickStart Edition of RedBeanPHP is meant for RAD, prototyping and
offers easy-to-use interfaces and a wonderful works-out-of-the-box
experience.

If you already know the power of RedBeanPHP and you would like to 
use RedBeanPHP in a more complex project or integrate RedBeanPHP in an
existing project you might find the RedBeanPHP 'Adaptive' Edition an
interesting solution.


Databases Supported
-------------------

RedBeanPHP supports MySQL/InnoDB, MariaDB/InnoDB, PostgreSQL, SQLite3 and CUBRID.

Quick Example
-------------

How we store a book object with RedBeanPHP:
```php
$book = R::dispense("book");
$book->author = "Santa Claus";
$book->title = "Secrets of Christmas";
$id = R::store( $book );
```

Yep, it's that simple.

This Github account is for development only.
If you want to use RedBeanPHP 4 KickStart please visit the website and
download the ALL-in-ONE PHAR file. This should work out-of-the-box
with no configuration at all.

More information
----------------

For more information about RedBeanPHP please consult
the RedBeanPHP online manual at:

http://www.redbeanphp.com/
