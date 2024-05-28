
# Picto

Picto is a system developed for Galantucci-style language workshops aimed at school children. The study aimed to measure the children's ability to create and learn an abstract language.

#### 📜 Rules

Participants are divided into ordered pairs consisting of a `Speaker` and a `Listener`. The `Speaker` must communicate the selected image to the `Listener` using symbols provided. The `Listener` must then choose the image being communicated based on the symbols chosen by the `Speaker`.

#### 🎯 Aim of the game

The aim of the game is to have as many correct answers as possible.

#### 📑 Objectives

The experiment aimed to measure cognitive capacity for creating and learning an abstract new language during the period of most rapid brain development. An article detailing the system's workings and study results is forthcoming.
## Suggested interface

#### 📢 Speaker
![Speaker](https://github.com/mikolaj-martyna/picto-backend/assets/149105135/542d9690-8f88-4d64-af37-f65a6974e6e0)  

#### 👂 Listener
![Listener](https://github.com/mikolaj-martyna/picto-backend/assets/149105135/30d6dbe8-8f3f-4c1a-9262-094401d6d030)

#### ⏳ Waiting screen
![Waiting screen](https://github.com/mikolaj-martyna/picto-backend/assets/149105135/1533c172-9032-456d-8261-9e45ef93caa0)


## Features

- Customizable image and symbol selection
- Parametrized topology generation
- Admin panel with complete control over each game
- Multiple independent games can be played simultaneously
## API Reference

API reference is available at `/swagger-ui.html`

## Deployment

To deploy this project run

```bash
  docker compose up
```


## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`PICTO_DB_HOST`

`PICTO_DB_PORT`

`PICTO_DB_NAME`

`PICTO_DB_USER`

`PICTO_DB_PASSWORD`

`PICTO_JWT_SECRET`

`SPRING_PROFILES_ACTIVE`


## Running Tests

To run tests, run the following command

```bash
  mvn clean test
```


## Known Issues

#### 1. Server Sent Events

As of now, in certain cases, events sent by the SSE are blocked by adblockers (e.g. in Firefox), causing the entire application to stop working. To work around this, we recommend using Chromium-based web browsers when interacting with the application through its frontend. A complete rewrite of this application based solely on websockets is in the works to mitigate the problem.

#### 2. Data validation

Since Picto started as an internal project for a specific frontend, there aren't as many data validation mechanisms as needed to make it work on its own. We are aware of this and are actively working on improving the project.


## Related

**Frontend:** [github.com/skni-umcs/picto-front](https://github.com/skni-umcs/picto-front)


## Roadmap

- Migration from Sever Sent Events to Websockets

- Implement Data Transfer Object design pattern

- Improve hardening, in particular add data validation for all inputs

- Improve summary generation (don't include generations, which have not been completed by all participants, etc.)

