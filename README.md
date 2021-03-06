<!--- ![](https://www.simform.com/wp-content/uploads/2019/11/Node.JS-Use-Cases-Cover-Image.png) -->

<img src="https://www.simform.com/wp-content/uploads/2019/11/Node.JS-Use-Cases-Cover-Image.png" width="750px">

*** C O N F I G **** More detais in https://www.youtube.com/watch?v=1nVUfZg2dSA

### Configuration eslint, prettier (** conflict prrettier and eslint, not install prettier)
 ```
 yarn add eslint -D
 yarn add prettier eslint-plugin-prettier eslint-config-prettier -D
 yarn eslint --init
 ```

 + Config add in file .eslintrc.json (add this file, files and folder, eslint not correction)
 + Add in .eslintrc.json lib to test code (here jest)
 ```
     "env": {
        "es2021": true,
        "node": true,
        "jest": true
    },
 ```
 + create file .eslintignore
 ```
 node_modules
 ```
 + create file prettier.config.js
 ```js
 module.exports = {
  semi: false,
  SingleQuote: true,
  trailingComma: 'none',
  endOfLine: 'auto'
}
```

### Update NodeJs (Windows), https://community.chocolatey.org/packages/nodejs#versionhistory

### npm link (https://medium.com/dailyjs/how-to-use-npm-link-7375b6219557 or https://flaviocopes.com/npm-local-package/)

### Routes (api rest) with Express (Post, Put, Get, Delete)

See https://stackoverflow.blog/2020/03/02/best-practices-for-rest-api-design/ or
CRUD here https://github.com/flavioro/ignite-template-conceitos-do-nodejs-main

Middlewares
https://github.com/flavioro/ignite-template-conceitos-do-nodejs-main

## Types of REST API Parameters
### Query & Route Params
```
http://minhaapi.com/movies?name=transformes&duration=2&actor=octimusprime
```
```js
/**
* três tipos de parâmetros
* Query params = ?teste=1
* Route params = /users/1
* Request Body = { "name": "Thiago" }
*/
  
// Query params = ?name=thiago
// fazer a requisição no navegador: http://localhost:3333/users/?name=Thiago
server.get("/users", (req, res) => {
  const name = req.query.name;
	return res.json({ message:  `Hello ${name}` });
});

// Route Params = /users/1
// fazer a requisição no navegador: http://localhost:3333/users/1
server.get("/users/:id", (req, res) => {
// const id = req.params.id;
const { id } = req.params; // desestruturado com ES06
	return res.json({ message:  `Buscando o usuário de ID: ${id}`});
});
```
See here https://rapidapi.com/blog/api-glossary/parameters/

### Debug VSCode in file launch.json
```json
{
  // Use IntelliSense to learn about possible attributes.
  // Hover to view descriptions of existing attributes.
  // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "attach",
      "name": "Launch Program",
      "skipFiles": [ "<node_internals>/**" ],
      "outFiles": [ "${workspaceFolder}/**/*.js" ]
    }
  ]
}
```
### Before add this (--inspect) in package.json
```json
  "scripts": {
    "dev": "ts-node-dev --inspect --transpile-only --ignore-watch node_modules --respawn src/server.ts"
  },
```

### Example test with Jest
```js
function filterByTerm(inputArr, searchTerm) {
  return inputArr.filter(function(arrayElement) {
    return arrayElement.url.match(searchTerm);
  });
}

describe("Filter function", () => {
  test("it should filter by a search term (link)", () => {
    const input = [
      { id: 1, url: "https://www.url1.dev" },
      { id: 2, url: "https://www.url2.dev" },
      { id: 3, url: "https://www.link3.dev" }
    ];

    const output = [{ id: 3, url: "https://www.link3.dev" }];

    expect(filterByTerm(input, "link")).toEqual(output);
  });
});
```
Or https://github.com/flavioro/ignite-template-conceitos-do-nodejs-main

### NPM: Install Specific Version of a Package
```
npm install express@4.16.1
```

### Update npm
``` 
sudo npm install -g npm
``` 
 
* Run app after build 
 ```
node dist/shared/infra/http/server.js
 ```

Create folder 'Util' with:
 - Work files (pdf, csv, json, xml, figure);
 - Rename multiple files (extension and name);
 - Public APIs:
  - github
  - https://github.com/public-apis/public-apis, 
  - https://apilist.fun/category/business
  - https://any-api.com/
  - https://github.com/BrasilAPI/BrasilAPI


* https://www.npmjs.com/package/json-server
```
npx json-server --watch server.json --port 3333 -w -d 2000
```
  
 How to update all dependencies in package.json (https://classic.yarnpkg.com/en/docs/cli/upgrade-interactive/)
  ```
 yarn upgrade-interactive
  ```
 
**API - P H O T O S**

https://picsum.photos/

* Update NPM
 ```
 npm install -g npm
 ```
 
 * Update NodeJs
 ```
 npm cache clean -f
 npm install -g n
 n stable
 PATH="PATH"
 ```

* npm-cache
 ```
npm cache verify
 ```
