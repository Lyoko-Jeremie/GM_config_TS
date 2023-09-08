# GM_config Typescript port

Typescript port of [GM_config](https://github.com/sizzlemctwizzle/GM_config)

---

the [GM_config](https://github.com/sizzlemctwizzle/GM_config) project, translate Javascript code to Typescript code, for
use GM_config with TS+Webpack

I want to use typescript + webpack to write GM script, and pack the GM_config into project to keep script can always run
offline,
but the `.d.ts` defined and `js` implement seems like not work well with webpack.

so I translate the code to pure typescript, hope it can help someone like me.


Because the origin code become from 2009, and need support old browser, so, it too old and lose some new feature.  
so, i add some feature to enhance it, about what's new feature and how to use, please see the `where are using` section follow.

---

## how to use

install `lodash` for `assignIn, pick` . (or you can replace those function with a simple impl if you don't like lodash).

```shell
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
// in your code 
import {GM_config} from '../GM_config_TS/gm_config';
```

then , use it happy.


---

## where are using

1. [Degrees-of-Lewdity_Cheats-Mod](https://github.com/Lyoko-Jeremie/Degrees-of-Lewdity_Cheats-Mod) , see [file](https://github.com/Lyoko-Jeremie/Degrees-of-Lewdity_Cheats-Mod/blob/master/src/GreasemonkeyScript/init.ts)

3. [KinkiestDungeon_Mod_enchanted_restraints](https://github.com/Lyoko-Jeremie/KinkiestDungeon_Mod_enchanted_restraints) , see [file](https://github.com/Lyoko-Jeremie/KinkiestDungeon_Mod_enchanted_restraints/blob/master/src/GreasemonkeyScript/init.ts)


