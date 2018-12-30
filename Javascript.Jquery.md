#### Basic
* change or remove attribute 
```javascript
  //remove attribute in parent element
  $("input[name='category']:checked").closest("label").removeClass("active");
  //change attribute
  $("input[name='category']:checked").prop('checked', false);
```
