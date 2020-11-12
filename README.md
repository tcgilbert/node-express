# node-express

## Node and NPM basics
- make sure you have both node and npm installed 
    - `node -v`
    - `npm -v`

- `npm init` to create a json package 
    - this will let you pick specific details like description and author name
- `npm init -y` will create json with all default values

To run any javascript in the command line type `node index.js`
- index.js is the defualt file name used by npm

In order to use anything that is not in index.js you have to link that via the `require()` function 
___
## Example
the `add` and `minus` functions are declared in the myModule.js file. To run them in index.js you have to include the first line of the following code

```js
const { add, minus } = require("./myModule");

console.log(add(5, 23));

console.log(minus(6, 9));
```

In order for that to work, in `myModule.js`, you have to assign the functions you want to include to the `module.exports` variable 

```js
const beBasic = () => "That's so fetch!";

function add(num1, num2) {
    return num1 + num2;
}

function minus(num1, num2) {
    return num1 - num2;
}

module.exports = {
    beBasic, 
    add, 
    minus
}
```