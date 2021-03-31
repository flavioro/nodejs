# Typeorm
<img src="https://miro.medium.com/max/683/1*XzJfDO6t-nCRqrWqv64t-g.png" width="450px">

### Configurations package.json used typescript in scripts
```json
"typeorm": "ts-node-dev -r tsconfig-paths/register ./node_modules/typeorm/cli.js",
```

### Run Production
./node_modules/.bin/typeorm migration:run

### Environment developer show commands (helper)
```
yarn typeorm 
```

### Show info table
```
yarn typeorm migration:show
```
### Create migrations
```
yarn typeorm migration:create -n CreateUser
```
