Leaflet Routing Machine / Locationiq
=====================================

Extends [Leaflet Routing Machine](https://github.com/perliedman/leaflet-routing-machine) with support for [Locationiq](https://locationiq.com/docs) directions API.

Some brief instructions follow below, but the [Leaflet Routing Machine tutorial on alternative routers](http://www.liedman.net/leaflet-routing-machine/tutorials/alternative-routers/) is recommended.

## Installing

```sh
npm install --save leaflet-routing-machine-locationiq
```

## Using

There's a single class exported by this module, `L.Routing.Locationiq`. It implements the [`IRouter`](http://www.liedman.net/leaflet-routing-machine/api/#irouter) interface. Use it to replace Leaflet Routing Machine's default OSRM router implementation:

```javascript
var L = require('leaflet');
require('leaflet-routing-machine');
require('lrm-locationiq'); // This will tack on the class to the L.Routing namespace

L.Routing.control({
    router: new L.Routing.Locationiq('your api key'),
}).addTo(map);
```

Note that you will need to pass a valid Locationiq Api key to the constructor.


This is forked version based on [OSRMv1 perliedman](https://github.com/perliedman/leaflet-routing-machine/blob/master/src/osrm-v1.js)
