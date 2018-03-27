# `react-scripts-ts` [![npm version](https://badge.fury.io/js/react-scripts-ts.svg)](https://badge.fury.io/js/react-scripts-ts) [![Build Status](https://travis-ci.org/wmonk/create-react-app-typescript.svg?branch=master)](https://travis-ci.org/wmonk/create-react-app-typescript)

Create React apps (with Typescript) with no build configuration.

 * [Creating an App](#creating-an-app) – How to create a new app.
 * [User Guide](https://github.com/wmonk/create-react-app-typescript/blob/master/packages/react-scripts/template/README.md) – How to develop apps bootstrapped with react scripts ts.

_Do you know react and want to try out typescript? Or do you know typescript and want to try out react?_ Get all the benefits from `create-react-app` but you use typescript! 🚀

Create React App works on macOS, Windows, and Linux.<br>
If something doesn’t work, please [file an issue](https://github.com/wmong/create-react-app/issues/new).

## Quick Overview

```sh
npx create-react-app --scripts-version=react-scripts-ts my-app
cd my-app/
npm start
```

*([npx](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b) comes with npm 5.2+ and higher, see [instructions for older npm versions](https://gist.github.com/gaearon/4064d3c23a77c74a3614c498a8bb1c5f))*

Then open [http://localhost:3000/](http://localhost:3000/) to see your app.<br>
When you’re ready to deploy to production, create a minified bundle with `npm run build`.

<p align='center'>
<img src='https://cdn.rawgit.com/facebook/create-react-app/27b42ac/screencast.svg' width='600' alt='npm start'>
</p>

### Get Started Immediately

You **don’t** need to install or configure tools like Webpack or Babel.<br>
They are preconfigured and hidden so that you can focus on the code.

Just create a project, and you’re good to go.

## Migration

In general, most upgrades won't require any migration steps to work, but if you experience problems after an upgrade, please file an issue, and we'll add it to the list of migration steps below.

### From `<2.13.0` to `>=2.13.0`

Since `2.13.0`, `typescript` is listed as a peer dependency of `react-scripts-ts`. For projects generated with at least this version, the init script takes care of properly installing it as dev dependency to the generated projects. Older projects require manual installation, in case you have not already done that.

Using `npm`:
```
npm i -D typescript
```

Using `yarn`:
```
yarn add -D typescript
```

### From `<2.5.0` to `>=2.5.0`

Version `2.5.0` introduces a new config file for jest, that is necessary for the tests to run. If you were previously running a version older than `v2.5.0` and upgraded to `v2.5.0` or newer, you need to manually add the new file, or else you'll get an error similar to this when trying to run your tests:

```javascript
Test suite failed to run
{
    "messageText": "Cannot read file 'C:\\[project]\\tsconfig.test.json': ENOENT: no such file or directory, open 'C:\\[project]\\tsconfig.test.json'.",
    "category": 1,
    "code": 5012
}
```

To fix this, create a new file *in the root of the project* called `tsconfig.test.json`, and paste [the content of this file into it](https://raw.githubusercontent.com/wmonk/create-react-app-typescript/master/packages/react-scripts/template/tsconfig.test.json). Everything should work now. For more info, please see [this issue](https://github.com/wmonk/create-react-app-typescript/issues/141).

## Changelog

### 2.14.0
* README fixes - @kaminskypavel
* README fixes - @adambowles
* Remove unused JS files - @DorianGrey
* README fixes - @stephtr
* Added the abillity to import js and jsx files with ts-loader - @GeeWee
* Uglifyjs update for es6 support - @thetric

### 2.13.0
* Remove tslint-loader from prod builds - @DorianGrey
* Include typescript as devDependency in boilerplate - @ianschmitz
* Document custom module formats - @joshtynjala
* Fix tsconfig.json - @diabelb

### 2.12.0
* Update typescript to 2.6.2

### 2.11.0
* Upgrade to [`react-scripts@1.0.17`](https://github.com/facebookincubator/create-react-app/releases/tag/v1.0.17)

### 2.10.0
* README updates - StefanSchoof
* README updates - DorianGrey
* Add support for fork-ts-checker-webpack-plugin - johnnyreilly

### 2.9.0 - UNPUBLISHED
This included changes that were not published by the facebook upstream, so was unpublished.

### 2.8.0
* Update typescript to 2.5.3 - @nicolaserny

### 2.7.0
* Merge react-scripts@1.0.13 - @JohnNilsson
* Fix git tempalte - @hktonylee
* Provide migration docs - @JReinhold
* Updated dependencies - @swengorschewski
* Fix tslint config - @comerc

### 2.6.0
* Merge react-scripts@1.0.10 - @wmonk
* Update component template - @pelotom

### 2.5.0
* Support dynamic imports - thanks @nicolaserny, @DorianGrey
* Fix up tsconfig - thanks @js-n
* Fix readme typo - thanks @adambowles
* Move to ts-jest - thanks @DorianGrey

### 2.4.0
* Upgrade typescript to 2.4 and ts-loader to 2.2.1 - thanks @frederickfogerty
* Fix readme typo - thanks @wrongway4you

### 2.3.2
* Fix `typescript` version to 2.3.x until 2.4 @types are fixed

### 2.3.1

* All tsc to parse config (for `extend`) - Thanks to @DorianGrey
* Fix various jest issues - thanks to @zinserjan
* Fix code coverage - thanks to @zinserjan

### 2.2.0
* Upgrade to [`react-scripts@1.0.6`](https://github.com/facebookincubator/create-react-app/)

### 2.1.0
* Update to `tslint@5.2.0` - thanks to @mindjuice
* Fix test setup issue - thanks to @jonmpqts
* Add `source-map-loader` - thanks to @Place1
* Update to `typescript@2.3.3` - thanks to @sjdweb

### 2.0.1
* Fix issue with jest finding test files

### 2.0.0
* Upgrade to [`react-scripts@1.x.x`](https://github.com/facebookincubator/create-react-app/blob/0d1521aabf5a0201ea1bcccc33e286afe048f820/CHANGELOG.md)

### 1.4.0
* Upgrade to typescript@2.3.2 - thanks to @patrick91
* Add tests around react-scripts-ts - thanks to @migerh

### 1.3.0
* Upgrade to typescript@2.2.2 - thanks to @jeremistadler

### 1.1.8
* Fix regression where no `@types` were being installed on init

### 1.1.7
* Merge facebookincubator/create-react-app@0.9.5 into react-scripts-ts
* Merge facebookincubator/create-react-app@0.9.4 into react-scripts-ts
* Merge facebookincubator/create-react-app@0.9.3 into react-scripts-ts
* Merge facebookincubator/create-react-app@0.9.2 into react-scripts-ts
* Merge facebookincubator/create-react-app@0.9.1 into react-scripts-ts

### 1.1.6
* Merge facebookincubator/create-react-app@0.9.0 into react-scripts-ts

### 1.0.6
* Add missing `cli-highlight` dependency

### 1.0.5
* Print file names when running `npm run build`
* Add support for `setupTest.ts`
* Highlight source code when erroring in `npm run build`

### 1.0.4
* Change mentions of `eslint` to `tslint`

### 1.0.3
* Remove hidden character from `tsconfig.json`

### 1.0.2
* Copy `typescriptTransform.js` when running `npm run eject`


## Creating an App

**You’ll need to have Node >= 6 on your local development machine** (but it’s not required on the server). You can use [nvm](https://github.com/creationix/nvm#installation) (macOS/Linux) or [nvm-windows](https://github.com/coreybutler/nvm-windows#node-version-manager-nvm-for-windows) to easily switch Node versions between different projects.

To create a new app, run a single command:

```sh
npx create-react-app --react-scripts=react-scripts-ts my-app
```

*([npx](https://medium.com/@maybekatz/introducing-npx-an-npm-package-runner-55f7d4bd282b) comes with npm 5.2+ and higher, see [instructions for older npm versions](https://gist.github.com/gaearon/4064d3c23a77c74a3614c498a8bb1c5f))*

No configuration or complicated folder structures, just the files you need to build your app.<br>
Once the installation is done, you can open your project folder:

```sh
cd my-app
```

Inside the newly created project, you can run some built-in commands:

### `npm start` or `yarn start`

Runs the app in development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will automatically reload if you make changes to the code.<br>
You will see the build errors and lint warnings in the console.

<p align='center'>
<img src='https://cdn.rawgit.com/marionebl/create-react-app/9f62826/screencast-error.svg' width='600' alt='Build errors'>
</p>

[Read more about testing.](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#running-tests)

### `npm run build` or `yarn build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
By default, it also [includes a service worker](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#making-a-progressive-web-app) so that your app loads from local cache on future visits.

Your app is ready to be deployed.

## User Guide

The [User Guide](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md) includes information on different topics, such as:

- [Updating to New Releases](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#updating-to-new-releases)
- [Folder Structure](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#folder-structure)
- [Available Scripts](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#available-scripts)
- [Supported Browsers](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#supported-browsers)
- [Supported Language Features and Polyfills](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#supported-language-features-and-polyfills)
- [Syntax Highlighting in the Editor](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#syntax-highlighting-in-the-editor)
- [Displaying Lint Output in the Editor](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#displaying-lint-output-in-the-editor)
- [Formatting Code Automatically](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#formatting-code-automatically)
- [Debugging in the Editor](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#debugging-in-the-editor)
- [Changing the Page `<title>`](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#changing-the-page-title)
- [Installing a Dependency](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#installing-a-dependency)
- [Importing a Component](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#importing-a-component)
- [Code Splitting](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#code-splitting)
- [Adding a Stylesheet](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#adding-a-stylesheet)
- [Post-Processing CSS](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#post-processing-css)
- [Adding a CSS Preprocessor (Sass, Less etc.)](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#adding-a-css-preprocessor-sass-less-etc)
- [Adding Images, Fonts, and Files](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#adding-images-fonts-and-files)
- [Using the `public` Folder](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#using-the-public-folder)
- [Using Global Variables](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#using-global-variables)
- [Adding Bootstrap](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#adding-bootstrap)
- [Adding Flow](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#adding-flow)
- [Adding a Router](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#adding-a-router)
- [Adding Custom Environment Variables](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#adding-custom-environment-variables)
- [Can I Use Decorators?](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#can-i-use-decorators)
- [Fetching Data with AJAX Requests](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#fetching-data-with-ajax-requests)
- [Integrating with an API Backend](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#integrating-with-an-api-backend)
- [Proxying API Requests in Development](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#proxying-api-requests-in-development)
- [Using HTTPS in Development](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#using-https-in-development)
- [Generating Dynamic `<meta>` Tags on the Server](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#generating-dynamic-meta-tags-on-the-server)
- [Pre-Rendering into Static HTML Files](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#pre-rendering-into-static-html-files)
- [Running Tests](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#running-tests)
- [Debugging Tests](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#debugging-tests)
- [Developing Components in Isolation](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#developing-components-in-isolation)
- [Publishing Components to npm](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#publishing-components-to-npm)
- [Making a Progressive Web App](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#making-a-progressive-web-app)
- [Analyzing the Bundle Size](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#analyzing-the-bundle-size)
- [Deployment](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#deployment)
- [Advanced Configuration](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#advanced-configuration)
- [Troubleshooting](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#troubleshooting)

A copy of the user guide will be created as `README.md` in your project folder.

## How to Update to New Versions?

Please refer to the [User Guide](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#updating-to-new-releases) for this and other information.

## Philosophy

* **One Dependency:** There is just one build dependency. It uses Webpack, Babel, ESLint, and other amazing projects, but provides a cohesive curated experience on top of them.

* **No Configuration Required:** You don't need to configure anything. Reasonably good configuration of both development and production builds is handled for you so you can focus on writing code.

* **No Lock-In:** You can “eject” to a custom setup at any time. Run a single command, and all the configuration and build dependencies will be moved directly into your project, so you can pick up right where you left off.

## What’s Included?

Your environment will have everything you need to build a modern single-page React app:

* React, JSX, ES6, and Flow syntax support.
* Language extras beyond ES6 like the object spread operator.
* Autoprefixed CSS, so you don’t need `-webkit-` or other prefixes.
* A fast interactive unit test runner with built-in support for coverage reporting.
* A live development server that warns about common mistakes.
* A build script to bundle JS, CSS, and images for production, with hashes and sourcemaps.
* An offline-first [service worker](https://developers.google.com/web/fundamentals/getting-started/primers/service-workers) and a [web app manifest](https://developers.google.com/web/fundamentals/engage-and-retain/web-app-manifest/), meeting all the [Progressive Web App](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#making-a-progressive-web-app) criteria.
* Hassle-free updates for the above tools with a single dependency.

Check out [this guide](https://github.com/nitishdayal/cra_closer_look) for an overview of how these tools fit together.

The tradeoff is that **these tools are preconfigured to work in a specific way**. If your project needs more customization, you can ["eject"](https://github.com/facebook/create-react-app/blob/master/packages/react-scripts/template/README.md#npm-run-eject) and customize it, but then you will need to maintain this configuration.

## Popular Alternatives

Create React App is a great fit for:

* **Learning React** in a comfortable and feature-rich development environment.
* **Starting new single-page React applications.**
* **Creating examples** with React for your libraries and components.

Here’s a few common cases where you might want to try something else:

* If you want to **try React** without hundreds of transitive build tool dependencies, consider [using a single HTML file or an online sandbox instead](https://reactjs.org/docs/try-react.html).

* If you need to **integrate React code with a server-side template framework** like Rails or Django, or if you’re **not building a single-page app**, consider using [nwb](https://github.com/insin/nwb), or [Neutrino](https://neutrino.js.org/) which are more flexible. For Rails specifically, you can use [Rails Webpacker](https://github.com/rails/webpacker).

* If you need to **publish a React component**, [nwb](https://github.com/insin/nwb) can [also do this](https://github.com/insin/nwb#react-components-and-libraries), as well as [Neutrino's react-components preset](https://neutrino.js.org/packages/react-components/).

* If you want to do **server rendering** with React and Node.js, check out [Next.js](https://github.com/zeit/next.js/) or [Razzle](https://github.com/jaredpalmer/razzle). Create React App is agnostic of the backend, and just produces static HTML/JS/CSS bundles.

* If your website is **mostly static** (for example, a portfolio or a blog), consider using [Gatsby](https://www.gatsbyjs.org/) instead. Unlike Create React App, it pre-renders the website into HTML at the build time.

* If you want to use **TypeScript**, consider using [create-react-app-typescript](https://github.com/wmonk/create-react-app-typescript).

* Finally, if you need **more customization**, check out [Neutrino](https://neutrino.js.org/) and its [React preset](https://neutrino.js.org/packages/react/).

All of the above tools can work with little to no configuration.

If you prefer configuring the build yourself, [follow this guide](https://reactjs.org/docs/add-react-to-an-existing-app.html).

