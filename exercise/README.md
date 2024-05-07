# ![Express API - Jukebox Lab - Exercise](./assets/hero.png)

## Requirements

Welcome to the Reactville Jukebox! In this lab, you'll be building the backend of a collaborative, community-driven jukebox application where anyone can contribute tunes by adding, updating, or deleting music tracks. This lab is designed to give you practice developing a backend API using Express. As you develop each feature, we highly recommend using Postman to test your API endpoints.

You'll implement full CRUD operations, allowing users to interact freely with the music database. Let’s dive in and make Reactville a bit more musical!

### Technical stack

- **Node.js and Express**: The backend will be built using Node.js with Express to handle server-side logic and HTTP requests.
- **MongoDB and Mongoose**: Use MongoDB as the database for storing track data, with Mongoose to provide schema validation.

### API requirements

- **One Model - Full CRUD**: The application will manage a single model, `Track`, which will support full CRUD operations.
- **Asynchronous Processing**: All routes must utilize `async/await` to handle asynchronous operations properly.
- **Error Handling**: Each route must include `try/catch` blocks to catch and handle errors effectively.
- **CORS Middleware**: Implement `CORS` middleware to enable cross-origin requests, ensuring the React frontend can interact seamlessly with the Express backend.

## Track Model Entity

| Field  | Type   | Required | Description                         |
| ------ | ------ | -------- | ----------------------------------- |
| title  | String | Yes      | The title of the track.             |
| artist | String | Yes      | The artist of the track.            |
| time   | String | No       | The runtime of the track, optional. |

## Required routes

| HTTP Method | Controller | Response | URI           | Use Case           |
| ----------- | ---------- | -------- | ------------- | ------------------ |
| POST        | `create`   | 200      | `/tracks`     | Create a track     |
| GET         | `index`    | 200      | `/tracks`     | List all tracks    |
| GET         | `show`     | 200      | `/tracks/:id` | Get a single track |
| PUT         | `update`   | 200      | `/tracks/:id` | Update a track     |
| DELETE      | `delete`   | 204      | `/tracks/:id` | Delete a track     |

### 1. Get All Tracks

- **Endpoint**: `GET /tracks`
- **Function**: Retrieves a list of all tracks.
- **Response**: Array of track objects.
- **Success Status Code**: 200 OK
- **Error Status Code**: 500 Internal Server Error


### 2. Get a Single Track

- **Endpoint**: `GET /tracks/:id`
- **Function**: Retrieves details of a specific track using its ID.
- **Response**: Track object.
- **Success Status Code**: 200 OK
- **Error Status Code**: 500 Internal Server Error

### 3. Add a New Track

- **Endpoint**: `POST /tracks`
- **Function**: Adds a new track to the database.
- **Success Status Code**: 201 Created
- **Error Status Code**: 500 Internal Server Error
- **Request Body**:
  ```json
  {
    "title": "Track Title",
    "artist": "Artist Name",
    "time": "3:45"
  }
  ```

### 4. Update a Track

- **Endpoint**: `PUT /tracks/:id`
- **Function**: Updates an existing track.
- **Success Status Code**: 200 OK
- **Error Status Code**: 500 Internal Server Error
- **Request Body**:
  ```json
  {
    "title": "New Track Title",
    "artist": "New Artist Name",
    "time": "3:25"
  }
  ```

### 5. Delete a Track

- **Endpoint**: `DELETE /tracks/:id`
- **Function**: Deletes a track from the database.
- **Response**: Success message.
- **Success Status Code**: 204 No Content
- **Error Status Code**: 500 Internal Server Error


Happy Coding! 
