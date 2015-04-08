#Inventory

* [get()](#get)
* [getCalendar()](#getcalendar)

get()
=========

Description:
```php
array get( string $date, array $params )
```
	Returns inventory.

Parameters:

	$date - date string. 
	$params - associative array of parameters:
		array(
				'lang'	=>
				'sort'	=>
			 )
  
Return Values:

	Returns array:

		array(
	            'params' =>
				'data' => array(
									'products'	=> array of items:
										array(
												'id'		=>
												'sku'		=>
												'name'		=>
												'type'		=>
												'category'	=>
												'times'		=> array of items:
													array(
															'time'		=>
															'booked'	=>
															'capacity'	=>
															'status'	=>
														 )
											 )
									'counts'	=> array(
															'label' =>
															'count' =>
														)
								)
                        
			 )

getCalendar()
=========

Description:
```php
array getCalendar( array $params )
```

	Returns calendar.

Parameters:

	$params - associative array:
		array(
				'year'	=>
                'month'	=>
                'lang'	=>
			 )
  
Return Values:

	Returns associative array:

		array(
	            'params'	=>
				'data'		=> array of items:
					array(
							'date'      =>
							'summary'   =>
						 )
			 )
                'type'      => $product->type,
                'id'        => $product->token,
                'sku'       => $product->sku,
                'category'  => $product->category,
                'name'      => $name,
                'inventory' => $inventory
