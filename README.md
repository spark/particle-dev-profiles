# Particle Dev Profiles package

[![Build Status](https://travis-ci.org/spark/particle-dev-profiles.svg?branch=master)](https://travis-ci.org/spark/particle-dev-profiles) [![](https://img.shields.io/badge/docs-latest-brightgreen.svg?style=flat)](http://spark.github.io/particle-dev-profiles/) [![apm](https://img.shields.io/apm/v/particle-dev-profiles.svg?maxAge=2592000)]()

Package providing support for Particle CLI profiles and basic Particle Cloud authentication.

## Usage

This package provides [a service](http://flight-manual.atom.io/behind-atom/sections/interacting-with-other-packages-via-services/) which other packages can consume:

`package.json`
```json
"consumedServices": {
  "particle-dev-profiles": {
    "versions": {
      "^0.0.1": "consumeProfiles"
    }
  }
}
```

`main.coffee`
```coffeescript
consumeProfiles: (@profileManager) ->
	console.log @profileManager.currentProfile
```

## API reference

When consuming profile manager you'll get instance of `ProfileManager` which [following API](http://spark.github.io/particle-dev-profiles/).
