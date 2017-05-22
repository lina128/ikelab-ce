# Cubius
This project is designed to help students and researchers make online psychology experiments. The engine takes experiment script, and then compile and run script in browser. Read more about how to install below, or check out the API documentation in [Wiki](https://github.com/lina128/cubius/wiki).

We are looking for contributors to design new modules and effects, please send a PR.

![version](https://img.shields.io/badge/version-1.0.3-brightgreen.svg)

## Table of Contents
1. [Requirements](#requirements)
2. [Installation](#installation)
3. [Running the Project](#running-the-project)
4. [Project Structure](#project-structure)
5. [Live Development](#live-development)
6. [Development](#development)

## Requirements
* node `^5.0.0`
* yarn `^0.23.0` or npm `^3.0.0`

## Installation
After confirming that your environment meets the above [requirements](#requirements), checkout this project and give it a new name:

```bash
$ git clone https://github.com/lina128/cubius.git <my-project-name>
$ cd <my-project-name>
```

When that's done, install the project dependencies. It is recommended that you use [Yarn](https://yarnpkg.com/) for deterministic dependency management, but `npm install` will suffice.

```bash
$ yarn  # Install project dependencies (or `npm install`)
```

## Running the Project
After completing the [installation](#installation) step, you're ready to start the project!

```bash
$ yarn start  # Start the development server (or `npm start`)
```

|`yarn <script>`    |Description|
|-------------------|-----------|
|`start`            |Serves your app at `localhost:3000`|
|`deploy`           |Builds the application to ./dist|

A successful start should look like this screenshot:



![start](http://res.cloudinary.com/ikelabrepo/image/upload/c_scale,w_622/v1495391136/startscreenshot_cly265.png)



A successful deploy should look like this screenshot:



![deploy](http://res.cloudinary.com/ikelabrepo/image/upload/c_scale,w_622/v1495391137/deployscreenshot_ed6xls.png)


## Project Structure
The project structure follows the **fractal** pattern demonstrated in this project (https://github.com/davezuko/react-redux-starter-kit) by Davezuko.

```
.
├── bin                      # All build-related code
├── config                   # All configurations
├── dist                     # Compired files
├── public                   # Static public assets
├── server                   # Express application that provides webpack middleware
│   └── main.js              # Server application entry point
├── src                      # Application source code
│   ├── index.html           # Main HTML page container for app
│   ├── main.js              # Application rendering
│   ├── config.js            # Game configurations
│   ├── Game                 # Main Game object for app
│   ├── states               # States/Modules
│   │   ├── index.js         # Bootstrap states
│   │   ├── Blank.js         # Blank state
│   │   ├── Boot.js          # Boot state
│   │   ├── Preload.js       # Preload state
│   │   ├── End.js           # End state
│   │   ├── Text.js          # User-defined state
│   │   ├── Image.js         # User-defined state
│   │   ├── effects          # Effects
│   │   │   ├── index.js     # Bootstrap effects
│   │   │   ├── flicker.js   # User-defined effect
│   │   │   ├── flip.js      # User-defined effect
│   │   │   └── rotate.js    # User-defined effect
└── tests                    # Unit tests
```

## Live Development

### Hot Reloading

Hot reloading is enabled by default when the application is running in development mode (`yarn start`). With hot reloading, your code updates can be reflected in the app while it's running without restart the server. This is very useful for development. Read more about [Hot Module Replacement](https://webpack.github.io/docs/hot-module-replacement.html).


## Deployment

Out of the box, this project is deployable by serving the `./dist` folder generated by `yarn deploy`. The simplest deployment strategy is a [static deployment](#static-deployments).

### Static Deployments

Serve the application with a web server by pointing it at your `./dist` folder. Make sure to direct incoming route requests to the root `./dist/index.html` file. Follow this article on how to host a static website on Amazon S3 (http://docs.aws.amazon.com/AmazonS3/latest/user-guide/static-website-hosting.html).
