# Typeorm
<img src="https://miro.medium.com/max/683/1*XzJfDO6t-nCRqrWqv64t-g.png" width="450px">

### Configurations (package.json) used typescript in scripts
```json
"typeorm": "ts-node-dev -r tsconfig-paths/register ./node_modules/typeorm/cli.js",
```

### Pre-requisites: Installing CLI and Path to run migrations (ormconfig.json)
Before creating a new migration you need to setup your connection options properly:
```json
"entities": ["./dist/modules/**/infra/typeorm/entities/*.js"],
  "migrations": ["./dist/shared/infra/typeorm/migrations/*.js"],
  "cli": {
    "migrationsDir": "./dist/shared/infra/typeorm/migrations"
  }
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
### Add field to table (migrations)
```
yarn typeorm migration:create -n addPhoneFieldToUsers
```
