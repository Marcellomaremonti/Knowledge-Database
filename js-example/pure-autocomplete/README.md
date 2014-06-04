Autocomplete
===

Completely Free, without jQuery or any plugin.

Focus on `tagsinput` and `autocomplete`, but *small amount* and *known data*

Requirement
===

Modern Browser is required

Open up a `http://localhost` or just `file://` server

>  node web-server.js

How to use
===
```html
<!-- include autocomplete form css -->
<link rel="stylesheet" href="autocomplete.css"/>
<!-- include autocomplete js prototype -->
<script src="autocomplete.js"></script>
<!-- initial autocomplete Element -->
<script>
    var auto = new AutoComplete({
        /* options */
    });
    auto.setList([/* Array data */])
</script>

<!-- else add the following html -->
<div class="form">
    <div class="form-wrapper">
        <input id="form-input" type="text" onkeyup="auto.getList(this)" placeholder="Type your keywords"/>
    </div>
    <ul id="form-autocomplete">
    </ul>
</div>
```

API
===
Constructor AutoComplete
```javascript
var auto = new AutoComplete({
    inputElementId: '', // input text Element ID
    listElementId: '', // list view Element ID, usually <ul>
    formList: [], // [Array] You can initial list here, default is null Array
    selectListCB: callback, // callback function when select a list item,
    deleteCB: callback, // callback function when delete a item
});
```
AutoComplete.setList

>  Setup formList manually

```javascript
auto.setList([ /* Array List here */]);
```

Constructor.getList

> Show the list for user to select

```javascript
auto.geList(value); // value is a input value
```
Constructor.showList

> Show the list (display block)

Constructor.hideList

> Hide the list (display none)

Constructor.getFormList

> return the formList selected

Screenshot
===
![screen shot 2014-06-05 at 1 06 09 am](https://cloud.githubusercontent.com/assets/2560096/3176985/be3d75da-ec0a-11e3-8125-13a4b68b2630.png)

![screen shot 2014-06-05 at 1 06 31 am](https://cloud.githubusercontent.com/assets/2560096/3176975/ac6c2a72-ec0a-11e3-86cd-f3cfa4b0154f.png)

![screen shot 2014-06-05 at 1 06 35 am](https://cloud.githubusercontent.com/assets/2560096/3176978/b02340ba-ec0a-11e3-8844-4f62b27da4de.png)