#ng-json-explorer

Simple json explorer angular directive that uses raw json data as source.

This module is inspired by the firefox jsonview extenrsion made by Ben Hollis: https://github.com/bhollis/jsonview/

##Usage

Check the demo folder (demo.html) for a simple example.

#Including the required files (js and css)
```
<script src="ng-json-explorer.min.js"></script> 
<link rel="stylesheet" type="text/css" media="screen" href="ng-json-explorer.min.css" />
```

##Sending the json data to your template
```
$scope.data = {
	'name': 'Json Explorer',
	'qty': 10,
	'has_data': true,
	'arr': [
		10,
		'str',
		{
			'nested': 'object'
		}
	],
	'obj': {
		'hello': 'world'
	}
};
```

##Usage

####Using the directive to display the data

```
<json-explorer json-data="{{data}}"></json-explorer>
```

#####Using the directive to display the data from a URL

```
<json-explorer json-url="http://myurl.com"></json-explorer>
```
####Using the collapsed attribute

```
<json-explorer json-data="{{data}}" collapsed="true"></json-explorer>
```

####Using the order-by attribute (beta)

```
<json-explorer json-data="{{data}}" order-by="price:asc"></json-explorer>
<json-explorer json-data="{{data}}" order-by="price:desc"></json-explorer>
```
