# GM_config Typescript port

Typescript port of [GM_config](https://github.com/sizzlemctwizzle/GM_config)

---

the [GM_config](https://github.com/sizzlemctwizzle/GM_config) project, translate Javascript code to Typescript code, for
use GM_config with TS+Webpack

I want to use typescript + webpack to write GM script, and pack the GM_config into project to keep script can always run
offline,
but the `.d.ts` defined and `js` impl seems like not work well with webpack.

so I translate the code to pure typescript
in [there](https://gist.github.com/Lyoko-Jeremie/3e7d97a5c2eb14d1bc0bb53ae76a4446) ,
hope it can help someone like me.

## now to use

install `lodash` for `assignIn, pick` . (or you can replace those function with a simple impl if you don't like lodash).

```
yarn install lodash @types/lodash
```

```json5
// tsconfig.json
{
  "compilerOptions": {
    "types": [
      "./src/GM_config_TS/Greasemonkey.d.ts",
    ],
  }
}

```

```typescript
import {GM_config} from '../GM_config_TS/gm_config';
```

then , use it happy.
