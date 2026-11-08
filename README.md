# backend-web

Node.js + Express + MongoDB Atlas (Mongoose) CRUD API.

## Structure
```
config/db.js                 MongoDB connection
models/Student.js            Mongoose model
controllers/studentController.js   CRUD logic
routes/studentRoutes.js      Express routes
server.js                    App entry point
postman/                     Importable Postman collection
```

## Setup
```bash
npm install
cp .env.example .env     # then put your real Atlas password in MONGO_URI
npm run dev
```
In Atlas: **Network Access** must include your IP address.

## Endpoints
| Method | URL | Action |
|---|---|---|
| POST | /api/students | Create |
| GET | /api/students | Read all |
| GET | /api/students/:id | Read one |
| PUT | /api/students/:id | Update |
| DELETE | /api/students/:id | Delete |

## Testing
Import `postman/backend-web.postman_collection.json` into the Postman desktop app and run the requests in order (Create saves `studentId` automatically).

