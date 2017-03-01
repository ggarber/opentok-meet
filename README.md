[![Build Status](https://travis-ci.org/opentok/opentok-meet.svg?branch=master)](https://travis-ci.org/opentok/opentok-meet)
[![Code Climate](https://codeclimate.com/github/opentok/opentok-meet/badges/gpa.svg)](https://codeclimate.com/github/opentok/opentok-meet)
[![Test Coverage](https://codeclimate.com/github/opentok/opentok-meet/badges/coverage.svg)](https://codeclimate.com/github/opentok/opentok-meet/coverage)

opentok-meet
===============

Opentok app with screen sharing using the WebRTC screen sharing and Archiving features. You can check it out running at [meet.tokbox.com](https://meet.tokbox.com).

## Disclaimer


>This is a fork of the [opentok-meet](https://github.com/aullman/opentok-meet) project that deploys to [meet.tokbox.com](https://meet.tokbox.com). It is pointing to the OpenTok nightly environment which is experimental and likely to break. It also includes experimental features.

>If you wish to fork this project, please fork the [parent project](https://github.com/aullman/opentok-meet).

1. If you haven't already, [sign up for OpenTok](https://tokbox.com/signup).
1. Clone this repo
2. `cp config.json.sample config.json`
3. Add your OpenTok apikey and secret to config.json
4. Create your screensharing extensions by following the instructions at https://github.com/opentok/screensharing-extensions and put your Chrome Extension ID in config.json.
4. Run redis. You can find instructions for doing this [here](https://redis.io/topics/quickstart).
5. `npm install` (you will need at least 1GB memory for this step)
6. If you want to use SSL you will need to generate a key and make sure the server.key and server.crt files are in the main directory. You can find instructions for generating a self-signed certificate [here](https://devcenter.heroku.com/articles/ssl-certificate-self). SSL is recommended so that screen-sharing works and so that you don't have to keep clicking the allow button to allow access to your camera. If you still don't want to use SSL then just update [app.js](app.js) to use `http.createServer` instead of `https.createServer`.
7. `npm start`
8. Go to https://localhost:3000

## Deploying to meet.tokbox.com

If you push to the master branch of this repo [Travis](https://travis-ci.org/opentok/opentok-meet) and [BrowserStack](https://browserstack.com/automate) tests will run and when they pass meet.tokbox.com will be updated.
