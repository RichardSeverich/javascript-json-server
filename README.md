# Javascript-json-server

This project fake REST API with zero coding in less than 30 seconds (seriously).
Created with <3 for front-end developers who need a quick back-end for prototyping and mocking.

See more information here: https://www.npmjs.com/package/json-server

## Prerequisites
1. Install Windows 10
2. Install node.js version v10.16.3
3. Install npm version v6.9.0

## Deploy

1. do git clone from: https://github.com/RichardSeverich/javascript-json-server
2. install dependencies: npm install
3. deploy: npm start or npm run start-auth
4. deploy will start with mock data in http://localhost:3000/.

5 run with alternative port: json-server --watch db.json --port 3004

## Use 1: npm start

1. GET  http://localhost:3000/users
2. GET  http://localhost:3000/users/9996666
3. POST http://localhost:3000/users
```
    {
      "id": "9996666",
      "nick_name": "Manu",
      "password": "manu123",
      "name": "Manuel",
      "last_name": "Lira",
      "career": "System engineer",
      "email": "Manuel546@gmail.com",
      "type": "Student"
    }
```
3. PUT http://localhost:3000/users/9996666
```
    {
      "nick_name": "Liza",
      "password": "liza123",
      "name": "Liza",
      "last_name": "Muzi",
      "career": "System engineer",
      "email": "Liza5984@gmail.com",
      "type": "Student"
    }
```
4. PATCH  http://localhost:3000/users
5. DELETE http://localhost:3000/users
3. OPTIONS http://localhost:3000/users

## Use 2: npm run start-auth

1. POST http://localhost:3000/auth/loginYou can login by sending a POST request to

2. POST http://localhost:3000/auth/login
3. with the following data

```
{
  "email": "nilson@email.com",
  "password":"nilson"
}
```

4. You should receive an access token with the following format
```
{
   "access_token": "<ACCESS_TOKEN>"
}
```

5. You should send this authorization with any request to the protected endpoints
```
Authorization: Bearer <ACCESS_TOKEN>
```