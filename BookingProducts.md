#BookingProducts

* [all()](#all)
* [get()](#get)
* [update()](#update)

all()
=========

Description:
```php
	array all( array $params )
```
	
	Returns all booking products.
  
Parameters:

	$params - associative array:
		array(
				'lang'		=>
				'company'	=>
				'filter'	=> array(
										'status'	=>	
										'date_from'	=>	
										'date_to'	=>	
										'search'	=>	
									)
				'per_page'	=>
				'page'		=>
				'sort'		=>
			 )

Return Values:

	Returns associative array:

		array(
				'total'		=> total items
				'params'	=> array(
										'page'		=> 
										'per_page'	=> 
									)
				'data' => array of pages, where page item is:
					array(
							'token'             =>
							'customer'          =>
							'name'              =>
							'trip_dt'           =>
							'booking_dt'        =>
							'destination'       =>
							'status'            =>
							'currency'          =>
							'amount_customer'   =>
							'currency_customer' =>
							'amount_supplier'   =>
							'currency_supplier' =>
							'amount_usd'        =>
						 )
			 )

get()
=========

Description:
```php	
	array get( string $id, array $params = [] )
```
	Returns booking products by token.

Parameters:

	$id     - booking token;
	$params - associative array of parameters:
		
		array(
				'lang' =>
			 )

Return Values:

	Returns associative array:

        array(
				'token'                     =>
				'customer_name'             =>
				'customer_phone'            =>
				'customer_email'            =>
				'credit_card_type'          =>
				'credit_card_last_four'     =>
				'credit_card_exp_month'     =>
				'credit_card_exp_year'      =>
				'order_number'              =>
				'booking_dt'                =>
				'thumbnail'                 =>
				'name'                      =>
				'date'                      =>
				'time'                      =>
				'tz'                        =>
				'status'                    =>
				'items'                     =>
				'notes'                     =>
				'balance'					=> array(
														'amount_supplier'       =>
														'currency_supplier'     =>
														'amount_usd'            =>
														'fee'                   =>
														'profit'                =>
													 )
            )

update()
===========

Description:
```php
	array update( $id, array $data )
```	
	Update booking products

Parameters:
	$id		- booking products token
	$data	- associative array:

		array(
				'status' =>
			 )

Return Values:

	Returns array:
		
		array(
				'token'		=> 
                'status'	=>
			 )
