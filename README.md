This is a base NodeJS project template, which anyone can use as it has been prepared by keeping some of the most important code principles and project management recommendations. Feel free to change anything.

`src` -> Inside the src folder, all the actual source code regarding the project will reside, this will not include any kind of tests. (You might want to make separate tests folder)

Let's take a look inside the `src` folder 

- `config` -> In this folder, anything and everything regarding any configurations or setup of a library or module will be done. For example: setting up `dotenv` so that we can use the environment variables anywhere in a cleaner fashion, this is done in the `server-config.js`. One more example can be to setup the logging library that can help to prepare meaningful logs, so configuration for this library would also be done here.

- `routes` -> In the routes folder, we register a route and the corresponding middleware and controllers.

- `middlewares` -> They are just going to intercept the incoming requests where we can write our validators, authenticators etc

- `controllers` -> They are kind of the last middleware, they call the business layer to execute the business logic. In controllers, we just receive the incoming requests and data and then pass it to the business layer, and once business layer returns an output, we structure the API response in controllers and send the output.

- `repositories` -> This folder contains all the logic using which we interact with the DB by writing queries, all the raw queries or ORM queries will go here.

- `services` -> Contains the business logic and interacts with the repositories for data from the database

- `utils` -> Contains helper methods, error classes 

### Setup the project

- Download this template from Github and open it in your favourite text editor

- Go inside the folder path and execute the following command:

    ```
    npm install
    ```

- In the root directory create a `.env` file and add the following environment variables
    ```
        PORT=<port number of your choice>
    ```
    ex:
    ```
        PORT=3000
    ```

- Go inside the src folder and run `npx sequelize init`.

- Inside the `config/config.json`, setup the configuration for dev, test and production environment databases.

To run the server execute 

```
    npm run dev
```


