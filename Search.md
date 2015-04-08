#Search

* [get()](#get)
* [create()](#create)
* [update()](#update)

get()
=========

Description:
```php
array get( string $id, array $params = [] )
```

Parameters:

	$id     - search context id
	$params - associative array:
		array(
				'currency'	=>
				'filter' =>
				'sort' =>
				'search' => $this->value
	            'per_page' => $this->per_page,
				'page' => $this->page
			 )
  
Return Values:

	Returns associative array:

		array(
				'search_progress'	=> array(
												'done' =>
												'total'=>
											)
				'params'			=> array(
												'per_page'      =>
												'page'          =>
												'sort'          =>
												'currency'      =>
												'type'          =>
												'status'        =>
												'search'        =>
												'starting_at'   =>
												'dates'         =>
												'category'      =>
												'price'         =>
												'rating'        =>
												'price_range'   =>
											)

				'search'			=>
				'total'				=>
				'counts				=>
				'data'				=> array of items:
										array(
												'id' => $s['token'],
												'company_id' => $s['company']['token'],
												'provider' => $s['supplier_code'],
												'type' => $s['type'],
												'category' => $s['category'],
												'distance' => isset($f['distance'])? $f['distance'][0] : null,
												'starting_at' => $s['starting_at'],
												'price_range' => isset($s['price_range'])?$s['price_range']: null,
												'currency' => $s['currency'],
												'name' => $f['name'][0],
												'thumbnail' => $s['thumbnail'],
												'extras' => isset($s['extras']) ? unserialize($s['extras']) : '' ,
											 )
			 )


create()
=========

Description:
```php
array create( array $data )
```  

	Create search

Parameters:

	$data - associative array:
		array(
				'from'		=>
				'to'		=>
				'adults'	=>
				'children'	=>
				'location'	=> array(
										'latitude'	=>
										'longitude' =>
										'address'	=>
								    )
             )
  
Return Values:

	Returns associative array:

		array(
	            'id' =>
			 )

update
=========

Description:
```php
array update( string $id, array $data )
```

	Update search (only for vehicle)

Parameters:
	$id   - search id
	$data - should be merged array of current search context and updated fields
	        call Search::get() to obtain current search context, resulted array will have field 'search' that can be used as search context
			updated fileds is array like this:
				array(
						'vehicle'	=> array(
												'location_from' => array(
																			'latitude'  =>
																			'longitude' => 
																			'address'   => 
																		)
												'location_to'	=> array(
																			'latitude'  => 
																			'longitude' => 
																			'address'   => 
																		)
												'date'          => 
												'time'          =>
												'time_origin'   =>
												'distance'      =>
												'duration'      =>
												'full_time'     =>
											)
					)

Return Values:

	Returns associative array:

		array(
	            'id' =>
			 )
