#Api

* [setApiKey()](#setapikey)
* [getApiKey()](#getapikey)
* [setLanguage()](#setlanguage)
* [getLanguage()](#setapikey)
* [setErrorHandler()](#seterrorhandler)

setApiKey()
=========
  setApiKey(string $key)

Description:
	Set api key.
  
Parameters:
	$key - api key

Example:
	Api::setApiKey('J0iBErnbzwLz65Keupi3ZIkCkMALnr1x');

getApiKey()
=========
  string getApiKey()

Description:
	Get current api key.
  
Return Values:
	Returns api key.

setLanguage()
===========
  setLanguage(string $language)

Description:
	Set language.

getLanguage()
===========
  string getLanguage()

Description:
	Get current language.

Return Values:
	Returns current language.

setErrorHandler()
===============
  setErrorHandler(callable $callback)

Description:
	Set user error handler function.
