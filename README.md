Question: Orchestration API to load data from the external dataset into local in-memory DB, and
then provide REST endpoints to fetch the users based upon various user criteria.
Category: Backend API
Tags: Users API, Load In-Memory DB, REST API
DataSet: https://dummyjson.com/users
Spend time to go through the dataset and understand the the 3rd party API’s
https://dummyjson.com/users response payload that needs to be loaded into the in-memory H2
DB
Go through the below references to understand the in-memory H2 database, which will need to
be integrated in the API implementation: https://www.baeldung.com/spring-boot-h2-database
and https://initializ.io/blogs/create-crud-rest-api-with-h2-database-and-jpa-with-spring-boot-in-
under-15-min/
Go through the below reference to understand free text search implementation, which will be
required in the API implementation: https://www.baeldung.com/hibernate-search
Write a RESTful API endpoint to load all the users data from the dataset to in-memory H2 DB.
Expose the following RESTful API endpoints to retrieve data from the in-memory H2 DB:
a. List all users based on free text search on the users firstName, lastName and ssn
b. Find a specific user by id or email
Expectations:
1. The code should follow clean code practices
a. Modular
b. Application Logging
c. Exception Handling
d. Environment Layering
e. Input Data Validations
f. Unit testcases & Code Coverage
g. Externalized config parameters, if any
h. README.md file to describe the API and steps to build and run it
2. The call to the 3rd party https://dummyjson.com/users should be optimized
3. The call to the 3rd party https://dummyjson.com/users should be resilient
4. The APIs should follow REST standards for fetching the users from in-memory DB
5. The REST APIs should be documented using Swagger/OpenAPI plug-ins
 
Question: Develop a frontend based upon ReactJS/AngularJS to perform a free text search of the
users in the backend and display on the web UI, with client-side sorting and filtering.
Category: Frontend UI
Tags: Users UI, REST API
PreCondition: “Users Question for Backend – 006” has been solved and the REST API endpoints to
fetch the users on various criteria are working.
Develop the frontend app to display a global search bar (just like the one on the Google.com home
page) on the default page.
The frontend user should be allowed to enter the user’s firstName and/or lastName and/or ssn.
Upon entering the first 3 characters, when the user clicks on the enter key or clicks on the search
icon in the search bar, the frontend app calls the backend API, which in turn makes the free text
search to fetch all the users matching the partial text entered by the user.
The frontend should display the users in a grid format on the list/default page. Pick and choose the
user’s attributes to be shown.
User should be able to sort the grid results at client-side (i.e. without making any backend API call)
based upon age in ascending or descending order.
User should be able to filter the grid results at client-side (i.e. without making any backend API call)
based upon role.
Fire your imagination to design the UI pages.
Expectations:
1. The code should follow clean code practices
a. Atomic design
b. Exception Handling
c. Environment Layering
d. Unit testcases & Code Coverage
e. Externalized config parameters, if any
f. README.md file to describe the frontend and steps to build and run it
2. The frontend UI app should be developed as single page app.
3. The frontend UI app should demonstrate the responsive design features.
4. The frontend UI app should demonstrate lazy loading techniques, as applicable

{"users":[{"id":1,"firstName":"Emily","lastName":"Johnson","maidenName":"Smith","age":28,"gender":"female","email":"emily.johnson@x.dummyjson.com","phone":"+81 965-431-3024","username":"emilys","password":"emilyspass","birthDate":"1996-5-30","image":"https://dummyjson.com/icon/emilys/128","bloodGroup":"O-","height":193.24,"weight":63.16,"eyeColor":"Green","hair":{"color":"Brown","type":"Curly"},"ip":"42.48.100.32","address":{"address":"626 Main Street","city":"Phoenix","state":"Mississippi","stateCode":"MS","postalCode":"29112","coordinates":{"lat":-77.16213,"lng":-92.084824},"country":"United States"},"macAddress":"47:fa:41:18:ec:eb","university":"University of Wisconsin--Madison","bank":{"cardExpire":"03/26","cardNumber":"9289760655481815","cardType":"Elo","currency":"CNY","iban":"YPUXISOBI7TTHPK2BR3HAIXL"},"company":{"department":"Engineering","name":"Dooley, Kozey and Cronin","title":"Sales Manager","address":{"address":"263 Tenth Street","city":"San Francisco","state":"Wisconsin","stateCode":"WI","postalCode":"37657","coordinates":{"lat":71.814525,"lng":-161.150263},"country":"United States"}}
 
 
 

