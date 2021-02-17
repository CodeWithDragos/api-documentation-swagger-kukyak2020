# API Documentation with Swagger by CodeWithDragos

### Getting Started :rocket:

Please install dependenies by running:

`npm install`

---
### Add [Swagger](https://swagger.io/) to your REST API

Set up the Swagger UI Express and write a Swagger file:

In the [App](/app.js) file:
1. Run `npm install swagger-ui-express --save` 
2. Run `npm install yamljs --save` to be able to read YAML files
3. Create a file called `swagger.yaml` in the root directory
4. Copy the basic structure into your file from this [link](https://swagger.io/docs/specification/basic-structure/)
5. Add the following to [app.js](./app.js):
   ```javascript
    const swaggerUi = require('swagger-ui-express');
    const YAML = require('yamljs');
    const swaggerDocument = YAML.load('./swagger.yaml');
   ```
6. In the same file add the following endpoint to your app:
   ```javascript
    app.use('/api-docs', swaggerUi.serve, swaggerUi.setup(swaggerDocument));
   ```
7. Run the app with `npm start`
8. Got to [localhost:3000/api-docs](http://localhost:3000/api-docs) and check the reuslt
9. Use the [Swagger Sintax](https://swagger.io/docs/specification/api-host-and-base-path/) to document the API fully
---


### Made with :orange_heart: in Berlin by @CodeWithDragos