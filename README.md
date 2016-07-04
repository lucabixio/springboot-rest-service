# springboot-rest-service
## Create a simple Hello World REST Web Service
Publish a RESTful Web Service where the following Web Methods are available:
* ```http://<webserver_add>:<webserver_port>/greeting``` (e.g., http://localhost:8080/greeting).
* ```http://<webserver_add>:<webserver_port>/greeting?name=<your_name>``` (e.g., http://localhost:8080/greeting?name=Luca)
* ```http://<webserver_add>:<webserver_port>/greeting/{name}``` (e.g., http://localhost:8080/greeting/Luca)

The output of the calls has to be:
* ```{"id":22,"content":"Hello, World!"}```
* ```{"id":23,"content":"Hello, Luca!"}```
* ```{"id":24,"content":"Hello, Luca!"}```

respectively. Please note that the attribute "id" has to be incremented at each call.

Create a test case to test both the Web Methods provided by the REST Web Service.


## Hints:
Publish a RESTful Web Service.
* Use the wizard "Spring Starter Project" available in Eclipse STS.
* Create a POJO to create the response and to maintain the status (i.e., the incremental "id" attribute. Have a look at ```incrementAndGet#AtomicLong```).
* Create the Web Service using the Spring Annotations. Use ```@RestController```, ```@RequestMapping```, ```@PathVariable``` and ```@RequestParam``` to create the Web Service and the Web Method.

Create a test case ```@WebAppConfiguration```, ```@Autowired```, ```WebApplicationContext``` and ```MockMvc``` classes;