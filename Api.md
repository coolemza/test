#Api

* [setApiKey()](#setapikey)
* [getApiKey()](#getapikey)
* [setLanguage()](#setlanguage)
* [getLanguage()](#setapikey)
* [setErrorHandler()](#seterrorhandler)

setApiKey()
=========

Description:
  
	setApiKey(string $key)

	Set api key.
  
Parameters:
	$key - api key string

Example:
```php
	Api::setApiKey('J0iBErnbzwLz65Keupi3ZIkCkMALnr1x');
```

getApiKey()
=========

Description:
  
	string getApiKey()

	Get current api key.
  
Return Values:
	Returns api key string.

Example:
```php
	$apiKey = Api::getApiKey();
	print_r($apiKey);
```

The above example will output:

	J0iBErnbzwLz65Keupi3ZIkCkMALnr1x

setLanguage()
===========

Description:

	setLanguage(string $language)

	Set language.

Parameters:

	$language - language tag
	
Example:
```php
	Api::setLanguage('en');
```

getLanguage()
===========

Description:
	string getLanguage()

	Get current language.

Return Values:
	Returns current language.

Example:
```php
	$language = Api::getLanguage();
	print_r($language);
```

The above example will output:

	en

setErrorHandler()
===============

Description:
	setErrorHandler(callable $callback)

	Set user error handler function.
