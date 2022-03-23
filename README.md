Hello All :)

Wanted to learn some industry relevant skills so built a Twitter Clone (inspired by this tutorial https://www.youtube.com/watch?v=MT5j7xroSu4).

This is my first time coding in TypeScript and GraphQl (I'm used to using Vanilla JavaScript and RESTful APIs).

# Tech Stack #

## BACKEND ##
- TypeScript (programming language)
- GraphQL (APIs)
- Prisma (ORM)
- Node.js (server-side language)
- PostgreSQL (database)

## FRONTEND ##
- React (frontend library)
- TypeScript (programming language)
- Apollo Client (connects to backend)
- CSS (styling)

# Initial Set Up #
Open your coding IDE (e.g. Visual Studio Code), cd into the right directory, and in your terminal git clone this 'ready-to-run' Prisma example projects for authentication (https://github.com/prisma/prisma-examples) using the SSH key from the repo:

```
$ git clone git@github.com:prisma/prisma-examples.git
```

Drag the the folder 'graphql-auth' out into your twitterClone root directory. Then delete the 'prisma-examples' directory (just needed the graphql-auth folder for this project).

Rename the 'graphql-auth' folder to 'server', then cd into 'server'. Once inside, then run this command:

```
$ npm install
```