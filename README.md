# Backbone.webStorage (fork of Backbone.localStorage)

Quite simply an HTML5 WebStorage adapter for Backbone's sync functionality. It's a drop-in replacement for Backbone.Sync() to handle saving to a localStorage or sessionStorage database.

## Usage

Include Backbone.webStorage after having included Backbone.js:

    <script type="text/javascript" src="backbone.js"></script>
    <script type="text/javascript" src="backbone.webStorage.js"></script>

Create your collections like so:

    window.SomeCollection = Backbone.Collection.extend({
      
      localStorage: new Backbone.Storage("SomeCollection"), // Unique name within your app - all keys are prepended with this
      
      // ... everything else is normal.
      
    });
  
Feel free to use Backbone as you usually would, this is a drop-in replacement.

## LocalStorage versus SessionStorage

Backbone.webStorage supports both localStorage and sessionStorage mechanisms. Default implementation uses localStorage,
however you can switch to a sessionStorage mechanism by creating a new Backbone.Storage object with the second optional
type parameter. E.g.

    localStorage: new Backbone.Storage("SomeCollection", "session"),

## Credits

Forks from jeromegn (original Backbone.localStorage) and ajpiano for the sessionStorage support. Other bugfixes merged from the network.
