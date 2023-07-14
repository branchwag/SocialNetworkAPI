# Social-Network-Api

## Description

This project is a simple API for a social networking app using MongoDB! Users can share their thoughts, react to friends’ thoughts, and create a friend list. Feel free to clone this repo and test the endpoints in Insomnia!

Walkthrough video testing endpoints: 
https://drive.google.com/file/d/1vmiJtqY9kQtIP1oaF6miozJv-BDaJZdB/view

Screenshot of sample endpoint testing: 

![alt text](assets/thoughtsendpscreen.png)

## Installation

Make sure to run 'npm i' to install all of the dependencies in the package.json file. This app uses Express, Moment (for timestamp), and Mongoose. 

## Usage

You can seed users by going to the POST user endpoint in Insomnia (http://localhost:3001/api/users) and populating it with sample data in the following JSON structure:

```
{
  "username": "lernantino4",
  "email": "lernantino4@gmail.com"
}
```
You can then do a get request to see your sample user data (http://localhost:3001/api/users). You can also get data by User ID as well (http://localhost:3001/api/users/:userIDhere).

PUT and DELETE for users is also supported.

POST thoughts by usiing a valid userID (http://localhost:3001/api/thoughts/:useridhere) in the below format:

```
{
  "thoughtText": "Here's another cool thought 4...",
	"username": "lernantino4"
}
```

GET all current thoughts via http://localhost:3001/api/thoughts. You can also get thoughts by their id. 

PUT and DELETE for thoughts is also supported. 

POST reactions by using a valid thoughtID (Example: http://localhost:3001/api/thoughts/64b18e4ffed373230ca97abc/reactions) and populate the body of the request with sample JSON like below. 

```
{
	"reactionBody": "Ohno3",
	"username": "lernantino3"
}
```

DELETE is also supported for reactions. 

A fun 404 page for nonexistent routes has also been added! Enjoy!

## Credits

Columbia University Coding Bootcamp

404 Photo by <a href="https://unsplash.com/fr/@cookiethepom?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Cookie the Pom</a> on <a href="https://unsplash.com/photos/gySMaocSdqs?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>

## License

MIT License

## How to Contribute

Follow the [Contributor Covenant](https://www.contributor-covenant.org/)!
