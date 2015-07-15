# npm variables example

An example using npm package variables and [Surge](https://surge.sh) in an npm run script.

## Getting started

Deploy to [Surge](https://surge.sh) with an npm run script: `npm run deploy`.

Use other keys within your `package.json` file as part of your npm run script. Since you already have metadata like the URL of the project, in the `package.json`, why not make it part of your run script too?

```js
"scripts": {
  "deploy": "surge --domain $npm_package_homepage"
}
```

You might even make the `main` filed the source directory:

```js
"script": {
  "deploy": "surge --project $npm_package_main --domain $npm_package_homepage"
}
```

The variable-based approach was inspired by [this tweet](https://twitter.com/juice49/status/621439134310223872) from @juice49.

## License

[The MIT License (MIT)](LICENSE.md)

Copyright © 2015 [Chloi Inc.](http://chloi.io)
