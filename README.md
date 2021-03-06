# MarkerClustererPlus

## Warning!

The following files have been deprecated and will be removed in the next release:
* [src/markerclusterer.min.js](https://github.com/mahnunchik/markerclustererplus/blob/master/src/markerclusterer.min.js)
* [src/markerclusterer_packed.js](https://github.com/mahnunchik/markerclustererplus/blob/master/src/markerclusterer_packed.js)

Use [dist/markerclusterer.min.js](https://github.com/mahnunchik/markerclustererplus/blob/master/dist/markerclusterer.min.js) instead.

---

This is an enhanced version of the MarkerClusterer library for managing large amounts of markers. It adds support for several new properties as well as support for four more events. It also allows greater control over the styling of the text that appears on the cluster marker. The documentation has been significantly improved and the overall code has been simplified and polished. Very large numbers of markers can now be managed without causing Javascript timeout errors on Internet Explorer. It is backward compatible with MarkerClusterer.

This is git version of the [google svn repo](http://google-maps-utility-library-v3.googlecode.com/svn/trunk/markerclustererplus/).

**This version allows es5 and es6 imports.**

### Installation

Install with [npm](https://www.npmjs.com/).

```bash
$ npm install markerclustererplus-node --save
```

### Usage

If using Angular 2+
```typescript
import MarkerClusterer = require('markerclustererplus-node');

let markers = [
  new google.maps.Marker()
]
// map = google map instance

let clusterer = new MarkerClusterer(map, [], options);
```

You can also use type MarkerClustererOptions
```typescript
import MarkerClusterer = require('markerclustererplus-node');

let clusterOptions: MarkerClustererOptions = {
  gridSize: 20,
  maxZoom: 10,
  zoomOnClick: true
}
let markers = [
  new google.maps.Marker()
]
// map = google map instance
let clusterer = new MarkerClusterer(map, markers, clusterOptions);
```

### Additional Features

* hideLabel option - removes numbers on the clusters

### Build

To rebuild a minified version of the library try the following commands:

```bash
$ npm install
$ npm run build
```

### License

[Apache License, Version 2.0](http://opensource.org/licenses/Apache-2.0)
