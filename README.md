# Cubius
This project is designed to help students and researchers make online psychology experiments. It is built with Webpack and Phaser game engine. Check out the documentation below.

We are looking for contributors to design new modules and effects, please send a PR.


## Table of Contents
1. [Requirements](#requirements)
2. [Installation](#installation)
3. [Running the Project](#running-the-project)
4. [Project Structure](#project-structure)
5. Live Development
6. Development
7. Donation

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
|`start`            |Serves your app at `localhost:1300`|
|`deploy`           |Builds the application to ./dist|

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
│   ├── states               # Main route definitions and async split points
│   │   ├── index.js         # Bootstrap states
│   │   ├── Blank.js         # Blank state
│   │   ├── Boot.js          # Boot state
│   │   ├── Preload.js       # Preload state
│   │   ├── End.js           # End state
│   │   ├── Text.js          # User-defined state
│   │   ├── Image.js         # User-defined state
│   │   ├── effects             # Fractal route
│   │   │   ├── index.js     # Bootstrap effects
│   │   │   ├── blink.js     # User-defined effect
│   │   │   ├── flip.js      # User-defined effect
│   │   │   └── rotate.js    # User-defined effect
└── tests                    # Unit tests
```
