## 01. Installing Node.js

### Using Macbook
```
brew install node
```

#### Check if the frameworks have been installed

```
npm -v
node -v
```

## 02. Creating a new package of the current directory

```
npm init
```

## 03. Installing packages

#### Install packages globally

Installing live server globally

```shell
npm install -g live-server
```

If error for permission arrises, use sudo

```shell
sudo npm install -g live-server
```

#### Installing packages locally

Lodash is an extension of javascript, really good helper framework when dealing with complex data manipulation in javascript

```shell
npm install lodash
```

If the package is locally, the package will be added to dependencies. The `node_modules` folder will contain the dependencies for the project.

We can then import modules locally into our scripts

```js
import { without } from 'lodash';
```

This will only work in `React`.

For this excercise we are going to be using `browserify`, this allow us to use the `require()` syntax

```shell
npm install -g browserify
```

Once installed we can then see we are able to use

```js
var _ = require('lodash');
```

We are able to bundle our js together with the require js files. We can do this by typing the following command.

```shell
browserify script.js > bundle.js
```

We want to be careful with this, it's a good idea to assess whether we need the package. We also need to take into concederation that our website will now have dependencies, while we have dependencies we need to make sure the project has the packages.

Never include the `node_modules` folder inside the GIT repo.

## 04. Updating Packages

We can use [semver.npmjs.com](https://semver.npmjs.com) to view packages and the version currently out on said packages.