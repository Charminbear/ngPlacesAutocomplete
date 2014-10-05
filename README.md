ngPlacesAutocomplete
====================

A simple Directive to easily add the autocomplete feature of the Google Places Service to a Textbox. 
Feel free to contribute or leave an issue here on Github if you are missing functionality or want to report
a bug.


##How to use

First download the directive, either with `bower` or `npm`:

    npm install ng-places-autocomplete --save

or 

    bower install ng-places-autocomplete --save

Then refer it inside your index.html, careful to do this **after** the Google-Javascript-API and Angular, but **before** your 
app.js:

```HTML
<script type="text/javascript" src="http://maps.googleapis.com/maps/api/js?libraries=places&sensor=false"></script>
<script src="../bower_components/angular/angular.min.js"></script>
<script src="../ngPlacesAutocomplete.min.js"></script>
<script src="app.js"></script>
```

Just use it as a HTML-Attribute on a text-input as you would every other directive:

```HTML
<input  type="text" 
        ng-places-autocomplete 
        pa-options="optionsObject" 
        pa-on-details-ready="callbackFunction"
/> 
```

##API
The directive offers two attributes:

**paOnPlaceReady** - Expects a Callback-Function that gets executed everytime a user chose a place from the autocomplete-window. 
The function get

**paOptions** (optional) - The Options Object to configure the autocomplete-service. It takes the exact same values as
the Google-Places-Service described [here](https://developers.google.com/maps/documentation/javascript/reference#AutocompleteOptions). 
The given Options-Object is being watched and therefore automatically adjusts to changes you make.

##Todos
* Make free text search for an address available
* Write some tests
* Add more examples which actually use options
* Implement "bind" option for bounds of map


##License
Copyright (c) <2014> <David Losert>
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.