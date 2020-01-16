<img align="left" style="padding:10px" src="http://pomegranate.io/img/pomegranate_100.png" >

# Pomegranate 7 Beta

#### A wildly flexible application framework.

# What does it do?

Simply? Pomegranate is a framework to build other frameworks, though it just as happily handles general application programming tasks.

Pomegranate is a graybox, Inversion of Control based application framework. It ingests simple plugins, sorts them topologically and runs the hooks they expose. It supports polymorphic dependencies and simple, expressive configuration external to its plugins. It maintains the lifecycle of plugins, so you don't have to.

By wrapping the key elements of your application, you are able to consistently generate reusable components for future projects.

Steve Jobs once spoke of Objective-C, and a day when developers wouldn't focus on writing a network stack, or a database connection. They would simply open up their toolbox, with these items, and just connect the scaffolding that enables their business application to work. Pomegranate is a tools that makes that happen.

***
[![NPM Version][npm-image]][npm-url]
[![Linux][travis-image]][travis-url]
***

# Beta installation

```bash
yarn add pomegranate@beta
yarn add --dev pomegranate-cli

Unless you have `./node_modules/.bin` as part of your $PATH, or have Pomegranate installed globally, make sure you add it.

pom init myProject
pom application configure --environment (pom a c -e)
pom application build --clean (pom a b -c)
pom start
```

# Install and configure plugins

```bash
yarn add @restmatic/server

```

Edit `pomegranateSettings.js#pluginNamespaces` to make them visible to Pomegranate.

`pluginNamespaces: ['restmatic']`


```bash
pom a c -e #builds plugins configs and directory structure
pom plugin @restmatic/router generate my/path # generates a route file
pom a b -c
pom start
```

[doc-url]: http://pomegranate.paperelectron.com
[npm-image]: https://img.shields.io/npm/v/pomegranate.svg
[npm-url]: https://www.npmjs.com/package/pomegranate
[travis-image]: https://travis-ci.org/Pomegranate/Pomegranate.svg?branch=master
[travis-url]: https://travis-ci.org/Pomegranate/Pomegranate
