# meteor-typeahead [![Build Status][buildstatus]][buildstatusurl]

Autocomplete package for meteor powered by twitter typeahead.js

## Usage

Install the package with [Meteorite](https://github.com/oortcloud/meteorite).

```
mrt add typeahead
```

## Examples

You will need to create the HTML input element and supply the appropriate JavaScript helpers to populate the data source.

### HTML

```
<input class="form-control typeahead" name="names" type="text" placeholder="Names" autocomplete="off" spellcheck="off" data-source="{{names}}"/>
```

### Javascript

#### Static Data

```
Template.search.rendered = function(){
  Meteor.typeahead(this.find('.typeahead'));
};

Template.search.helpers({
  'names': function(){
    return JSON.stringify(['Ben', 'Nicholas', 'Murray', 'Sergey', 'Alexander', 'Michael']);
  }
});
```

[buildstatus]: https://drone.io/github.com/sergeyt/meteor-typeahead/status.png
[buildstatusurl]: https://drone.io/github.com/sergeyt/meteor-typeahead/latest
