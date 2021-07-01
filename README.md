# 🐱 Petgatô 7

<!-- <h1 align="center">
  <img height="200px" src="./readme-images/Screenshot_2.png" />
</h1> -->

----------

# 📄 About

The **Petgatô** project is an blog, that readers can see posts, login, comment, like and search for posts related to pets, also the author can create, edit posts and manage several parts of the blog. It was develop during CJR's trainee process.

----------

# 🧰 Technologies used
- Frontend - **ReactJS**
  - react-quill
  - styled-components
  - axios
  - react-router-dom
  - html-react-parser
  - react-bootstrap
- Backend - **Ruby on Rails**
  - postgresql
  - jbuilder
  - jwt
  - bcrypt
  - CORS
  - mailer

----------

# 📚 Features implemented
This section lists a bunch of features made through the process.
  - [x] Login / Sign up
    - [x] Validations
  - [x] Forgot password (using mailer)
  - [x] Loading component
  - [x] Home page
    - [x] Posts
      - [x] Tags
      - [x] Like on home page
    - [x] Popular posts
    - [x] Search
    - [x] About author
  - [x] Post page
    - [x] Explore tags section
    - [x] Popular posts
    - [x] Format dates from backend
    - [x] Comment section
      - [x] Comment/reply
        - [x] Report
        - [x] Edit
        - [x] Delete
  - [x] About us page
  - [x] Contact us page
    - [x] Sending email
  - [x] Edit profile page
    - [x] Edit profile image
    - [x] Edit name
    - [x] Edit password
  - [x] Backoffice page / Admin page
    - [x] Tables of posts/tags/users/reports
      - [x] Edit page
      - [x] Delete

----------

# 🏭 How to install/use

This section describes how to run this app locally at your environment, of course you can access the deployed version [here](https://letmeask-19e44.web.app/). For this you need to have `ruby 2.7.3`, `postgresql`, `node`, `git` installed.

- **Backend**

First of all, we need to setup some files, starting with `config/database.yml`, you'll need to define your user and password there, it's simple, there are two pairs of it, don't forget.

This part is optional, just if you want to see the mailer working, go to `config/enviroments/development.rb`, on the last lines you will need to set some configurations for `action_mailer` work, like email, password, domain...

If you don't have these gems, install it:
```powershell
$ gem install bundler
$ gem install rails
```

Open a shell and get the repository on your local files with:
```powershell
$ git clone https://github.com/m4ycon/petgato-7.git
$ cd petgato-7/backend
# install the gems
$ bundle install
$ rails db:drop db:create db:migrate db:seed
# start the server
$ rails s
```

- **Frontend**

You can replace `npm` by `yarn`, if you have it. Now open another shell and:

```powershell
$ cd petgato-7/frontend
$ npm install
$ npm start
```

And finally you can access the app on `http://localhost:3000`

Happy hacking!

----------

Made by Maycon Fabio, Herisson Neves and Vitor Lemos 🚀
