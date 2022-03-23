Hello All :)

Wanted to learn some industry relevant skills so built a Twitter Clone (inspired by this tutorial https://www.youtube.com/watch?v=MT5j7xroSu4).

This is my first time coding in TypeScript and GraphQl (I'm used to using Vanilla JavaScript and RESTful APIs).

# Tech Stack #

### BACKEND ###
- TypeScript (programming language)
- GraphQL (APIs)
- Prisma (ORM)
- Node.js (server-side language)
- PostgreSQL (database)

### FRONTEND ###
- React (frontend library)
- TypeScript (programming language)
- Apollo Client (connects to backend)
- CSS (styling)


# How I Set Up My Local Dev Environment #
I created a new repo on my GitHub called 'twitterClone'. Added a README.md and .gitignore file (Node). Once created, I git cloned it (using it's SSH key) into my generic coding directory on my laptop (via my terminal).

## Initial Set Up: Backend ##
Open your coding IDE (e.g. Visual Studio Code), cd into the 'twitterClone' directory, and in your terminal git clone this 'ready-to-run' Prisma example projects for boiler plate authentication code (https://github.com/prisma/prisma-examples) using the SSH key from the repo:

```
$ cd twitterClone
$ git clone git@github.com:prisma/prisma-examples.git
```

Within this 'prisma-examples' directory, inside the 'typescript' folder, drag the 'graphql-auth' folder out into your twitterClone root directory. Then delete the entire 'prisma-examples' directory (just needed the graphql-auth folder for this project).

Rename the 'graphql-auth' folder to 'server', then run these commands:

```
$ cd server
$ npm install
$ npm run dev
```

Click the localhost URL in the terminal to open up the server sandbox running Graphql. Now the backend is set up!

## Initial Set Up: Frontend ##
Open up a new terminal (should automatically open into the root directory 'twitterClone'), and run the following command to install the react-app and also typeScript (https://create-react-app.dev/docs/adding-typescript/):

```
$ npx create-react-app my-app --template typescript
```
nb: I tweaked the above command slightly >> changed the folder name 'my-app' to instead be 'frontend' before I pressed enter in the terminal (creates a folder called 'frontend' rather then 'my-app', and installs React in that instead)

Finally run the below commands to start React:

```
$ cd frontend
$ npm start
```

The React localhost URL should automatically open up in a new browser window. Now the frontend is set up! --Enjoy hacking!