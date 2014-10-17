# Journey Heroku Buildpack for Node.js

A Heroku buildpack for Node.js which:
 * stays as close as possible to the [offical buildpack](https://github.com/heroku/heroku-buildpack-nodejs)
 * installs `devDependencies` in addition to production `dependencies` in order to access build tools
 * supports [gulp.js](http://gulpjs.com/) build system.

## How it Works

Here's an overview of what this buildpack does:
 * Everything in the [offical buildpack](https://github.com/heroku/heroku-buildpack-nodejs)
 * Runs the `gulp heroku:$NODE_ENV` task during compile if `./gulpfile.js` exists (`$NODE_ENV` is typically `production`)

## Notes
 * Ensure your `devDependencies` (or `dependencies`) contain an entry for gulp.
 