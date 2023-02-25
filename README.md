# Todo list

Todo list is a web application created by node.js, express and sequelize.

You can use the default account and password below to log in. Also, you can create a new one or log in by facebook.

```
email: root@example.com
password: 12345678
```

## Features

- Registration with name, email and password
- Log in via facebook
- Log out

After log in, user can

- view each todo list
- view detail / edit / delete

![Log in page](/public/photos/todo_list.png)

## Prerequisites

- [Git](https://git-scm.com/downloads)
- [Node.js v14.21.1](https://nodejs.org/en/)
- [Express](https://expressjs.com/)
- [MySQL](https://www.mysql.com/)

## Install Todo List

#### Clone the repository locally

```
$ git clone https://github.com/freeway26tw/todo-sequelize.git
```

#### Install project dependencies

```
$ cd todo-sequelize
$ npm install
```

#### Add .env file

In order to use facebook login authentication, you have to submit the setting data below to .env

Facebook id and secret: [Facebook Developers](https://developers.facebook.com/)

```
FACEBOOK_ID=SKIP
FACEBOOK_SECRET=SKIP
FACEBOOK_CALLBACK=http://localhost:3000/auth/facebook/callback

SESSION_SECRET=ThisIsMySecret
MONGODB_URI=mongodb://localhost/expense-tracker
PORT=3000
```

## Use Todo List

#### Import seed data

To create seed data, you can to submit the command below.

```
$ npx sequelize db:seed:all
```

#### Start the app

If you already install [nodemon](https://www.npmjs.com/package/nodemon)，execute this
```
$ npm run dev
```

Or execute this

```
$ node app.js
```

The server will start running on http://localhost:3000/