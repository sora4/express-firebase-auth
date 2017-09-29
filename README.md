# Express Firebase Auth Middleware
[![npm version](https://badge.fury.io/js/express-firebase-auth@2x.png)](https://badge.fury.io/js/express-firebase-auth)

Authenticate your endpoints with Firebase auth.

## Features:

- Authenticate the user using Firebase before running the function.
- Ability to skip authentication on public API endpoints.

## Usage:

```
yarn install git@github.com:LeafyCode/express-firebase-auth.git
```

In your app:

```
import serviceAccount from '../firebase-config.json'; // Get this from the Firebase console.

```

## Installing / Getting started

```shell
yarn add express-firebase-auth
```

In your app:

```javascript
// Get this credentials file from the Firebase console.
import serviceAccount from '../firebase-config.json';
// Import the package
import { createFirebaseAuth } from 'express-firebase-auth';

// Initialize the firebase auth
const firebaseAuth = createFirebaseAuth({
  serviceAccount,
  ignoredUrls: [
    '/ignore'
  ]
});
app.use(firebaseAuth);
```

| Option           | Value                                                                                                        |
| -------------    |:------------------------------------------------------------------------------------------------------------:|
| `serviceAccount` | (**Required**) [Obtain this from firebase](https://firebase.google.com/docs/admin/setup#initialize_the_sdk)  |
| `ignoredUrls`    | (*Optional*) An array of URLs where you need to skip the authentication.                                     |

## Developing

### Prerequisites
- NodeJS: [https://nodejs.org/en/](https://nodejs.org/en/)
- Yarn: [https://yarnpkg.com/en/](https://yarnpkg.com/en/)
- ESLint in your editor.


### Setting up Dev

Clone the repo and run `yarn install`. Make sure you have an editor with an `eslint` plugin active. **Never** start working without `eslint`.


## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [link to tags on this repository](/tags).

## Style guide

Always follow the AirBnb Style Guide.
