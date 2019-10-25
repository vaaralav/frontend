[![Build Status](https://travis-ci.org/DependencyTrack/frontend.svg)](https://travis-ci.org/DependencyTrack/frontend)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/5d481daa38134900abe88e9e064e05c7)](https://www.codacy.com/manual/DependencyTrack/frontend?utm_source=github.com&utm_medium=referral&utm_content=DependencyTrack/frontend&utm_campaign=Badge_Grade)
[![License](https://img.shields.io/badge/license-Apache%202.0-brightgreen.svg)][license]

# Dependency-Track Front End

This repo contains a 2nd experimental front-end web client for OWASP Dependency-Track. The project is built with:

- Vue 2.x / CLI 3.x
- Bootstrap Vue
- CoreUI

## Build Setup

```bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run serve

# build for production with minification
npm run build

# run linter
npm run lint
```

## Development Setup

In order to test with a Dependency-Track instance, the `.env.development` file needs to be modified and the `VUE_APP_SERVER_URL` property updated to
reflect the base URL of a Dependency-Track server.

### Use docker-compose to run the backend

Make sure memory limit of your Docker containers is [high enough for Dependency-Track](https://docs.dependencytrack.org/getting-started/deploy-docker/).

In backend/ directory run `docker-compose up -d`. This starts containers for PostgeSQL and Dependency-Track. It takes some time to initially start Dependency-Track. Dependency-Track will be available at http://localhost:1337. Use this address in `.env.development`.

## Internationalization (i18n)

This project supports internationalization. Currently on English language is supported. Pull requests to support additional languages are encouraged.

Note to developers: Textual labels are defined in `src/i18n/messages.json`. Ensure that all labels are defined here and that components use i18n, not textual labels directly.

## Copyright & License

Dependency-Track is Copyright (c) Steve Springett. All Rights Reserved.

Permission to modify and redistribute is granted under the terms of the
Apache 2.0 license. See the [LICENSE] file for the full license.

[license]: https://github.com/DependencyTrack/frontend/blob/master/LICENSE
