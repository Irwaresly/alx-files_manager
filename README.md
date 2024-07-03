# File Manager Application

This project is a file manager application built with Node.js, MongoDB, Redis, and ExpressJS. It allows users to authenticate, manage files, and perform operations such as uploading files, changing permissions, viewing files, and generating thumbnails for images.

## Project Overview

- **Project Duration:** June 27, 2024, to July 4, 2024
- **Team Members:** You and Silvia Irware

## Features

- **User Authentication:** Token-based authentication for secure access.
- **File Management:**
  - List all files in the system.
  - Upload new files with metadata.
  - Change permissions (read, write, execute) for files.
  - View files and their details.
- **Image Processing:**
  - Automatically generate thumbnails for uploaded images.

## Technologies Used

- **Backend:** Node.js, ExpressJS
- **Database:** MongoDB for storing file metadata
- **Caching:** Redis for temporary data storage and caching
- **Background Processing:** Kue for handling background jobs

## Installation and Setup

1. **Clone the repository:**

   ```bash
   git clone <repository-url>
   cd <project-folder>
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Set up environment variables:**

   Create a `.env` file in the root directory with the following variables:

   ```dotenv
   PORT=5000
   MONGODB_URI=<your-mongodb-uri>
   REDIS_URL=<your-redis-url>
   ```

4. **Start the server:**

   ```bash
   npm start
   ```

## API Documentation

- **Authentication:**
  - `POST /api/auth/register`: Register a new user.
  - `POST /api/auth/login`: Login and receive a JWT token.

- **File Management:**
  - `GET /api/files`: Retrieve all files.
  - `POST /api/files/upload`: Upload a new file.
  - `PUT /api/files/:id/permissions`: Update file permissions.
  - `GET /api/files/:id`: View details of a file.

## Folder Structure

```
├── README.md
├── package.json
├── server.js
├── routes/
│   └── index.js
├── controllers/
│   ├── authController.js
│   └── fileController.js
├── models/
│   └── File.js
├── utils/
│   ├── db.js
│   └── thumbnailGenerator.js
└── .env.example
```

## Testing

- This project uses Mocha for unit testing and Chai for assertions. Run tests using `npm test`.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
