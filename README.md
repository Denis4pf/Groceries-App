# Online Store :Grocery:
 

# Welcome to my UI/UX Project :blush:



This project is a frontend web application that allows users to interact with an API and view the data in a user-friendly way.

# Link to my recorded video Grocery App [Grocery-online-app](https://watch.screencastify.com/v/WykEk8aYuK7ZRrtEBBsc)

### Mvp :m: :v: 

- user can create an account
- User can add grocery products
- User can buy groceries
- User can delete the products
- User can login and log out of their respective accounts


 ```
## Features :sparkling_heart: :sparkles:
 ```
This project includes the following features: 

```
- A user interface for interacting with the API
- A data visualization component for viewing the data
- Authentication for securing user data
- Response caching for performance optimization
```
## Installation :download:

To install the project, you will need to clone the repository from GitHub and install the dependencies.

### Prerequisites

- Node.js
- NPM


# Installing :white_check_mark: :white_check_mark::white_check_mark:

1. Fork and Clone the repository from GitHub :computer: with the following command: 

`git clone https://github.com/username/project-name.git`

2. Install the dependencies with the following command: :zap:

`npm install`

3. Start the server with the following command: :zap:

`npm start`

4. Visit http://localhost:4000 in your browser to view the project.




## Feel free to add more grocery products and enjoy the expereience :grin: :+1:
## Contributing

To contribute to this project, please submit a pull request with your changes. 


# My Online Grocery API  :star2:

# Optional :point_left:
## Instructions for set up 
  * Clone this repository. :grin:

  To get set up, run: :running_woman:	:running:	

```console
$ bundle install   
$ rails db:migrate db:seed
$ rails s
```
This will download all the dependencies for our app and set up the database.
And additionally start the rails server in your console.

# Model Relationships

 - A `User` has many `Reviews`

- A `Review` belongs to a `User`

# Deployment to Render  :+1:

1. Create the application: Develop the application using the appropriate programming language and frameworks.

2. Set up the database: Set up the database that will be used to store the application's data.

3. Configure the server: Configure the server that will host the application on Render.

4. Configure the environment: Configure the environment that will be used to run the application on Render. This includes setting up the necessary libraries and packages.

5. Deploy the application: Deploy the application to Render using the appropriate methods. This could involve using a deployment tool such as Capistrano or a manual deployment process.

6. Test the application: Test the application to make sure it is running as expected.

7. Monitor the application: Monitor the application to make sure it is running smoothly. This includes keeping track of errors and performance.

### Sign Up Feature   :+1: :page_facing_up:

After creating the models, the next step is building out a sign up feature.

Handle sign up by implementing a `POST /signup` route. It should:

- Be handled in the `UsersController` with a `create` action
- In the `create` action, if the user is valid:
  - Save a new user to the database with their username, encrypted password,
    image URL, and bio
  - Save the user's ID in the session hash
  - Return a JSON response with the user's ID, username,password, an HTTP status code of 201 (Created)
- If the user is not valid:  :exclamation:
  - Return a JSON response with the error message, and an HTTP status code of
    422 (Unprocessable Entity)

> Note: Recall that we need to format our error messages in a way that makes it
> easy to display the information in our frontend. For this lab, because we are
> setting up multiple validations on our `User` and `Reviews` models, our error
> responses need to be formatted in a way that accommodates multiple errors.

### Auto-Login Feature  :+1:

Users can log into our app! 🎉 But we want them to **stay** logged in when they
refresh the page, or navigate back to our site from somewhere else.

Handle auto-login by implementing a `GET /me` route. It should:

- Be handled in the `UsersController` with a `show` action
- In the `show` action, if the user is logged in (if their `user_id` is in the
  session hash):
  - Return a JSON response with the user's ID, username, image URL, and bio; and
    an HTTP status code of 201 (Created)
- If the user is **not** logged in when they make the request:  :exclamation:
  - Return a JSON response with an error message, and a status of 401
    (Unauthorized)

Make sure the signup and auto-login features work as intended before moving
forward.



You should also be able to test this in the React application by signing up via
the sign up form to check the `POST /signup` route; and refreshing the page
after logging in, and seeing that you are still logged in to test the `GET /me`
route.

### Login Feature  :+1:

Now that users can create accounts via the API, let's give them a way to log
back into an existing account.

Handle login by implementing a `POST /login` route. It should:

- Be handled in the `SessionsController` with a `create` action
- In the `create` action, if the user's username and password are authenticated:
  - Save the user's ID in the session hash
  - Return a JSON response with the user's ID, username, image URL, and bio
- If the user's username and password are not authenticated:  :exclamation:
  - Return a JSON response with an error message, and a status of 401
    (Unauthorized)


### Logout Feature

Users can log into our app! 🎉 Now, let's give them a way to log out.

Handle logout by implementing a `DELETE /logout` route. It should:

- Be handled in the `SessionsController` with a `destroy` action
- In the `destroy` action, if the user is logged in (if their `user_id` is in
  the session hash):
  - Remove the user's ID from the session hash
  - Return an empty response with an HTTP status code of 204 (No Content)
- If the user is **not** logged in when they make the request:  :exclamation:
  - Return a JSON response with an error message, and a status of 401
    (Unauthorized)


You should also be able to test this in the React application by logging in to
check the `POST /login` route; and logging out with the logout button to test
the `DELETE /logout` route.

### View List Products

Users should only be able to view products on our site after logging in.

Handle viewing by implementing a `GET /users` route. It should:

- Be handled in the `ProductsController` with a `index` action
- In the `index` action, if the user is logged in (if their `user_id` is in the
  session hash):
  - Return a JSON response with an array of all products with their prices,
    detailed, and HTTP status code of 201 (Created)
- If the user is **not** logged in when they make the request:  :exclamation:
  - Return a JSON response with an error message, and a status of 404
    (not found)



# Thats it. 4PF Grocery Online Store API is done. 	:blue_heart: :innocent:	


## License

This project is licensed under the MIT License.
```
MIT License

Copyright (c) 2022 Denis Onwong'a Orina

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```
# contact me via
[Contact me via my email](dennisonwonga155@gmail.com)


# Soko