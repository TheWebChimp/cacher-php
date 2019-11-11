cacher-php
=============

A simple, general-purpose, file-based cache provider

### Basic usage

```php
<?php
	// You'll need a folder named 'cache' on the same folder of this file with write permissions
	$stuff = Cacher::getFromCache('stuff', 900);
	if (! $stuff ) {
		$stuff = performTimeConsumingTaskToRetrieveTheStuff();
		Cacher::saveToCache('stuff', $stuff);
	}
?>
```

###Licensing

This software is released under the MIT license.
