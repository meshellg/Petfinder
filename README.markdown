What is Petfinder?
==================
Petfinder is an online, searchable database of animals who need homes. This PHP Client Library helps developers build applications using the Petfinder.com API.


Why use this Petfinder.com PHP Client Library?
==============================================
* You want to build a website or application using Petfinder.com data
* This library has been used to build actual applications, namely CuteAdoptablePets.com


Getting Started
===============

* Download Petfinder.php
* Get a developer API key from http://www.petfinder.com/developers/api-key
* Save this PHP code and run it:

__Get a random pet's basic info__

	// Set $apiKey to your API key string.
	// Both XML and JSON responses are available
	include('Petfinder.php');
	$pf = new Petfinder(PETFINDER_API_KEY);
	$pf->setResponseFormat('json');
	$petJson = $pf->pet_getRandom(array('output'=>'basic'));
	$pet = json_decode($petJson, TRUE);
	print_r($pet);