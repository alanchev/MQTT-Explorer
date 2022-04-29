# [MQTT Explorer](https://mqtt-explorer.com)

> ### This fork merely adds Dependabot's security patches. For anything else, refer to [the original repository by Thomas Nordquist](https://github.com/thomasnordquist/MQTT-Explorer).

## Run from sources

```bash
npm install -g yarn
yarn
yarn build
yarn start
```

## Develop

Launch Application
```bash
npm install -g yarn
yarn
yarn dev
```

The `app` directory contains all the rendering logic, the `backend` directory currently contains the models, tests, connection management, `src` contains all the electron bindings. [mqttjs](https://github.com/mqttjs/MQTT.js) is used to facilitate communication to MQTT brokers.

## Automated Tests

To achieve a reliable product automated tests run regularly on travis.

- Data model
- MQTT integration
- UI-Tests (The demo is a recorded ui test)

## Run UI-tests

A [mosquitto](https://mosquitto.org/) MQTT broker is required to run the ui-tests.

Run tests with

```bash
# Run chromedriver in a separate terminal session
./node_modules/.bin/chromedriver --url-base=wd/hub --port=9515 --verbose
```

Compile and execute tests

```bash
npm run build
node dist/src/spec/webdriverio.js
```
> Note: [additional options on how to build this app as a win32 executable](https://stackoverflow.com/a/40615892).

## License

![CC-BY-ND 4.0](https://img.shields.io/badge/License-CC%20BY--ND%204.0-blue.svg)  
[CC-BY-ND 4.0](https://creativecommons.org/licenses/by-nd/4.0/)

The license is a little restrictive to distributing derived work, this may change in the future if the interest arises or more people work on this project.
