# backbone.mapview

Provides a Backbone.View backed abstraction for using maps in your application.
Currently only supports Google Maps but more are planned in the future.

Depends on Underscore.js, Backbone.js, either jQuery or Zepto and a 
compatible browser-based map api.

## Download & Setup ##

Development contains the fully commented source, Production is minified and 
stripped of all comments except for license/credits.

* [Development](https://raw.github.com/gsmaverick/backbone.mapview/master/backbone.mapview.js)
* [Production](https://raw.github.com/gsmaverick/backbone.mapview/master/backbone.mapview.min.js)

Include in your application *after* Zepto/jQuery, Underscore, and Backbone have 
been included.

``` html
<script src="/js/jquery.js"></script>
<script src="/js/underscore.js"></script>
<script src="/js/backbone.js"></script>

<script src="/js/backbone.mapview.js"></script>
```


## Configuration  ##

There are a number of options available to adjust the behaviour of Backbone.MapView.

* __center__:
A `google.maps.LatLng` instance that denotes the location on which the map should
be centered on when it is loaded.

``` javascript
center: null
```

* __mapOpts__:
A hash of options that are passed to the constructor of the Google Map.


``` javascript
mapOpts: {
  zoom: 13
  mapTypeId: google.maps.MapTypeId.ROADMAP
  streetViewControl: false
}
```