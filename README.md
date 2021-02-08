# N O D E J S - ![](https://www.simform.com/wp-content/uploads/2019/11/Node.JS-Use-Cases-Cover-Image.png)

nodejs, commands 

*** C O N F I G **** More detais in https://www.youtube.com/watch?v=1nVUfZg2dSA
 
### count the number of keys/properties of an object in JavaScript###
 ``` 
var obj = { name: "John", age: 30, city: "New York" };
Object.keys(obj).length //
 ``` 
 
 
 ** JSON.stringify() ** 
   ``` 
 var obj = { name: "John", age: 30, city: "New York" };
var myJSON = JSON.stringify(obj);
RESULT: {"name":"John","age":30,"city":"New York"}
 ``` 
 
 ** JSON.parse() **
 ``` 
 const json = '{"result":true, "count":42}';
const obj = JSON.parse(json);

console.log(obj.count);
// expected output: 42

console.log(obj.result);
// expected output: true
 ``` 
 
 * Configuration eslint
 ```
 yarn add eslint -D
 yarn add prettier eslint-plugin-prettier eslint-config-prettier -D
 yarn eslint --init
 ```

 + Config add in file .eslintrc.json 
 + create file .eslintignore
 + create file prettier.config.js

* Run app after build 
 ```
node dist/shared/infra/http/server.js
 ```
 
Run service
 ```
pm2 start dist/shared/infra/http/server.js --name power-back
 ```
 
* Alwasy restart
 ```
pm2 startup systemd
 ```

* Other commands pm2
 ```
pm2 logs
pm2 monit
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
