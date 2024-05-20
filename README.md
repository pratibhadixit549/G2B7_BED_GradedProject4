
# Employee Managemnent - Rest API
<br>
<br>

## GET Requests:

| HTTP Method | URL Path | PostMan Body | Authorization Required | User Role Allowance | Description | 
| ------------- | ------------- | :-------------: | ------------- | :-------------: | ------------- |
| `GET`   | localhost:8080/api/employees     | -    | No accessible to all   | All allowed     | To fetch all employees    |
| `GET`   | localhost:8080/api/employees/5     | -    | No accessible to all   | All allowed     | To fetch all employees by Id    |
| `GET`   | localhost:8080/api/employees/sort?order="asc"     | -    | No accessible to all   | All allowed     | To fetch all employees in increasing order of their firstName    |
| `GET`   | localhost:8080/api/employees/sort     | -    | No accessible to all   | All allowed     | By default sort by firstName    |
| `GET`   | localhost:8080/api/employees/sort?sortBy=firstName     | -    | No accessible to all   | All allowed     | Sort by firstName    |
| `GET`   | localhost:8080/api/employees/sort?pageSize=2     | -    | No accessible to all   | All allowed     | Fetch by pageSize    |
| `GET`   | localhost:8080/api/employees/sort?pageSize=2&sortBy=lastName     | -    | No accessible to all   | All allowed     | Sort by lastName along with pageSize    |
| `GET`   | localhost:8080/api/employees/sort?pageNo=0&sortBy=lastName     | -    | No accessible to all   | All allowed     | Sort by pageNo and lastName   |
| `GET`   | localhost:8080/api/employees/sort?pageNo=0&sortBy=lastName&pageSize=3     | -    | No accessible to all   | All allowed     | Sort by lastName along with pageNo and pageSize    |
| `GET`   | localhost:8080/api/employees/firstName/sita     | -    | No accessible to all   | All allowed     | To fetch all employees by firstName     |
| `GET`   | localhost:8080/api/roles     | -    | No accessible to all   | All allowed     | To fetch all roles    |
| `GET`   | localhost:8080/api/users     | -    | No accessible to all   | All allowed     | To fetch all users   |

<br>
<br>

## POST Requests:

| HTTP Method | URL Path | PostMan Body | Authorization Required | User Role Allowance | Description | 
| :-------------: | ------------- | ------------- | ------------- | ------------- | ------------- |
| `POST`   | localhost:8080/api/auth/signin     | {<br>&nbsp;&nbsp; "userName" : "Admin",<br>&nbsp;&nbsp; "password" : "Admin"<br>}  | No accessible to all   | All allowed     | SignIn/LogIn for access token    |
| `POST`   | localhost:8080/api/employees/create     | {<br>&nbsp;&nbsp;"userName" : "Admin",<br>&nbsp;&nbsp;"password" : "Admin"<br>}  | Yes  | ADMIN : Permitted <br> MANAGER : Not Allowed <br> USER : Not Allowed    | To create new employee    |
| `POST`   | localhost:8080/api/roles/create    | {<br>&nbsp;&nbsp;"roleName" : "ASSISTANT_MANAGER"<br>} |Yes   | ADMIN : Permitted <br> MANAGER : Not Allowed <br> USER : Not Allowed| To create new role   |
| `POST`   | localhost:8080/api/users/create    | {<br>&nbsp;&nbsp;"username" : "Aarti",<br>&nbsp;&nbsp;"password" : "Aarti",<br>&nbsp;&nbsp;"roles" : [{<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"roleId" : 3,<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;"roleName" :"USER"<br>&nbsp;&nbsp;}]<br>}| Yes   | ADMIN : Permitted <br> MANAGER : Not Allowed <br> USER : Not Allowed    | To create new user   |

<br>
<br>

## PUT Request:

| HTTP Method | URL Path | PostMan Body | Authorization Required | User Role Allowance | Description | 
| :-------------: | ------------- | -------------| ------------- | ------------- | ------------- |
| `PUT` |localhost:8080/api/employees/update/6|{<br>&nbsp;&nbsp;"firstName": "Avaneet",<br>&nbsp;&nbsp;"lastName": "Kaur",<br>&nbsp;&nbsp;"email": "avaneet_kaur@gmail.com"<br>} | Yes | ADMIN : Permitted <br> MANAGER : Permitted <br> USER : Not Allowed     | To update an employee data by Id |






<br>
<br>

## DELETE Request:

| HTTP Method | URL Path | PostMan Body | Authorization Required | User Role Allowance | Description | 
| :-------------: | ------------- | :-------------: | ------------- | ------------- | ------------- |
| `DELETE` | localhost:8080/api/employees/delete/6 | - | Yes | ADMIN : Permitted <br> MANAGER : Permitted <br> USER : Not Allowed | To delete an employee by Id|











