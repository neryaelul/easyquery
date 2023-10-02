# easyquery
## UI for Make your SQL Query with JS  

![easyquery gif](https://github.com/neryaelul/EasyQuery/blob/7d7c96551df57314e438552d381d29eef1d7b45c/assets/eq.gif?raw=true)
edit this config.js file to build your template
table_name - Name of your table,
condition_fields - Using to make a condition
related_field - The field to connect to another table 
related_table_to - The other table name

related_field_to - The field name to another table connected to
```
const db = [
  {
    table_name: "Customers", 
    condition_fields:["FirstName","LastName","Email"]
  }, {
    table_name: "Orders", 
    condition_fields:["OrderNumber","Date"],
    related_field: "CustomerId",
    related_table_to:"Customers",
    related_field_to: "Id"
  }
];
```
## you can add more like this:
```
const db = [
  {
    table_name: "Customers", 
    condition_fields:["FirstName","LastName","Email"]
  }, {
    table_name: "Orders", 
    condition_fields:["OrderNumber","Date"],
    related_field: "CustomerId",
    related_table_to:"Customers",
    related_field_to: "Id"
  }, {
    table_name: "OrdersProducts", 
    condition_fields:["Name","Price"],
    related_field: "OrderId",
    related_table_to:"Orders",
    related_field_to: "Id"
  }
];
```
