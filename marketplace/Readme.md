# Marketplace extensions

This directory contains production quality extensions for the
[Extension Marketplace](https://www.contentful.com/developers/marketplace).

These extensions are production quality and ready to use out of the box.

## Development

Extensions should be created using `create-contentful-extension`. After copying them over the require only minimal
modifications:

- Add a `version` property to `package.json` with the value `1.0.0` or higher.
- Add unit tests. Preferably using Jest.

  - Modify `.babelrc` to be environments aware.

    There need to be at environments for `test` (for Jest), `production` and `development`. The `test` environment must
    include the transformation of EcmaScript Modules to CommonJS while the other environments should omit this step.

- Follow the code formatting and linting rules of this directory.
- Add a file called `MARKETPLACE.md` containing the text for the marketplace listing. If it does not exist, the
  marketplace will fallback to a `README.md`, but it's better to have a more user-focused text for the marketplace. If
  neither file exists the marketplace won't list the extension.
