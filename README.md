create-ionic-nest-app
---
This is simple create app template for Ionic and NestJS.

# For start
```bash
% git clone git@github.com:rdlabo-team/create-ionic-nest-app.git winecode
% npm i @ionic/cli@latest @nestjs/cli@latest -g
% npm install
```

## Install App and Api template(First only)

- Launch Ionic CLI
```
% npm run create:app
```

- Launch NestJS CLI
```
% npm run create:api
```

### If you want to host NestJS in Lambda
You can use this command instead of `npm run create:api` .
Do `git clone` from https://github.com/rdlabo-team/serverless-nestjs
```
% npm run create:api:sls
```

## Connect learn
If you want to use learn, please execute:

```
% npm run install
```

# Launch App for development

```
% npm run app
```

```
% npm run api
```

# Connect app to api
Add api server domain to `app/environment/environment.ts` & `environment.prod.ts` .

```environment.ts
export const environment = {
  production: false,
  api: 'http://localhost:3000/',
};
```

And

```ts
import { environment } from '../environments/environment';
...
this.http.get(environment.api + 'controllerName');
```
