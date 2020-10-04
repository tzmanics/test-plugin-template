must have a github account

https://github.com/netlify/build-plugin-template
'Use this template'

this will lead you to create a repo

*plugin name should match repo name:


```bash
? Plugin name coolest
? Description Coolio cool plugin
? Author name tzmanics
? Author email address tzmanics@gmail.com
? Software license MIT
? Source code repository //github.com/tzmanics/test-plugin-template
? Supported Node.js version >=10.22.0
```

development documentation in `CONTRIBUTING.md`

file structure:
![plugin template file structure](https://res.cloudinary.com/dzkoxrsdj/image/upload/v1601780981/Screen_Shot_2020-10-03_at_11.08.07_PM_qtlp8c.jpg)

## To the Core

- review and edit core filles
  - manifest.yml
  - `main.js` or `index.js`

## Catch & Release `main.js`

- go over what's in `main.js`
- `mv main.js ./main-template.js`
- touch `main.js`

## Log it Out

- review build events & logging

- `onPreBuild`: runs before the build command is executed.
- `onBuild`: runs directly after the build command is executed and before Functions bundling.
- `onPostBuild`: runs after the build command completes and after onBuild tasks and Functions bundling are executed.
- `onSuccess`: runs only when the build stage succeeds, but before deploy begins; cannot be used to fail a build.
- `onError`: runs only when an error occurs in the build stage, failing the build; before deploy begins.
- `onEnd`: runs after completion of the build stage, regardless of build error or success; before deploy begins.

## Test, Clean & Publish

`npm run lint` lints and prettifies

`npm run ava` runs test

`npm test` does both

`npm run release` will publish the plugin to `npm`

## Creating a Demo Site

### Adding a Status Badge

[Status Badge documentation]( https://docs.netlify.com/monitor-sites/status-badges/)