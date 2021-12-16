# JSON Server 

## Setup

Fork and clone this repo. 
https://github.com/Ewelajna14/json-server-template

Then install the dependencies by running:
npm install


## Seeding Data

To set up your database, update the `db/seeds.json` file to contain an object
with a key pointing to an array of data, like this:

```json
{
  "mapsData": [
    {
      "id": 1,
      "name": "C-1",
      "date": "2018-05-01",
      "groundElevation": "249",
      "description": "Poorly graded gravel with sand and clay",
      "properties": "Loose and soft ground",
      "classification": "GP",
      "blowCounts": "23",
      "coordinates": [
        -95.29017448425293,
        41.64931448003169
      ]
    },
    {
      "id": 2,
      "name": "C-2",
      "date": "2018-05-01",
      "groundElevation": "250",
      "description": "Fat clay with sand, brown to gray brown.",
      "properties": "Hard, moist angular to rounded gravel.",
      "classification": "CH",
      "blowCounts": "32",
      "coordinates": [
        -95.28124809265137,
        41.65335485542299
      ]
    }
```

Then, run `npm run seed` to copy data from the `db/seeds.json` file to the
`db/db.json` file. `json-server` uses the `db.json` file to create your RESTful
API, so make sure your `db.json` file is always up to date!

Any time you want to reset your database back to your original data, run
`npm run seed` again. Doing this will overwrite all the data in your `db.json`
file, so make sure you don't have any data in that file that you don't mind
losing!

## Running the Server Locally

To run your server run

json-server --port 4000 --watch db.json


## Deploying the Server

Free services like Heroku make it simple to deploy your Node server. Heroku also
works nicely with Rails, which you'll learn later in the program.

First, download the [Heroku CLI](https://devcenter.heroku.com/articles/getting-started-with-nodejs#set-up).

Then, [deploy your app](https://devcenter.heroku.com/articles/getting-started-with-nodejs#deploy-the-app).

Since Heroku deployment integrates with your git repo, you can easily deploy
changes to your database. To deploy changes, make sure to commit your code:

```sh
git add .
git commit -m "Updated database"
```

Then push your main/default branch up to Heroku:

```sh
git push heroku main
```
