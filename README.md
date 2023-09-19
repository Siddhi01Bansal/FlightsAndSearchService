# Welcome to Flights Service

## Project Setup
-clone the project on your local
-Execute `npm install` on the same path as of your root directory of the downloaded project.
-Create a `.env` file in the root directory and add the following environment variables.
   -`PORT=3000`
-Inside the `src/config` folder create a new file `config.json` and then add the following piece of json
```
{
  "development": {
    "username": <YOUR_DB_USERNAME>,
    "password": <Your PWD>,
    "database": "Flights_Search_DB_DEV",
    "host": "127.0.0.1",
    "dialect": "mysql"
  }
}
```
-Once you have added your db config as listed above. go to the src folder from your terminal and execute `npm sequelize db:create`

## DB Design
- Airplane Table
- Flight
- Airport
- City

- Aflight belongs to an airplane but one airplane can be used in multiple flights.
- A city has many airports but one airport belongs to a city.
- One airport can have many flights but a flight belongs to one airport.