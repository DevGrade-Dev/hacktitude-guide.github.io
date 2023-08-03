# Welcome to `Hacktitude Malaysia 2023`

Welcome to the final run of Hacktitude Malaysia 2023! Before you begin, please ensure that your machine is set up correctly by following these instructions.

## Setting pre-requisites in your environment

This section helps you understand the prerequisites required to complete the hackathon.

Installations required:
   - [Git](https://git-scm.com/downloads)
   - [Node.js version 14.15.0](https://nodejs.org/ja/blog/release/v14.15.0)
   - [npm](https://www.npmjs.com/)

<br>

> _Recommended: To ensure seamless management of multiple Node.js versions on your machine, it is highly recommended to use a [Node Version Manager (NVM)](https://github.com/nvm-sh/nvm)._

## Remove code commit credentials

Remove code commit credentials if there are any previous credentials stored in your computer.

### In Windows

* Open **Control Panel > User Accounts > Credential Manager > Windows Credentials**
* Remove any stored credentials for CodeCommit.

<br>

<p align="center">
  <img src="./images/Windows Credentials.png" width="500px">
</p>

### In Mac

* Go to **KeyChain Access**
* Remove any stored credentials for CodeCommit.

<br>

<p align="center">
  <img src="./images/MAC Credentials.png" width="500px">
</p>

## Legitimacy of your solution

Any attempt to compromise the integrity of the contest will `unconditionally disqualify` your team. Therefore, please ensure you avoid attempting:

- Tampering with files in the `tests` folder or `config` folder.
- Hard coding values or logic to pass the test without solving the challenge legitimately.

## Improving your developer experience (Optional)

This step is not mandatory for working on the Hacktitude challenges, but it may improve your development experience. You can consider the following:

- Install a plugin for **SQLite** on your IDE so that you can explore the SQLite database.
- Install any other plugin that you find necessary to improve your developer experience.

##  Important <span style='color: red;'>!!</span> 

* _Using ChatGPT or any AI-related tools will be identified on the DevGrade platform and will result in immediate disqualification from the hackathon._

* _The  final competition is scheduled for a duration of **9 hours**._

* _Violation of the rules and regulations, or any attempt to gain an unfair advantage may result in disqualification._

* _Refrain from refreshing the page._

## Getting support

There will be minimal to no support available on the contest day. We are unable to clarify challenge descriptions on an individual basis. However, if you need help setting up the project, you may contact the **_technical support team_** via WhatsApp at the phone number `+94 74 354 6446`. Please note that no support for technical doubts will be provided. If we answer a question, we may share your question (anonymously) and our answer with all the team leaders via the common WhatsApp chat group where the team leaders will be added to in due course.

For **_non-technical support_**, you may reach out to our Malaysian Representative Anne Gomez at the number `+60 18 299 4076`, but please use calls only.

## References

- [Hacktitude official website](https://www.hacktitude.io)
- [Hacktitude FAQ](https://www.hacktitude.io/faq)
- [99x website](https://99x.io)
- [DevGrade website](https://devgrade.io/)


[15:20] Rashmika Silva

# Challenge 4 - View Friends and Their Details


In this challenge, you are required to implement functionalities to allow users to view their existing friends and their details in the HobbieSkout application.


## Core Functionalities


1. Return an Array of Friends (Challenge 4.a): Users can retrieve an array of their accepted friends. The response should include information about each friend, such as their `id`, `email`, `gender`, `firstname`, `lastname`, `image_url`, `hobbies`, and `skills`.


## Test Case


The provided test suite checks the functionality of retrieving an array of friends for the authenticated user. It ensures that the response contains the correct details of each friend.


### Challenge 4.a


The test retrieves the list of accepted friends for the authenticated user from the database. It then sends GET requests to the appropriate endpoints to fetch the details of each friend based on their `id`. The test validates that the responses contain the correct information for each friend, as shown below.


Implement the method `viewFriends(id)` inside the `friendRepository` to return the friends in the `friends` table. Check whether there are records where the respective user has sent a request whose status is `ACCEPTED` and the user received a request whose status is `ACCEPTED`. The parameter `id` in the method `viewFriends(id)` refers to the `id` attribute in the `users` table to fetch the friends for a corresponsing user. Then return the list of friends as below.


Hint: You can use the `getUser(id)` method in `userRepository` to fetch each user's details and return an array of users as friends.


API for the user `Liyana`, `http://127.0.0.1:3000/api/friends/6`


Expected output for user `Liyana`,


```json

[

      {

        "id": 3,

        "email": "laflame@cactusjack.com",

        "gender": "Female",

        "firstname": "Travis",

        "lastname": "Scott",

        "image_url":

          "https://upload.wikimedia.org/wikipedia/commons/thumb/1/14/Travis_Scott_-_Openair_Frauenfeld_2019_08.jpg/500px-Travis_Scott_-_Openair_Frauenfeld_2019_08.jpg",

        "hobbies": [

          {

            "name": "Music",

            "rate": 5,

          },

        ],

        "skills": [

          {

            "name": "Java",

            "rate": 2,

          },

        ],

        "reqId": 2

      },

      {

        "id": 5,

        "email": "random@user.com",

        "gender": "Female",

        "firstname": "Thomas",

        "lastname": "A. Anderson",

        "image_url":

          "https://th.bing.com/th/id/OIP.bEl-isZYhCmzsIGyhdEatgHaEK?pid=ImgDet&rs=1",

        "hobbies": [

          {

            "name": "Video Games",

            "rate": 1,

          },

          {

            "name": "Gym",

            "rate": 5,

          },

          {

            "name": "Rap",

            "rate": 5,

          },

        ],

        "skills": [

          {

            "name": "Dancing",

            "rate": 3,

          },

          {

            "name": "Docker",

            "rate": 5,

          },

        ],

        "reqId": 4

      },

    ]


```

In the above response, `id` refers to each user's `id` in the `users` table.

`reqId` is the `id` attribute of the `friends` table.

After successful implementation, you will be able to view the friends through the application, as shown below.

Note: The user avatar image can be different; ignore it as it was generated randomly.

