Certainly! Here's the rewritten version in the same format:

---

![MERN Starter](http://res.cloudinary.com/hashnode/image/upload/w_200/v1466495663/static_imgs/mern/v2/mernio-logo.png)

# MERN Starter

[MERN Starter](https://travis-ci.org/Hashnode/mern-starter.svg?branch=v2.0.0)

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com)

[![Discuss on Hashnode](https://hashnode.github.io/badges/mern.svg)](https://hashnode.com/n/mern)

MERN Starter is a scaffolding tool designed to expedite the development of isomorphic applications using MongoDB, Express, React, and NodeJS. It streamlines the setup process and leverages proven technologies to accelerate development.

## Quickstart

```
npm install -g mern-cli
mern init your_new_app
cd your_new_app
npm install
npm start
```

**Note**: Ensure MongoDB is running. For MongoDB installation guide, see [this](https://docs.mongodb.org/v3.0/installation/). Also, `npm3` is required to install dependencies properly.

## Available Commands

1. `npm run start`: Starts the development server with hot reloading enabled.
2. `npm run bs`: Bundles the code and starts the production server.
3. `npm run test`: Starts the test runner.
4. `npm run watch:test`: Starts the test runner with watch mode.
5. `npm run cover`: Generates a test coverage report.
6. `npm run lint`: Runs linter to check for lint errors.

## File Structure

### Webpack Configs

MERN utilizes Webpack for module bundling. Four types of Webpack configs are provided: development, production, server (for bundling server in production), and babel (for server rendering of assets included through webpack).

### Server

MERN utilizes the Express web framework. The app resides in `server.js`, where we check for `NODE_ENV`.

#### Server Side Rendering

We use React Router's match function to handle all page requests, ensuring browser history works. All routes are defined in `client/routes.js`. React Router renders components according to the requested route.

```js
// Server Side Rendering based on routes matched by React-router.
app.use((req, res) => {
    match({
        routes,
        location: req.url
    }, (err, redirectLocation, renderProps) => {
        // Handling errors and rendering components
    });
});
```

### Client

The client directory contains shared components, routes, and modules.

#### Components

This folder contains common components used throughout the project.

#### Modules

Modules organize different domain-specific modules in the project. Each module typically includes components, pages, reducers, and actions.

## Miscellaneous

- Assets can be imported into JavaScript or CSS files and served by Webpack.
- ES6 and experimental ES7 features are supported through Babel transpilation.
- Docker configurations are available for both development and production environments.

## Customization

MERN Starter facilitates easy customization and extension. Users can modify blueprints and generators to tailor the project to their specific requirements.

## License

MERN Starter is released under the [MIT License](http://www.opensource.org/licenses/MIT).

---

This version retains the structure and format of the original README while providing rewritten content.
