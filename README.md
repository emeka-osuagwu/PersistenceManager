
[![Build Status](https://travis-ci.org/andela-vdugeri/PersistenceManager.png?branch=master)](http://travis-ci.org/andela-vdugeri/PersistenceManager)

#Persistence Manager
Persistence Manager is a lightweight ORM based on concepts
borrowed from the laravel framework


#Testing
 The phpunit framework for testing is used to perform
 unit test on the classes. The TDD principle has been
 employed to make the application robust

 Run this on bash to execute the tests
 ```````bash
 /vendor/bin/phpunit
`````````

#Install

- To install this package, PHP 5.5+ and Composer are required

````bash
composer require verem/persitencemanager
``````

#usage

- When creating a model, PersistenceManager maps the name of the table
  to the Model name, replacing any camel cases with underscores
  and replaces it with the plural form of the word.

  ``````php
  Example
    UserRole maps to table user_roles
  ``````

- Save a record to database

````````php
$user = new User();
$user->username = "john";
$user->password = "password";
$user->email = "john@doe.co";
$user->save();
`````````
- Find a record from the database

``````php
$user = User::find($id);
``````
- Update a record

``````php
$user = User::find($id);
$user->password = "s†røngerPaSswoRd";
$user->save();
``````
- Delete a record -- returns a boolean

````````php
$result = User::destroy($id):
````````

- Find a record based on column value - Returns an object

```````
$user = User::where('username', 'john');
``````

- Find all users in the database - Returns object array
````````php
$users = User::all();
````````

## Change log
Please check out [CHANGELOG](CHANGELOG.md) file for information on what has changed recently.

## Contributing
Please check out [CONTRIBUTING](CONTRIBUTING.md) file for detailed contribution guidelines.

## Credits
PersistenceManager is maintained by `Verem Dugeri`.

## License
Persistence Manager is released under the MIT Licence. See the bundled [LICENSE](LICENSE.md) file for more details.



