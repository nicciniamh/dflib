# Notes for module dflib.rest
## RestClient
**Encapsulate RESTful API**
	

## class RestClient(object):
### `_init__(server=server,host=host,sensor=sesor)`

	
	kwargs:
		server - the server to connect to
		host - the host on which the sensor resides
		sensor - the sensor to interact with

		

### `RestClient.setup(server=server,host=host,sensor=sesor)`

	set new options in kwargs for server, host and sensor. Any or all
	may be specified.

	kwargs:
		server - the server to connect to
		host - the host on which the sensor resides
		sensor - the sensor to interact with
	

### `RestClient.read()`

		get sensor data from host as json object
		

### `RestClient.write(data)`

		write data to sensor as json object
		

### `RestClient.list`

		get list of sensors on host
		

### `RestClient.hosts`

		get a list of hosts the server knows about
		
