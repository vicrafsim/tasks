# `Kiddie Tasks Heroes!!`

`Kiddie Tasks Heroes` is a super cool web app designed to help all members of a certain family manage their tasks. It is specifically tailored for children, aiming to teach them about family responsibilities!

## Users: are you a `parent` or a `child`?

There are two types of app users: `parent` and `child`.
A person who is 18 years or older is considered a parent.
While parents have access to all application features, children have access only to a subset of them.

A parent can create a new family and create or delete a task.

Both parents and children can join an existing family, check a task when it's done, and edit their profile.

Upon signing up and logging in for the first time, users are prompted to choose whether they want to create a family (parent) or join an existing family (child or parent). Each user belongs to only one family.

Once you create a new family, a random code is assigned to the family. This code is necessary for other members of the family to access it. The family code is displayed in the user profile.

## TASKS `TASKS` TASK!

The Homepage of the App shows the tasks of the family of the specific current week day. You have two buttoms that allows you to move throught the week days and check the task of the next days or previous ones. 

## ...and other `features`

The Navbar allows you to access your profile page, where you can find information about yourself, your family, and your family members. This is where you can edit your profile pictures. Additionally, you can access a page that shows your personal scores and the scores of your family.

## ROUTES

| Path                        | Components               | Permissions            | Get/Post | Behavior                                                   |
|-----------------------------|--------------------------|-------------------------|----------|------------------------------------------------------------|
| /                           | HomePage                 | logged                  | get      |                                                            |
| /signup                     | SignupPage               | all permission         | post     |                                                            |
| /login                      | LoginPage                | logged                  | post     |                                                            |
| /verify                     | VerifyPage               | logged                  | get      |                                                            |
|                             |                          |                         |          |                                                            |
| **Task Routes**            |                          |                         |          |                                                            |
| /createtask                 | CreatePage               | logged/onlyParent       | post     | To create a new task for a family and assign for a specific person |
| /task                       | CreateTaskPage           | logged                  | post     | Display the task on the Home Page                           |
| /tasks/:_id/tasksByFamily   |                          | logged                  | get      | Assign task for the Family that created a task              |
| /tasks/:_id/:dayName        |                          | logged                  | get      | Show only the tasks of the day                              |
| /deletetask/:_id            | Task                     | logged/onlyParent       | delete   | Delete a task that is already done                          |
| /taskisdone/:_id            | Task                     | logged                  |          | Check if the task is done or not                            |
|                             |                          |                         |          |                                                            |
| **User Routes**            |                          |                         |          |                                                            |
| /uploaduserpicture          | UpLoadUserPicture        | logged                  | post     | All users can change their photo                            |
|                             |                          |                         |          |                                                            |
| **Family Routes**          |                          |                         |          |                                                            |
| /create                     | CreateFamily             | logged                  | post     | When you join our Application, you can create a "New Family" |
| /join                       | CreateFamily             | logged                  | post     | You can join a "Family"                                     |
| /familymembers/:_id         | CreateFamily             | logged                  | get      |                                                            |


## About us

We are Rafa from Brazil, Simone from Italy, and Victor from Spain. We met at a Full Stack Development program at Ironhack. Throughout this Boot Camp, we learned a so much about web development, and now we are excited to present our final project!

You can find us on LinkedIn and GitHub:

Rafa’s profiles:
https://github.com/Rgerotto
https://www.linkedin.com/in/rafael-gerotto-coelho-b4244120a/

Simo’s profiles:
https://github.com/simozan
https://www.linkedin.com/in/simone-zanni-4389478b

Victor’s profiles:
https://github.com/BittorChestnuts
https://www.linkedin.com/in/victorcastanos/


## Made in:
React
JavaScript
CSS
MongoDB
Node.js
Express

## Dependencies:
Axios
Cloudinary
