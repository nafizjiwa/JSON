# JSON use and functionality

JSON is used to exchange data to/from a web server.</BR>

Data sent to a web server has to be a string.</BR>

Convert JavaScript datatype (ex. object) into a string with JSON.stringify().

    const javascriptObject = {name: "John", age: 30, city: "New York"};
    const myJSON = JSON.stringify(javascriptObject);

Create a JSON string below from above JavaScript object.

    {"name":"John","age":30,"city":"New York"}
STORING AN OBJECT AS TEXT</BR>

### Stringify a Function
In JSON, functions are `not allowed` as object values.

The JSON.stringify() function will remove any functions from a JavaScript object, both the key and the value:</BR>
So to avoid this occuring convert functions into strings   FIRST with `.toString()`</BR>

      const obj = {name: "John", age: function () {return 30;}, city: "New York"};</BR>
      obj.age = obj.age.toString();         
      const myJSON = JSON.stringify(obj);

      RESULTS:
      {"name":"John","age":"function () {return 30;}","city":"New York"}

      RESULT WITHOUT .toString():
      {"name":"John","city":"New York"}

      
