# Notes for module dflib.rest
## RestClient


	This is the improved RESTapi interface as an class.
	

## __init__


		

## setup


		set new options in kwargs for server, host and sensor. Any or all
		may be specified.
		

## _detailedError


		build an error message and reutrn it. The exception and url are printed
		and the response object is pretty printed from the dict representation of the
		response object.
		

## _sendCommand


		Send a formatted command to the server, return the response, or
		return None on error. detailedError is called on exceptions.
		command contains the url encoded command and parameters. These are sent
		to server on port 4242.
		

## read


		get sensor data from host as json object
		

## write


		write sensor data to host as json object
		

## list


		get list of sensors on host
		

## hosts


		get a list of hosts the server knows about
		


