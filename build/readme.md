# Custom Loaders

## Fluent Loader

The fluent loader "compiles" `.ftl` files into `.js` files directly usable by both the frontend and server for localization.

## Generate Asset Map

This loader enumerates all the files in `assets/` so that `common/assets.js` can provide mappings from the source filename to the hashed filename used on the site.

## Generate L10N Map

This loader enumerates all the ftl files in `public/locales` so that the fluent loader can create it's js files.

## Package.json Loader

This loader creates a `version.json` file that gets exposed by the `/__version__` route from the `package.json` file and current git commit hash.

## Version Loader

This loader substitutes the string "VERSION" for the version string specified in `package.json`. This is a workaround because `package.json` already uses the `package_json_loader`. See [app/templates/header/index.js](../app/templates/header/index.js) for more info.

# See Also

- [docs/build.md](../docs/build.md)
- [webpack.config.js](../webpack.config.js)