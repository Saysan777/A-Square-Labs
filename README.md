<p align="center">
<a href="https://A-Square-Labs.herokuapp.com/">
<img src="media/logo.svg"  alt="logo" height="100px" width="200"/>
</a>

<h3 align="center">Learn, Collab & Grow Together.</h3>
</p>

<p align="center">
<img src="https://img.shields.io/github/workflow/status/Saysan777/A-Square-Labs/build" alt="github actions" />

<a href="https://github.com/Saysan777/A-Square-Labs/blob/master/LICENSE" target="_blank">
<img alt="License: MIT" src="https://img.shields.io/github/license/Saysan777/A-Square-Labs" />
</a>
</p>

<p align="center">
<a href="https://A-Square-Labs.herokuapp.com">View Demo</a>
·
<a href="https://github.com/Saysan777/A-Square-Labs/issues">Report Bug</a>
·
<a href="https://github.com/Saysan777/A-Square-Labs/issues">Request Feature</a>
</p>

<p align="center">
Apply for mentorship to the top mentors recommended by our powerful algorithm based on your profile. Enjoy one-to-one live mentorship in our interactive video streaming labs for free.
</p>

> ⚠️ This is pre-released (experimental) version of [A-Square Labs website](https://A-Square-Labs.herokuapp.com). That means we are still working to improve the site and breaking changes may occur anytime. So please avoid providing your real profile details as the app isn't fully secure and data may get erased any time. Meanwhile, you can help us by [raising an issue](https://github.com/Saysan777/A-Square-Labs/issues/new/choose) if you find any bugs in the project.

## Features

- Authentication and Authorization
- Personal Dashboard for Mentor and Mentee
- Recommendation System
- Apply and Respond Mentorship Request
- Create and join private room
- Video and text based chat
- Screen sharing

## Tech Stack

- **Frontend** : Typescript, React.js, Redux Toolkit
- **Styling** : Ant Design, Custom Css with BEM naming convention
- **Backend** : Typescript, Node.js, Express.js
- **Database** : TypeORM with PostgreSQL database
- **Testing** : Jest, React Testing Library
- **Realtime Communication** : simple-peer (WebRTC), Socket.io
- **Algorithms** : Jaccard Similarity, Supervised recommendation algorithm, QuickSort Hoare
- **Deployment** : Server, Client and Database hosted on Heroku

## Local Development

Before running app locally make sure that you've installed the following things in your machine:

- Node.js version _v14.18.1_ (if you are using nvm try `nvm use 14.18.1` ) and yarn version _v1.22.17_
- PostgreSQL >= _v12.8_
- Download and install [Beekeeperstudio](https://www.beekeeperstudio.io/) as database toolkit for easy database setup. (Optional)

#### Step 1: Clone the repo

```sh
https://github.com/Saysan777/Mentors-Lab.git
```

#### Step 2 : Install dependencies

cd into the directory

```sh
 cd A-Square-Labs
```

In the root folder do:

```sh
  # first install server deps
  yarn

  # also install client deps
  cd client && yarn
```

#### Step 3 : Configuration

1.  Create `.env` file in the root directory.

```sh
  touch .env
```

2. Open [.env.example](./.env.example) file, copy everything

3. Paste the content in `.env` file

4. Create database named `mentor-labs` with [Beekeeper Studio](https://www.beekeeperstudio.io/) or `postgres-cli` from your terminal. _(You don't have to create tables for database)_

```sql
  CREATE TABLE "mentor-labs";
```

5. Again open `.env` file and replace fields like `DB_USER`, `DB_PASS` with your own credentials.

6. Create account on [Twilio](https://twilio.com/) and open the [Twilio dashboard](https://console.twilio.com/?frameUrl=/console).

7. Copy `TWILIO_ACCOUNT_SID` and `TWILIO_AUTH_TOKEN` keys and paste it on `.env` file on their respective fields.

8. For client too, we have small issue (might be fixed on near future). Go to `client` folder and create `.env` file.

```sh
  cd client  && touch .env
```

9. Copy everything of [.env.example](./client/.env.example) located inside client directory and paste it inside `.env` file of client directory. (You ca leave `REACT_APP_SENTRY_DSN` field empty)

_The configuration is quite hard tbh, if you encounter any problems in setup you can directy create [issue](github.com/Saysan777/A-Square-Labs/issues). I will try to work on that._

#### Step 4: Usage

Now, you can run application by

```sh
yarn dev

# Server runs on http://localhost:5000 and client on http://localhost:3000

```

## Production Deployment

There is a Heroku post build script so that you do not have to compile your React frontend manually, it is done on the server. Simply push to Heroku and it will build and load the client index.html page

## Contributing

Contributions, issues and feature requests are welcome. After cloning & setting up project locally, you can just submit a PR to this repo and it will be deployed once it's accepted.
Read [CONTRIBUTING.md](https://github.com/Saysan777/A-Square-Labs/blob/master/CONTRIBUTING.md) for complete contributing guidelines.

## Contributors

- WIP

## License

Copyright © 2021 [Alok Aryal](https://host-next.vercel.app/).
This project is MIT licensed.
