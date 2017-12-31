# trans-Forms
A dashboard generator for fast forms creation and tables, it's allow user to take all form data and save it in structure and make operations to it before send it to server.

## Why
I had a problem in my company **ERP** system, each time system create invoice, systen send it to server, each time user want check the invoices it request from server, **So** i got an idea why each time i want to create invoice i should send it to server, why not to make push-commit *like github* i create many invoices and save in a data structure, when i get many of it, i will push it to server.

That's will lower the server requests especially when many works in system that have to push a lot of requests to server.

# Installation
```html
<script src="../Source/Forms.js"></script>
```

```js
forms = new Forms(meta-data, structure);
```
# Usage
```js
forms = new Forms({ //  MetaData
                makeForm: [true, 'form', '', 'POST'],
                makeTable: [true, 'table'],
                allowCRUD: true,
                xmlRequese: []
            }, {    //  Structure 
                id: {type: 'number', allowInput: false, attr: 'auto-increment'},
                name: {type: 'text', placeholder: 'Enter Your Name', allowInput: true, default: 'No Name', allowNulls:true, label: 'Name', small: 'the name you will use will appeare in your profile.'},
                age: {type: 'number', placeholder: 'Enter Your Age', allowInput: true, allowNulls: false, label: 'Age', small: 'Your age will be used for occasions'},
                email: {type: 'email', placeholder: 'Enter Your Email', allowInput: true, allowNulls: false, label: 'Email', small: 'We\'ll never share your email with anyone else.'}
            });

forms.Generate({Debug: true});

forms.RunFlow();
```
# API Reference

## Forms
this is the constructor for the class, holding the metadata and the structure for the form and table components.

### MetaData Object
the metadata object hold all properties that users define.
* **makeForm** key contains the properties of generating form for a given structure.
  * first element of the array if `true` it's allow to make a form / `false` will not generate form for given structure.
  * second element is the `id` for the form generation.
  * third element is the form `action`.
  * forth element is the method of form `POST` or `GET`.
* **makeTable** key contains the properties of generating tables for a given structure.
  * first element of the array if `true` it's allow to make a table / `false` will not generate table.
* **allowCRUD** key if `true` it allow update, delete to table
  * Still under development
* **xmlRequest** key contains all properties for xml request of table.
  * Still under development
```js
//  MetaData
{ 
    makeForm: [true, 'form', '', 'POST'],
    makeTable: [true, 'table'],
    allowCRUD: true,
    xmlRequest: []
}
```
### Structure Object
## SetKeys
## Generate
## RunFlow
## Insert
## Submit
## HoverInput
## InsertIntoTable

# Contributing
Contributions are `110%` welcome! That's a lot!
Please file issues for any bugs you find or features you'd like to see. And if you're up for it, send in a pull request.

# Support
Need a hand with something? Send me an email to `hishamelamir001@gmail.com` and i'll get back to you right away!
