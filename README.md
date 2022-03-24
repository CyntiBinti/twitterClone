Hello All :)

Wanted to learn some industry relevant skills so built a Twitter Clone (inspired by this tutorial https://www.youtube.com/watch?v=MT5j7xroSu4).

This is my first time coding in TypeScript and GraphQl (I'm used to using Vanilla JavaScript and RESTful APIs).

# Tech Stack #

### BACKEND ###
- TypeScript (programming language)
- GraphQL (APIs)
- Prisma (ORM -- database connector)
- Node.js (server-side language)
- PostgreSQL (database)

### FRONTEND ###
- React (frontend library)
- TypeScript (programming language)
- Apollo Client (facilitates connection to backend for GraphQL usage)
- CSS (styling)

# How I Set Up My Local Dev Environment #

## GitHub Repo ##
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
(if an npm error occurs then run command 'npm install' to install dependencies, then run command 'npm start')

The React localhost URL should automatically open up in a new browser window. Now the frontend is set up!

## Connect Prisma Backend to PostgreSQL Database ##
### Creating the Database ###
Download and install PostgreSQL via this link >> https://www.postgresql.org/download/

Once the installation is complete, the database can be accessed by using pgAdmin (graphical interface tool for database management) that is also installed with PostgreSQL.

Once opened, pgAdmin will ask for the password used as part of the setup wizard when installing PostgreSQL.

Create a new server and also a new database in that server (as per pgAdmin documentation).

For that server, under 'Login/Group Roles', create a new user for yourself (remember to toggle privileges)

In VS code, create a new '.env' file in the 'prisma' folder (under the 'server' directory). This is where the environmental variables will be stored.

In the same 'prisma' folder, edit lines 5-8 (datasource db object) with the following taken from this source (https://www.prisma.io/docs/concepts/database-connectors/postgresql):

```
datasource db {
  provider = "postgresql"
  url      = env("DATABASE_URL")
}
```

Then in the '.env' file define the DATABASE_URL as:

```
DATABASE_URL = "postgresql://<your database user>:<database password for user, if set>@localhost:5432/twitterClone"
```
nb: again, refer to this doc for further guidance with this https://www.prisma.io/docs/concepts/database-connectors/postgresql

### Creating the Database Schema ###

## Connect Frontend to Backend ##


-- Enjoy! Happy Hacking!
