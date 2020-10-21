Following are the functionalities supported in this project:-

1. CRUD Operation for Account Application and User Application
2. Creating an Account using Rest URI Post method((createAccountWithUser)http://localhost:8883/accountApp/account) will create User and it's role as well in the DB.
3. Account and Customer are two microservices. Account application gets the user details using rest calls to Customer microservice using ServiceDiscovery.
4. DB exists on Customer application only and Account application communicates through rest to get the customer details.
5. JWT is implemented to authenticate the user created. Below are the steps to test it.
	i. First create the account using the REST API URI: http://localhost:8883/accountApp/account (POST)
	ii. Now Create JWT token using authenticate API URI: http://localhost:8883/accountApp/authenticate (POST). This response of this API will be the JWT Token
	iii. Provide the above created JWT token in the header as Authorization header like Bearer <JWTTokenString>.
	Now by using the JWT token, one can access the rest of the Account app APIs i.e. (getAccounts)http://localhost:8883/accountApp/accounts