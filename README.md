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

## Usage ##

You use Backbone.MapView like a regular view with a few exceptions.

```javascript
var View = Backbone.MapView.extend({
  // ... custom view methods here ...
});

var StreetMap = new View({ id: 'map' });
$('body').html(StreetMap.render().el);
```

## Configuration  ##

### Maps API Configuration ###

The options listed here are a list what's required to initialize a map and not 
the complete configuration reference.  For the full details consult the 
[Google Maps Reference](https://developers.google.com/maps/documentation/javascript/reference#MapOptions).
The map will be initialized with all the properties in this hash so you can
simply define more keys if you want to specify extra options.  All these values 
are stored in the `mapOpts` property.

* __center__:
A `google.maps.LatLng` instance that denotes the initial center of the map.  You
must specify a value for this property otherwise the map will not load and just
show a grey background.

``` javascript
center: null
```

* __mapTypeId__:
The initial Map [mapTypeId](https://developers.google.com/maps/documentation/javascript/reference#MapTypeId).

``` javascript
mapTypeId: google.maps.MapTypeId.ROADMAP
```

* __zoom__:
Initial map zoom level.

``` javascript
zoom: 15
```


### MapView Configuration ###