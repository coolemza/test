#Products

* [all()](#all)
* [get()](#get)
* [create()](#create)
* [update()](#update)
* [delete()](#delete)
* [transfer()](#transfer)

all()
========

Description:
```php
array all( array $params )
```
	Returns array.
  
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
				'params'	=> array(
										'type'		=>
										'status'	=>
										'search'	=>
									)

				'total'		=> $results['hits']['total'];
				'data'		=> array of items:
					array(
							'id'			=>
							'type'			=>
							'category'		=>
							'name'			=>
							'status'		=>
							'updated_at'	=>
						 )
			 )


get()
=========

Description:
```php
array get( string $id, array $params = [] )
```

	Returns array.

Parameters:

	$id     - product id
	$params - associative array:
		array(
                'search'		=>
                'currency'		=>
                'from'			=>
                'to'			=>
                'filter_active'	=>
			 )
  
Return Values:

	Array returned depends on product type, for external products:
		array(
				'id'			=>
				'company_id'	=>
				'supplier_code'	=>
				'type'			=>
				'category'		=>
				'score'			=>
				'relevance'		=>
				'stop_sale'		=> 
				'price'			=>
				'currency'		=>
				'name'			=>
				'thumbnail'		=>
				'extras'		=>
			)
	for dining:
		array(
				'id'			=>
				'company_id'	=>
				'status'		=>
				'type'			=>
				'supplier_id'	=>
				'supplier_code'	=>
				'supplier_data'	=>
				'category'		=>
				'stop_sale'		=>
				'updated_at'	=>
				'location'		=>
				'currency'		=>
			 )
	for activity and tour:
		array(
				'id'					=>
				'company_id'			=>
				'status'				=>
				'type'					=>
				'supplier_id'			=>
				'supplier_code'			=>
				'supplier_data'			=>
				'category'				=>
				'stop_sale'				=>
				'updated_at'			=>
				'commission_type'		=>
				'commission_margin'		=>
				'commission_multiplier'	=>
				'currency'				=>
				'inventory'				=>
				'starting_at'			=>
				'location'				=>
				'availability'			=>
			)

create()
=========

Description:
```php
array create( array $data )
```

	Returns array.


array(
      'token'         =>
      'status'        =>
      'type'          =>
      'currency'      =>
      'supplier_code' =>
      'supplier_id'   =>
      'supplier_data' =>
     )

Parameters:

	$data - associative array:
		array(
	            'token'			=>
				'status'		=>
				'type'			=>
				'currency'		=>
				'supplier_code'	=>
				'supplier_id'	=>
				'supplier_data' =>
			 )

Return Values:

	Returns associative array:

		array(
	            'id' =>
			 )

update()
=========

Description:
```php
array update( string $id, array $data )
```

	Updates product

Parameters:

	$id   - product token
	$data - associative array
		array(
                'status' =>
             )
  
Return Values:

	Returns no content or bad request on failure.
  
delete()
=========
  
Description:
```php
array delete( string $id )
```
	Returns array.

Parameters:

	$id - product token

Return Values:

	Returns no content or bad request on failure.
 
transfer()
===========

Description:
```php
array transfer( $id, $api_key )
```

	Returns array.

Parameters:

	$id -		product token
	$api_key -	api key

Return Values:

	Returns no content or bad request on failure.
