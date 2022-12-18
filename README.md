# Think Out Loud API

## Description

This is an API for a social network web application where users can share their thoughts, react to friends’ thoughts, and create a friend list. 
 It uses Express.js for routing, a MongoDB database, the Mongoose ODM, and native JavaScript Date object to format timestamps. The seed data is created using Insomnia.

## Table of Contents
- [Think Out Loud API](#think-out-loud-api)
  - [Description](#description)
  - [Table of Contents](#table-of-contents)
  - [Installation](#installation)
  - [Usage](#usage)
  - [User Story](#user-story)
  - [Acceptance Criteria](#acceptance-criteria)
  - [Mock Up](#mock-up)
  - [Technologies](#technologies)
  - [License](#license)
  - [Questions](#questions)
  - [Author](#author)


## Installation 

  Before attempting to use this application, you must have the follow programs installed to your computer: 

  - VS Code
  - Node.js
  - MongoDB [Installation instructions available on MongoDB website](https://www.mongodb.com/docs/manual/installation/)
  
  In the terminal of VS Code please run the following command: 
  ```bash
npm install 
```

## Usage

 To use the application locally please clone the repo to your local environment.
 <br/>
 The application will be invoked by using the following command:

  ```bash
npm start
```

- When the server is started, the Mongoose models are synched to the MongoDB database.
- Open MongoDB and connect to the MongoDB URI `mongodb://localhost:27017`.
- On the list of databases, click on thinkoutloudDB to see users and thoughts data.

![Image showing MongoDB users](./Assets/MongoDB%20users.png)
![Image showing MongoDB thoughts](./Assets/MongoDB%20thoughts.png)
<br/>

A user can utilize this API to create a new user with a valid username and email, add other users as friends, post "thoughts" as well as "reactions" to thoughts, update and delete thoughts and reactions, and delete friends.

## User Story

```md
AS A social media startup
I WANT an API for my social network that uses a NoSQL database
SO THAT my website can handle large amounts of unstructured data
```

## Acceptance Criteria

```md
GIVEN a social network API
WHEN I enter the command to invoke the application
THEN my server is started and the Mongoose models are synced to the MongoDB database
WHEN I open API GET routes in Insomnia for users and thoughts
THEN the data for each of these routes is displayed in a formatted JSON
WHEN I test API POST, PUT, and DELETE routes in Insomnia
THEN I am able to successfully create, update, and delete users and thoughts in my database
WHEN I test API POST and DELETE routes in Insomnia
THEN I am able to successfully create and delete reactions to thoughts and add and remove friends to a user’s friend list
```

## Mock Up

(Links are also attached below in case there are any issues with video display)

The following animation shows how to start the application

![Demo of starting applicaiton](https://user-images.githubusercontent.com/106384519/208295167-af370d54-5286-4440-bf7e-821931cb912a.mp4)
https://user-images.githubusercontent.com/106384519/208295167-af370d54-5286-4440-bf7e-821931cb912a.mp4

The following animations show examples of the application's API routes being tested in Insomnia.

The following animation shows GET routes to return all users and all thoughts being tested in Insomnia:

![Demo of GET routes to return all users being tested in Insomnia.](https://user-images.githubusercontent.com/106384519/208295445-2814f3eb-cc55-466e-8fe7-899f995e890f.mp4)
https://user-images.githubusercontent.com/106384519/208295445-2814f3eb-cc55-466e-8fe7-899f995e890f.mp4

![Demo of GET routes to return all thoughts being tested in Insomnia.](https://user-images.githubusercontent.com/106384519/208295474-8a00e00f-0315-4268-8e42-64b445e616ee.mp4)
https://user-images.githubusercontent.com/106384519/208295474-8a00e00f-0315-4268-8e42-64b445e616ee.mp4


The following animation shows GET routes to return a single user and a single thought being tested in Insomnia:

![Demo that shows GET routes to return a single user being tested in Insomnia.](https://user-images.githubusercontent.com/106384519/208296103-d9f39781-3347-48b9-983d-f045388a819f.mp4)
https://user-images.githubusercontent.com/106384519/208296103-d9f39781-3347-48b9-983d-f045388a819f.mp4

![Demo that shows GET routes to return a single thought being tested in Insomnia.](https://user-images.githubusercontent.com/106384519/208296122-6a8a89c1-71b0-42ef-b2d8-e0b38ee4209e.mp4)
https://user-images.githubusercontent.com/106384519/208296122-6a8a89c1-71b0-42ef-b2d8-e0b38ee4209e.mp4


The following animation shows the POST, PUT, and DELETE routes for users being tested in Insomnia:

![Demo that shows the POST routes for users being tested in Insomnia.](https://user-images.githubusercontent.com/106384519/208295514-cc1d9525-0021-4566-81bc-a314f7c39f46.mp4)
https://user-images.githubusercontent.com/106384519/208295514-cc1d9525-0021-4566-81bc-a314f7c39f46.mp4

![Demo that shows the PUT routes for users being tested in Insomnia.](https://user-images.githubusercontent.com/106384519/208295559-cbfe3a79-9931-41f5-b937-7298fcdabbde.mp4)
https://user-images.githubusercontent.com/106384519/208295559-cbfe3a79-9931-41f5-b937-7298fcdabbde.mp4

![Demo that shows the DELETE routes for users being tested in Insomnia.](https://user-images.githubusercontent.com/106384519/208295602-e5e9a619-2d5d-4076-91a6-872d6af972db.mp4)
https://user-images.githubusercontent.com/106384519/208295602-e5e9a619-2d5d-4076-91a6-872d6af972db.mp4


The following animation shows the POST, PUT, and DELETE routes for thoughts being tested in Insomnia:

![Demo that shows the POST routes for thoughts being tested in Insomnia.](https://user-images.githubusercontent.com/106384519/208295618-697e7177-8e9c-419c-a002-91b0716e279c.mp4)
https://user-images.githubusercontent.com/106384519/208295618-697e7177-8e9c-419c-a002-91b0716e279c.mp4

![Demo that shows the PUT routes for thoughts being tested in Insomnia.](https://user-images.githubusercontent.com/106384519/208295653-52750808-4836-4fc1-949d-ebb8e397f231.mp4)
https://user-images.githubusercontent.com/106384519/208295653-52750808-4836-4fc1-949d-ebb8e397f231.mp4

![Demo that shows the DELETE routes for thoughts being tested in Insomnia.](https://user-images.githubusercontent.com/106384519/208295691-ef21914a-dc1c-46d4-8213-5e22dd50b25d.mp4)
https://user-images.githubusercontent.com/106384519/208295691-ef21914a-dc1c-46d4-8213-5e22dd50b25d.mp4

The following animation shows the POST and DELETE routes for a user’s friend list being tested in Insomnia:

![Demo that shows the POST routes for a user’s friend list being tested in Insomnia.](https://user-images.githubusercontent.com/106384519/208295803-a793a243-862b-4381-abe0-f104824ff1bd.mp4)
https://user-images.githubusercontent.com/106384519/208295803-a793a243-862b-4381-abe0-f104824ff1bd.mp4

![Demo that shows the DELETE routes for a user’s friend list being tested in Insomnia.](https://user-images.githubusercontent.com/106384519/208295823-1cac7474-8815-4cff-8dad-53bcb8ed98fe.mp4)
https://user-images.githubusercontent.com/106384519/208295823-1cac7474-8815-4cff-8dad-53bcb8ed98fe.mp4

The following animation shows the POST and DELETE routes for reactions to thoughts being tested in Insomnia: 

![Demo that shows the POST routes for reactions being tested in Insomnia.](https://user-images.githubusercontent.com/106384519/208295749-0ea7a6ef-df85-453c-819a-6a1d32995437.mp4)
https://user-images.githubusercontent.com/106384519/208295749-0ea7a6ef-df85-453c-819a-6a1d32995437.mp4

![Demo that shows the DELETE routes for reactions being tested in Insomnia.](https://user-images.githubusercontent.com/106384519/208295771-f72e519a-866c-4d4e-930a-b7c80780dee7.mp4)
https://user-images.githubusercontent.com/106384519/208295771-f72e519a-866c-4d4e-930a-b7c80780dee7.mp4

## Technologies
- JavaScript
- Node.js
- Express.js
- MongoDB
- Mongoose
- Insomnia

## License 
![License](https://img.shields.io/github/license/lalalaviv/think-out-loud-API)

## Questions

  Feel free to reach out if you have any enquiries
  <br/>
  GitHub: [@lalalaviv](https://github.com/lalalaviv)
  Email: lalala.viv@hotmail.com


## Author

  Vivian Lee