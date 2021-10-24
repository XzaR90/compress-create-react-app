[![npm version](https://img.shields.io/npm/v/compress-create-react-app.svg)](https://www.npmjs.com/package/compress-create-react-app)
[![npm monthly downloads](https://img.shields.io/npm/dm/compress-create-react-app.svg)](https://www.npmjs.com/package/compress-create-react-app)

Make your apps smaller by adding post build compression to your `create-react-app` build without configuration.

Compresses all html, css and javascript files in the build folder using brotli and gzip algorithms.

Feel free to create an issue for any problems you've had or if you want to request a new feature.

## Usage

##### 0) Create your app using create-react-app

#### 1) Installation

Install the package as a dev dependency:

```bash
npm install @xzar90/compress-create-react-app --save-dev
```

#### 2) Usage

Edit your app's build script in `package.json`:

```diff
  "scripts": {
    "start": "react-scripts start",
-   "build": "react-scripts build",
+   "build": "react-scripts build && compress-cra",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
  }
```

###### Custom build directory

Since version `1.1.0`, you can optionally provide a path to your build directory by adding `-d` or `--directory` argument to the command in your `package.json`:

```bash
...
"build": "react-scripts build && compress-cra -d /path/to/build",
...
```

The default build path is `/build`. The provided custom path should be a relative path from your project's **root directory**.

#### 3) Build your app just like you normally would

```bash
npm run build
```

#### 4) Make your server serve the compressed files

The way to set up your server highly depends on the server you use.

How to setup `express` server using [express-static-gzip](https://www.npmjs.com/package/express-static-gzip)
How to setup `asp.net core` server using [CompressedStaticFiles](https://github.com/AnderssonPeter/CompressedStaticFiles)

## Contributing

This is a small project that is currently maintained by one person. There are no strict contributing guidelines. If you're interested in contributing, see if there are any [issues](https://github.com/jnsjknn/compress-create-react-app/issues) you could help with or post a new one to suggest a feature.

## Donations

Due to Finnish laws, I can't accept direct donations. If you want to support the development of this package, you can buy a written greeting from me for 5€ (US \$6):

1. Send the payment for the greeting via [PayPal](https://paypal.me/jnsjknn).
2. Send the receipt to joonas@joonasjokinen.fi and you will receive your greeting within a week.

## License

This app is licensed under the [MIT License](LICENSE.md).
