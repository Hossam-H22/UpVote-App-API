# Up Vote API

The Up Vote API is a Node.js application built with Express and MongoDB, providing the backend services for a simple voting and commenting system. This API allows users to register, create posts, comment on posts, and vote on posts and comments. Additionally, it integrates with Cloudinary for handling image uploads.


<br>



## Table of Contents

- [ Introduction. ](#Introduction)
- [ Features. ](#Features)
- [ Technologies Used & Dependencies. ](#Technologies_Used)
- [ Project Structure. ](#Project_Structure)
- [ Getting Started. ](#Getting_Started)
- [ API Endpoints. ](#API_Endpoints)
- [ Available Base Url. ](#Available_Base_Url)
- [ Authentication and Security. ](#Authentication)
- [ Validation. ](#Validation)
- [ Media Upload. ](#Media_Upload)
- [ Feedback and Contributing. ](#Feedback_Contributing)
- [ License. ](#License)



<br>



<a id="Introduction"></a>

## Introduction
The Saraha API project provides the backend services for a simple voting and commenting system.


<br>



<a id="Features"></a>

## Features

- User registration and authentication.
- Add posts, and comments, and reply to comments.
- Input validation using Joi.
- Password hashing with Bcryptjs.
- Seamless media uploads using Cloudinary.



<br>



<a id="Technologies_Used"></a>

## Technologies Used & Dependencies
- **Node.js:** A server-side JavaScript runtime used to build fast and scalable network applications.
- **Express:** A minimal and flexible Node.js web application framework that simplifies API development.
- **MongoDB:** A NoSQL database used for efficient and flexible data storage.
- **Joi:** A validation library for JavaScript that helps ensure the integrity of data.
- **Bcrypt.js:** A library for hashing and salting passwords to enhance security.
- **Cloudinary:** A cloud-based media management platform for uploading, storing, and delivering images and other media.

For a complete list of dependencies, please refer to the `package.json` file.



<br>



<a id="Getting_Started"></a>

## Getting Started

To get started with the Fresh Cart frontend project, follow these steps:

1. <strong>Clone the Repository:</strong> Clone this repository to your local machine using the following command:
```bash
  git clone https://github.com/Dragon-H22/UpVote-App-API.git
```

2. <strong>Install Dependencies:</strong> Navigate to the project directory and install the required dependencies using your preferred package manager:
```bash
  cd UpVote-App-API
  npm install
```

3. <strong>Configure environment variables:</strong> Add variables for database connection, Cloudinary API keys, JWT secret, and token signature.

4. <strong>Run the Application:</strong> Start the development server to run the application locally:
```bash
  npm run dev
```

5. <strong>Access the Application:</strong> Open your web browser and visit `http://localhost:5000` to use it as a base link.



<br>



<a id="Project_Structure"></a>

## Project Structure
The project structure follows a modular pattern to enhance maintainability and readability:

* `DB/`
    * `Models/`: Defines MongoDB schemas.
    * `connection.js`: Connect to MongoDB.
* `src/`
    * `middleware/`: Middleware functions for authentication, error handling, etc.
    * `modules/`: Defines API routes and connects them to controllers to perform their business logic.
    * `utils/`: Utility functions for various tasks.
    * `app.js`: Main Express application setup.



<br>



<a id="API_Endpoints"></a>

## API Endpoints
* **Authentication**
  * `POST /auth/login`: Login user.
  * `POST /auth/signup`: Register new user.
* **User**
  * `GET /user/profile`: Retrieve details of a profile user.
  * `GET /user/:id/`: Retrieve details of a specific profile user to share it.
  * `PATCH /user/update`: Update general user date.
  * `PATCH /user/password`: Update the password of the user.
  * `PATCH /user/profilePic`: Upload the profile image of the user.
  * `PATCH /user/profileCovPic`: Upload cover images for the user profile with a maximum of 5 images.
* **Posts**
  * `GET /post`: Retrieve all posts.
  * `POST /post`: Create a post.
  * `PATCH /post/:postId`: Update specific post by id.
  * `PATCH /post/:postId/like`: Add like to specific post by id.
  * `PATCH /post/:postId/unlike`: Remove like from specific post id.
  * `DELETE /post/:postId`: Delete specific post by id.
* **Comments**
  * `GET /post/comment`: Retrieve all comments.
  * `POST /post/:postId/comment`: Create a comment on a specific post by his id.
  * `POST /post/:postId/comment/:commentId/reply`: Create a reply on a specific comment by his id.
  * `POST /post/:postId/comment/:commentId`: update specific comment data by his id.
  * `PATCH /post/comment/:commentId/like`: Add like to specific comment by id.
  * `PATCH /post/comment/:commentId/unlike`: Remove like from specific comment by id.
  * `DELETE /post/comment/:commentId`: Delete the specific comment by id.


> Detailed Postman API documentation can be found <a href="https://documenter.getpostman.com/view/23533987/2s9YC5xBwU" target="_blank">here</a>.



<br>



<a id="Available_Base_Url"></a>

## Available Base Url
- https://up-vote-app-api.vercel.app/
- https://up-vote-app-api-dragon-h22.vercel.app/
- https://up-vote-app-api-git-master-dragon-h22.vercel.app/





<br>



<a id="Authentication"></a>

## Authentication and Security
User passwords are securely hashed using Bcryptjs before being stored in the database. This ensures the confidentiality of user credentials.



<br>



<a id="Validation"></a>

## Validation
Joi is used to validate incoming data for user registration, login, posts, and comment sending. This ensures that only valid data is processed by the API.



<br>



<a id="Media_Upload"></a>

## Media Upload
The integration with Cloudinary allows users to upload media files, such as images, for their profile, and media in posts and comments.


<br>



<a id="Feedback_Contributing"></a>

## Feedback and Contributing
I'm excited to hear your <u><a href="https://forms.gle/zbBoPc8yRrUu8VJ9A" target="_blank">feedback</a></u> and discuss potential collaborations and if you'd like to contribute, please fork the repository, make your changes, and submit a pull request.



<br>



<a id="License"></a>

## License
This project is licensed under the [MIT license](LICENSE).


<br>

