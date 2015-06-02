### Bootstrap list picker
Extends HTML's native multiple-select input to provide additional functionality. Introduces a [ListPicker](https://github.com/0xC70FF3/bootstrap-list-picker/blob/master/js/bootstrap-listpicker.js) class that operates behind the scenes to handle multiple-select inputs by listening on their events.

[Bootstrap](http://twitter.github.io/bootstrap/) list picker works better when used with [Bootstrap input clear button](https://github.com/mahpour/bootstrap-input-clear-button/blob/master/bootstrap.input-clear.js) from Ehsan Mahpour.

##### Demo
A live demo can be found [here](http://0xc70ff3.github.io/demos/bootstrap-listpicker/).

##### Installation
- Download the lastest version [here](https://github.com/0xC70FF3/bootstrap-list-picker/archive/master.zip) and unzip.
- Include `css/bootstrap-listpicker.css` after the main bootstrap css files.
- Include `js/bootstrap.input-clear.js` and `js/bootstrap-listpicker.js` after the main bootstrap js files.
 
##### HTML Code Example
This example can also be seen in action in index.html:
```html
    <!-- Core CSS -->
    <link rel="stylesheet" type="text/css" href="css/bootstrap.min.css" />
    <link rel="stylesheet" type="text/css" href="css/bootstrap-responsive.min.css" />
        
    <!-- Plugins CSS -->
    <link rel="stylesheet" type="text/css" href="css/bootstrap-listpicker.min.css"/>
        
    <!-- Core SCRIPTS -->
    <script type="text/javascript" src="js/jquery-1.8.2.min.js"></script>
    <script type="text/javascript" src="js/bootstrap.min.js"></script>
        
    <!-- Plugins SCRIPTS -->
    <script type="text/javascript" src="js/jquery.input-clear.js"></script>
    <script type="text/javascript" src="js/bootstrap-listpicker.min.js"></script>

    <!-- Custom SCRIPTS -->
    <script type="text/javascript">
        $(document).ready(function() {
            $('select[multiple="multiple"]').listpicker();
        });
    </script>

    <form method="post">
        <select multiple="multiple" name="data[model][field][]">
            <option data-tabs="A" value="1">option 1</option>
            <option data-tabs="B" value="2" disabled="disabled">option 2</option>
            <option data-tabs="C" value="3">option 3</option>
            <option data-tabs="A,C" value="4">option 4</option>
            <option value="5" selected="selected">option 5</option>
        </select>
    </form>
```

##### Configuration Options
###### sort
Define if the picker source list have to be sorted or not at anytime.
```javascript
$(document).ready(function() {
    $(".myList").listpicker({
        sort: false  // Default.
    });
});
```

###### delay
Define the delay (in ms) between the last keyup event and the search action.
```javascript
$(document).ready(function() {
    $(".myList").listpicker({
        delay: 700  // Default.
    });
});
```

##### References

* [Twitter Boostrap](http://twitter.github.io/bootstrap/)
* [Bootstrap input clear button](https://github.com/mahpour/bootstrap-input-clear-button/blob/master/bootstrap.input-clear.js)
* [jQuery](http://api.jquery.com/)
