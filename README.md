# Nodejs boilerplate

### What does it include.

- This is a brand new boilerplate to start with a nodejs project. This has been written with alot of critical thinking and based on my personal experience that issues might come or that will cause alot of problems in later stage.

- It includes
    - The typescript approach to make it static language and rectifying errors before runtime.
    - validation on environment variables is present too. In case you are missing or providing wrong environment variables. The app will not run silently, instead it will throw the error.
    - Large number of good practices are used to keep the code DRY for example, Singleton pattern, Enums, Interfaces, Inheritence.
    - Logger is added so that no data could get lost right from day one. Two types of loggers are used named `morgan` and `winston`. Morgan is to log all the failing api's automatically whereas Winston is for custom logging mechanism and will log it whereever you have introducted it.
    - Logger will print on terminal or dump it in the logs based on the environment. Former is when it is development mode where as the latter on is for the others.
    - Rotational mechanism is provided in the logs, so that logs will be distributed over different days and small chunks. However it is customizable in the configuration files.
    - A temporary example of models, routes and controllers is provided so as to extend it as required.
    - `Mongoose` is setup to interact with the database which is `MongoDB` in our case.
    - All the required actions are consolidated in `appStartUtil.ts` and they are chained in a neat way in the main file. Some of the required actions are including `morgon`, `helmet`, `body-parser`, `cookie-parser` and the automatic inclusion of all the mongoose models and api routes.
    - Added `socket.io` for socket server and connection. Separate file has been created for socket connection and it's respective connection event. Although a static instance variable is introduced in the class to ensure only single socket connection, but even without that it works just fine.
    - This also supports hot reloading of the components with the help of `nodemon`

### Some general instructions
- To start the app `npm start`. This will compile the ts and run the node server.
- Mongodb should be installed on the windows and the service must be in the running state. Only after that the backend will be able to connect.
- use `ES6` syntax generously as the ts will automatically compile it to es5 during transpilation process.
- `.env` file is not present in the repo. So you may need to set in order to successfully run the setup.

### Note
- Please note that this repo is just based on personal experience in terms of developer requirement and common issues that come up while setting up the node.js server. However it is not in it's best version and I have published it for my own good and others as well.
- If you think this is too complicated to understand due to too much modularity and typescript approach. You can go for my `boilerplate` repo as it was created long time ago with no brainstorming. Yet it is easy to understand (Maybe). However, the critics and suggestions are welcome for the betterment of the repo and improving the way of starting a nodejs server.