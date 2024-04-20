# Creating and publishing scoped public packages 

```console
$ npm login --registry=https://registry.npmjs.org/
npm notice Log in on https://registry.npmjs.org/
Login at:
https://www.npmjs.com/login?next=/login/cli/58266ac2-33d9-41ac-94aa-77138a83785f
Press ENTER to open in the browser...
Logged in on https://registry.npmjs.org/.
$ npm whoami --registry=https://registry.npmjs.org/
jonx

$ npm publish --access public --registry https://registry.npmjs.org/
npm notice
npm notice í ½í³¦  @jonx/greeting@1.0.0
npm notice === Tarball Contents ===
npm notice 1.1kB LICENSE
npm notice 454B  README.md
npm notice 74B   index.js
npm notice 557B  package.json
npm notice === Tarball Details ===
npm notice name:          @jonx/greeting
npm notice version:       1.0.0
npm notice filename:      jonx-greeting-1.0.0.tgz
npm notice package size:  1.3 kB
npm notice unpacked size: 2.1 kB
npm notice shasum:        97276124df568ab1149b3150368fa212987544d7
npm notice integrity:     sha512-qi0ICL3BsvICi[...]Q2efflgzJXhiw==
npm notice total files:   4
npm notice
npm notice Publishing to https://registry.npmjs.org/ with tag latest and public access
+ @jonx/greeting@1.0.0
```

```sh
npm i @jonx/greeting
```

```console
$ cat package.json
{
  "type": "module",
  "scripts": {
    "start": "node ./index.js"
  },
  "dependencies": {
    "@jonx/greeting": "^1.0.0"
  }
}
$ cat index.js
import greeting from "@jonx/greeting";
greeting("Jon");
$ npm start

> start
> node ./index.js

Hi, Jon!
```
