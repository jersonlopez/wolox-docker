# wolox-docker
This repository is to know the advantages and how to use docker

### Previous requirements:
- [NodeJS 10.x](https://nodejs.org/en/download/)
- [Docker](https://www.docker.com/get-started)
- [Docker-compose](https://docs.docker.com/compose/install/)

### Project Structure
```
wolox-docker
│
├── package.json
├── app.js
├── .gitignore
└── Dockerfile
```

### Starting server:

1. First of all what we need to install express, which will help us build the NodeJS server:
    ```sh
      $ npm i express
    ```
2. Configure the server, for this we are going to write the following code block in the [`app.js`](app.js) file:
    ```js
      const express = require('express');

      const app = express();
      const port = process.env.PORT || 3000;

      app.get('/', (_, res) => res.status(200).send('Hello World!'));

      app.listen(port, () => console.log(`Server running on port ${port}!`));
    ```
3. To start the server we just need to run the follow command:
    ```sh
      $ node app.js # if you have the scripts you can run: `npm start` instead
    ```
    And in the console we should see something like this:
    ```shell
      > Server running on port 3000!
    ```
4. Finally, let's check in the browser if our server is running, for this we just have to visit [http://localhost:3000](http://localhost:3000).

### Let's rock with Docker(In Progess):
To build a dockerized node application
