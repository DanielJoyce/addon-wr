# PUG ARG Experience.

This plugin is designed to ruin all goodwill Mozilla has in the opensource community, by being pushed out to users as part of an ad campaign between Mozilla and Comcast, the creators of Mr Robot

While for decades Mozilla has sought to educate users on safe browsing, this plugin makes your browser or computer appear to be infected by malware. Not only that, it is pushed out to you without your approval as part of a "Mozilla Study".

In the past Mozilla used their telemetry and studie process to collect data on user - site interactions and to design a safer firefox. But now that it's being used for advertising without any kind of warning, feel free to disable it!

Preferences -> Privacy & Security ( Hah! ) -> Scroll down to "FireFox Data Collection and Use". Uncheck telemetry and "Allow firefox to install and run studies".

Then go to Add-Ons, and remove the Looking Glass garbage.

Time to look for a well run fork that doesn't pull this nonsense.

## Getting started

```
# install depndencies
npm install

## build
npm run eslint
npm run build

## build and run
npm run firefox
```

### Details

First, make sure you are on NPM 5+ installed so that the proper dependencies are installed using the package-lock.json file.

`$ npm install -g npm`

After cloning the repo, you can run the following commands from the top level directory, one after another:

```
npm install
npm run build
```

This packages the add-on into `dist/linked-addon.xpi`. This file is the addon you load into Firefox.

Note: `linked-addon.xpi` is a symbolic link to the extension's true XPI, which is named based on the study's unique `addon.id` specified in `package.json`.


## User Experience / Functionality

See [./testplan.md](./testplan.md)

## Interesting files / dirs

1. `npm run build`.  Built addons go in `dist/`
2. `addon/` contains all files that go into the Embedded WebExtension
3. `bin/xpi.sh` zips up the addon directory into the addon.
