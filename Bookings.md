#Bookings

* [all()](#all)
* [get()](#get)
* [create()](#create)

all()
=========

Description:
```php
array all(array $params)
```
	Returns all bookings.
  
Parameters:

	$params - associative array of parameters:

		array(
				'lang'			=> 
				'booking_app'	=> 
				'filter'		=>	array(
											'status' => 
											'date_from' => 
											'date_to' => 
											'search' => 
											'agent' => 
										 )
				'per_page'		=> 
				'page'			=> 
				'sort'			=> 
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
							'token'				=> 
							'customer'			=> 
							'booking_dt'		=> 
							'status'			=> 
							'agent'				=> 
							'amount_customer'   => 
							'currency_customer' => 
							'amount_usd'        => 
						 )
			 )

get()
=========

Description:
```php
array get(string $id, array $params = [])
```

	Returns array.

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
				'created_at'                => 
				'status'                    => 
				'products'                  =>
				'amount_customer'           => 
				'currency_customer'         =>
				'amount_usd'                => 
			 )

create()
=========

Description:
```php
  array	create(array $data)
```  

	Creates booking.

Parameters:

	$data - associative array:

	array(
			'locale'         =>
            'timezone'       =>
            'booking_app'    => 
            'agent_token'    =>
            'currency'       =>
            'first_name'     =>
            'last_name'      => 
            'email'          =>
            'phone'          =>
            'credit_card'    => array(
										'number'     =>
										'exp_month'  =>
										'exp_year'   =>
										'cvc'        => 
										'name'       => 
									 )
            'products'       => $products,
            'expected_price' => $expected_price,
         )
  
Return Values:

	Returns array:
		
		array(
				'id'		=> 
                'products'	=>
			 )
