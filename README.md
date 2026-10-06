# Student Management REST API

This is Lab Assignment 2 for Web Dev III (Node.js & Express Backend).

The project uses Node.js and Express.js to create a simple REST API for managing student records.

## Features

- Add a student
- View all students
- View a student by ID
- Update a student
- Delete a student
- Custom logger middleware
- Modular routing
- Basic error handling
- JSON data stored in an array

No database is used.

## Project Structure

```text
student-management-rest-api/
│
├── app.js
├── package.json
│
├── data/
│   └── students.js
│
├── middleware/
│   └── logger.js
│
└── routes/
    └── studentRoutes.js
```

## How to Run

Open the project folder in VS Code and run:

```bash
npm install
npm start
```

The server will start at:

```text
http://localhost:3000
```

## API Endpoints

| Method | URL | Purpose |
|--------|-----|---------|
| GET | /students | Get all students |
| GET | /students/:id | Get one student |
| POST | /students | Add a student |
| PUT | /students/:id | Update a student |
| DELETE | /students/:id | Delete a student |

## POST /students

Body:

```json
{
    "name": "Neha",
    "course": "BTech"
}
```

## PUT /students/:id

Example:

```text
PUT http://localhost:3000/students/1
```

Body:

```json
{
    "name": "Rahul Sharma",
    "course": "BTech"
}
```

## Status Codes

- 200 - Successful request
- 201 - Student created
- 400 - Bad request
- 404 - Student or route not found

## Postman Testing

Test all five endpoints in Postman:

1. GET `/students`
2. GET `/students/1`
3. POST `/students`
4. PUT `/students/1`
5. DELETE `/students/1`

For POST and PUT, select **Body -> raw -> JSON** in Postman.

Note: Since the assignment does not use a database, the changes are only kept while the server is running. Restarting the server loads the original student array again.
