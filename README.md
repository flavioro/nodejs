# N O D E J S - ![](https://www.simform.com/wp-content/uploads/2019/11/Node.JS-Use-Cases-Cover-Image.png)

nodejs, commands 

*** C O N F I G ****
 - yarn add eslint -D
 - yarn eslint --init
 - yarn add prettier eslint-plugin-prettier eslint-config-prettier -D

node dist/shared/infra/http/server.js

Run service
pm2 start dist/shared/infra/http/server.js --name power-back

Alwasy restart
pm2 startup systemd

pm2 logs

pm2 monit

Create folder 'Util' with:
 - Work files (pdf, csv, json, xml, figure);
 - Rename multiple files (extension and name);
 - Public APIs:
  - github
  - https://github.com/public-apis/public-apis, 
  - https://apilist.fun/category/business
  - https://any-api.com/
  - https://github.com/BrasilAPI/BrasilAPI

https://www.npmjs.com/package/json-server
npx json-server --watch server.json --port 3333 -w -d 2000
