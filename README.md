# IDSK 3.0 Core Library

This library contains core styles and assets for IDSK 3.0 template framework. The purpose of this library is to have unified styles and assets for IDSK component libraries built with various technologies (React, HTML, ...)

## Library usage

The npm packages for this library are stored in Gitlab:

https://gitlab.slovenskoit.sk/components/shared-web-libs/esvk_web_lib_idsk_core/-/packages

To be able to install the `@eslovensko/idsk-core` package you need these credentials to be stored in `.npmrc` file:
```
@eslovensko:registry=https://gitlab.slovenskoit.sk/api/v4/packages/npm/
//gitlab.slovenskoit.sk/api/v4/packages/npm/:_authToken=5MU3Q9noGTTLvf6JcznZ
```

Then you can add the library to your project dependencies
```
npm install @eslovensko/idsk-core
```

## Library development

### Install dependencies

```
npm install
```

### Build styles

```
npm run build-styles
```
This builds the `idsk3_theme.css` stylesheet using Tailwind framework (https://tailwindcss.com)
Currently, this library depends on the `idsk-react` library (https://gitlab.slovenskoit.sk/components/shared-web-libs/esvk_web_lib_idsk_react), because this is where the components are being created and styled. Only the css classes used in the `idsk-react` project are included in the final `idsk3_theme.css` stylesheet. 

### Build the library

```
npm run rollup
```
This builds the styles and copies the assets into `dist` folder.

### Publish the library

We don't publish the library locally. The npm package is published automatically during Gitlab CI pipeline when merged into develop branch.
Just **make sure to increment the project version in package.json** whenever you make any changes.


