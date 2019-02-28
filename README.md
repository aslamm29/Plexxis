# Plexxis Interview Exercise
## Requirements
Create a simple but __impressive__ (looks good, works well, has intuitive design, etc.) CRUD application that can do the following:

1) Retrieve employees from a REST API  - Completed
2) Display the employees in a React application  - Completed
3) Has UI mechanisms for creating and deleting employees - Completed
4) Has API endpoints for creating and deleting employees - Completed
5) Edit your version of the `README.md` file to explain to us what things you did, where you focussed your effort, etc. - Please find below as steps

*Read over the `Bonus` objectives and consider tackling those items as well*

## Bonus (Highly Encouraged)

1) Use a relational database to store the data (SQLite, MariaDB, Postgres) - Completed(Postgres)
2) UI mechanisms to edit/update employee data - Completed
3) Add API endpoint to update employee data   - Completed
4) Use [React Table](https://react-table.js.org) - Completed

## Getting Started
This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app). The front-end app runs off localhost:3000. The REST API is located in the /server folder and runs off localhost:8080. The data is being served from a JSON file located in the /server/data folder. Run `npm start` to start both servers.

## Getting it Done
* You are free to use whatever libraries that you want. Be prepared to defend your decisions.
* There is no time limit. Use as little or as much time as is necessary to showcase your abilities.
* You should fork or clone our repository into your own repository.
  * Send us the link when you are done the exercise (pglinker at plexxis dot com).

If you do well on the test, we will bring you in for an interview. Your test results will be used as talking points.  

 __This is your chance to amaze us with your talent!__

Steps implemented:

* To run code please create a postgres database as "api" with the user as "me" and password as "password

Back-End:
1. Setup a postgres dabase "api" with the user as "me" and password as "password
2. Created a queries.js controller file to handle CRUD operations (get, post, put, delete)
3. Used the index.js file as handler to route requests from the front end to the queries.js file
4. Tested the postgres database for operations on the terminal window

Front-End:
1. I used the react table library to display the contents on the web page
2. Integrated react table library into to capture the details from the postgres server using axios get
3. Plugged in redux store to get data from the postgres database using axios to load the content on the page
4. Used redux form library (for validation, errors) to enable creating new employee entries "NewEmployeeForm" and for updating the same details "EditForm"
5. Used the react router library to handle navigation between pages on click of a button between 3 Components(Table, NewEmployeeForm, EditForm)
6. Used material UI components to create a button to navigate to a form for creating new employee details
7. Navigation Flow:

src -> index.js -> app.js -> Table.js (internally navigates through buttons -> NewEmployeeForm.js, EditForm.js) 