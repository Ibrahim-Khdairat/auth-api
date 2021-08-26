

## LAB - 08 : auth-api

### Deployment Test

**Author: Ibrahim Khdairat**


- [Back-End-Heroku-Link](https://ibrahim-auth-api.herokuapp.com/).
- [Repo Link](https://github.com/Ibrahim-Khdairat/auth-api).

**Setup**

`.env` **requirements**

- `PORT` - Port Number

- `DATABASE_URL` = Postgres DB

- `SECRET` = JWT SECRET

**Running the app**

- `npm start`

- Endpoint: `/signup`

> `{"username": "Anolla","password": "Haddad","role": "editor"}`

- Returns Object

 >  {
    "user": {
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6IklicmFoaW0iLCJpYXQiOjE2Mjk4NzQyNTh9.EyCC2WdB4zLlm8evU0j2Dtn5ToZQyqM7DfDCR9FK1NY",
        "capabilities": [
            "read",
            "create",
            "update",
            "delete"
        ],
        "id": 1,
        "username": "Ibrahim",
        "password": "$2b$10$Zm4SAHTMRY/ebxWJESuGyOewMlsvIcgsI3/w4eMQXyuoM3PGfeL92",
        "role": "admin",
        "updatedAt": "2021-08-25T06:50:56.247Z",
        "createdAt": "2021-08-25T06:50:56.247Z"
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6IklicmFoaW0iLCJpYXQiOjE2Mjk4NzQyNTh9.EyCC2WdB4zLlm8evU0j2Dtn5ToZQyqM7DfDCR9FK1NY"
}
- Endpoint: `/signin`

> - Username `Isra'a`
> - Password `Othman`

- Returns Object

      
  {
    "user": {
        "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6IklzcmEnYSIsImlhdCI6MTYyOTg3NDU1MX0.7tNhxTxba6Tdxajl_S8-9Gx6vcs3v0QANjlvHMOVvQc",
        "capabilities": [
            "read",
            "create",
            "update"
        ],
        "id": 2,
        "username": "Isra'a",
        "password": "$2b$10$y8J3LYG3rv6pokAhrWdUJO/sDUoVoUd/A6vHB3M0cQnDZHzcBqIkG",
        "role": "editor",
        "createdAt": "2021-08-25T06:54:53.566Z",
        "updatedAt": "2021-08-25T06:54:53.566Z"
    },
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6IklzcmEnYSIsImlhdCI6MTYyOTg3NDU1MX0.7tNhxTxba6Tdxajl_S8-9Gx6vcs3v0QANjlvHMOVvQc"
}

- Endpoint: `/users`

> - Token `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6IklicmFoaW0iLCJpYXQiOjE2Mjk4NzQyNTh9.EyCC2WdB4zLlm8evU0j2Dtn5ToZQyqM7DfDCR9FK1NY`

- Returns Object

  [
    "Ibrahim",
    "Isra'a"
]

> - Token `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6IklzcmEnYSIsImlhdCI6MTYyOTg3NDU1MX0.7tNhxTxba6Tdxajl_S8-9Gx6vcs3v0QANjlvHMOVvQc`

- Returns Object

{
"status": 500,
"message": "Access Denied"
}

**Tests**

- Unit Tests: `npm run test`
- Lint Tests: `npm run lint`

**UML**

![UML](uml.jpeg)