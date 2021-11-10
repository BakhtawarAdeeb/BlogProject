In this project I have used angular, Spring boot and MySql.
Tools/IDE used for this project are: 
⦁	STS for spring boot
⦁	Visual code for angular
⦁	XAMP anf mySQL Workbench for database
On Spring Boot side:
⦁	For authenetication have implemented JWT token. When a user login to our application we generate a JWT response after that whenever a request is send to the server it is filtered and we look for the authorization header.
⦁	For authorization we are using Granted authorities list in the User Details Implementaion.

On angular side we are using:
⦁	We store the Jwt token we got from Spring Boot into the Session storage. And whenever we are sending request to the the backend we get token from the session storage and add it to our request by using HTTP Interceptor.
⦁	When we logout we romove the token from the session storage.

I have attached my Sql script with the project.
My database name is code and it contain three tables (users, mypost, mycomments)

The credential for admin are:
username: bakhtawar
Password: 12344321

The credential for simple user are:
username: helloo
Password: 33443344

When a new user will signup it will be by default saved as a user. If you want to save him as an admin you have to manually set roles as "ROLE_ADMIN" in AuthController.java when the user is being created (in registerUser function)
