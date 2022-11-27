# stack-overflow-clone-server

## [Deployed URL](https://stack-overflow-api.onrender.com)

## [Frontend Source_code](https://github.com/SaiPraneethPegada/stack-overflow-clone-client.git)

    Test Credentials: 
          email : guest@guest.com
          password : Guest@123


----

## API End-Points:

| Method | End point | Description |
| ---- | ---- | ---- |
| POST | /signup | signup requirements -> displayName, email(unregistered) and password(Min 8 characters length) |
| POST | /login | login credential requirements -> email and password |
| POST | /forgot_password | user submit their registered email ID -> Receives email -> on click on the link received in mail will redirect to reset password page  |
| POST | /reset_password | requirements password and confirm password. Handles -> password and confirm password should match, New password and old password should be different |
| GET | /questions/getAll | get all posted questions |
| GET | /questions/get/:id | get a respective question by the question ID provided in params |

> After succesful logged in :-

| Method | End point | Description |
| ---- | ---- | ---- |
| POST | /questions/postQuestion | Post a unique question with questionTitle, questionBody and questionTags |
| PUT | /questions/edit/:id | with respective question ID provided in params, user who posted the question will have authorization to update the question. |
| DELETE | /questions/delete/:id | with respective question ID provided in params, user who posted the question will have authorization to delete the question. |
| PATCH | /questions/vote/:id | positive and negative voting system |
| PATCH | /answers/postAnswer/:id | answering a particular question |
| PATCH | /answer/delete/:id | user who posted that answer will have authorization to delete an answer. It takes question ID from params and answer ID from req.body |
| GET | /profile/:id | fetches user details stored in mongodb |
| PATCH | /update/:id | user can update their username, about and tags |

> Postman API Endpoints: https://postman.com/red-comet-158705/workspace/stack-overflow-clone
