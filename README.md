# moodle-cardano-connect

It is a small but useful tool that allows students to login into [Moodle](https://moodle.org) Learning Management System via a Cardano wallet (such as Nami, Eternl, Flint, etc).

Users do not need to access Moodle with credentials, because they are authenticated through the browser wallet plugin.

### About the authentication process

The user wallet address is encrypted and used as the user's unique ID in Moodle. This data can be shared safely because it prevents revealing the cardano user behind the moodle learner.

For example, an address like this addr1x8dgthgc5tgk9v70jzaesgsexs92yhqfq39gy5vnzyuvssw6shw33gk3v2euly9mnq3pjdq25fwqjpz2sfgexyfcepqsn3r7pu generates the moodle user ID like this 4dece4f7431e625b36ce27a4a09727a2 (collisions are extremely rare and isolated per moodle server instance).

### Thanks to

<https://github.com/txpipe/wallet-connect-starter-kit> for the fundamental work on the Cardano wallet connection.

# Config instruction

1. You have to install the plugin from https://moodle.org/plugins/auth_userkey in to your Moodle Deployment and enable it according to the documentations.
2. In the plugin settings, set the `Mapping field` to `ID number` and `Create user?` to `Yes`.
3. Copy to `sample.env` to `.env` and update the fields as mentioned in the file.

# Building info

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information
