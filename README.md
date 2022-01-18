# keeper-app
A minimal Clone of Google Keep written in ReactJS with Material UI Components, themed to look exactly like Google Keep, with complex features like sharing, archiving, reminders etc. shoved away. The backend is a GraphQL server written in Golang, with data persisted in SQLite DB file, via GORM. The server implementation is complete with Cookie based Authentication, implemented using Authboss.

Frontend
ReactJS - See Web source

Complete frontend JS framework

Follows React Hooks pattern

MaterialUI - See Login.js

Follows the new Material Design guidelines (known as Material v2)

Completely themed to adapt Google's version for Keep - See theme.js

Uses Montserrat font to match Google's Product Sans (See this Subreddit post) and Roboto font - See fonts.js

MaterialUI Icons - See AppBar.js

Uses Outlined Icon design
Reach Router - See App.js

For client-side (browser) routing
URQL - See gql.js

Complete GraphQL client-side JS library

Provides React-hooks based implementations

Has Subscriptions (via Websockets) for dynamic updates from server (to create/delete notes with different tabs open)

Axios - React Hooks - See Login.js

React-hook based extension for Axios
Backend
Gorilla Mux - See main.go#main()

GORM - See models_gen.go

gqlgen - See resolver.go

AuthBoss - See main.go#setupAuthboss()

Deployment
Docker - Multistage build - See Dockerfile

Builds a deployable Docker image in 3 stages

Stage 1 - Builds runtime binary for Golang server

Stage 2 - Builds Production-ready ReactJS artifacts

Stage 3 - Assembles the artifacts from Stage 1 & Stage 2, and builds a container image

Heroku - Container Deployment - See heroku.yml

Builds and deploys the Docker image, with a git push
 
