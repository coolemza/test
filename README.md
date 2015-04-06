#Dashboard

class Dashboard

* [summary](#summary)
* [summaryByDate](#summaryByDate)

summary
=========
  array summary()

Description:

	Returns summary information.
  
Return Values:

	Returns an associative array containing the following elements: products, profit and reservation.

Example:

	$results = Dashboard::summaryByDate('2015-04-06');
	print_r($results);

The above example will output:

	Array
	(
		[products] => Array
			(
				[ACTIVE] => 129298
				[INACTIVE] => 70
			)

		[profit] => Array
			(
				[today] => 0
				[yesterday] => 0
				[last_7_days] => 0
				[last_30_days] => 0
			)

		[reservations] => Array
			(
				[sold] => 0
				[pending] => 0
				[cancelled] => 3
				[declined] => 0
			)

	)

summaryByDate
=========
  array summaryByDate(string $date)

Description:

	Returns array of summary for given date.

Parameters:

	$date - A date string. 
  
Return Values:
	Returns an associative array containing the following elements: sold_products, profit and active_products.

Example:

	$results = Dashboard::summaryByDate('2015-04-06');
	print_r($results);

The above example will output:

	Array
	(
		[sold_products] => 0
		[profit] => 0
		[active_products] => 129298
	)
