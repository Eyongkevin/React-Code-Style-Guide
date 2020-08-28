# Adipster React Code Style Guide 

As a team, we need to make sure our code is easy to read, understand, and modify. To achieve that, we put in place this guide which should be followed strictly.

>**NB**: This guide is to help new developers understand the React code style and best practices we adopt here at Adipster(**Web-Dev Team**).

## Table of contents

1. Bacis Rules
    - [Import](#import)
    - Naming
    - Alignment
    - Declaration
    - Initialization
    - Spacing
    - [Commenting](#commenting)
    - Tags
    - Methods
    - Props
    - Parentheses
    - Lines
2. Structure & Design Pattens
    - Class-Based Components
    - Functional Components

3. CSS Format

4. Concepts & Principles
    - Single Responsibility 
    - Command-query seperation
    - Computation-Presentation seperation
    - Loose Coupling
    - High Cohesion




### 1. Basic Rules
These are basic rules that shouldn't be neglated. tiny mistakes can pill up to become hard to maintain.

#### Import
- Extenal and internal imports should be seperated by a double space. Starting with extenal imports. 

**BAD**
```
import React, { Component, Fragment } from 'react'; // external
import DraggableDialog from './DraggableDialog'     // internal
import PropTypes from 'prop-types';                 // external
```
**GOOD**
```
import React, { Component, Fragment } from 'react'; // external
import PropTypes from 'prop-types';                 // external
....
                       //double space

import DraggableDialog from './DraggableDialog'     // internal
...
```
- On name conflict, rename on import

**BAD**
```
import NewsContainer from '...'
```
**GOOD**
```
import NewsContainer as News from '...'
```

### Naming

### Alignment
### Declaration
### Initialization
### Spacing
### Commenting
Use comments to explain code.
    - What is the overall purpose of the component(Top of the file)
    - Use block comment at the top of all methods/functions
    - Use inline-comments inside a method/function
Bellow is a small subset of the available options from JSDoc we deem important and usefull in our case.

- [@async](https://jsdoc.app/tags-async.html): Indicate that a function is asynchronous
- [@author](https://jsdoc.app/tags-author.html): I dentify the author of an item.
- [@callback](https://jsdoc.app/tags-callback.html): document a callback function.
- [@classdesc](https://jsdoc.app/tags-classdesc.html): Used to provide a description for a class, separate from the constructor function's description
- [@contructor](https://jsdoc.app/tags-class.html): This function is intended to be called with the "new" keyword
- [@method](https://jsdoc.app/tags-function.html): Describe a function/method
- [@param](https://jsdoc.app/tags-param.html): Document the parameter to a function.
- [@generator](https://jsdoc.app/tags-generator.html): Indicate that a method is a generator method.
- [@yield](https://jsdoc.app/tags-yields.html): Document the value yield by a generator function
- [@readonly](https://jsdoc.app/tags-readonly.html): Meant to be read-only.
- [@return](https://jsdoc.app/tags-returns.html) : Document the return value of a method/function
- [@see](https://jsdoc.app/tags-see.html): Refer to some other documentation for more information
- [@summary](https://jsdoc.app/tags-summary.html): A shorter version of the full description
- [@tutorial](https://jsdoc.app/tags-tutorial.html): Insert a link to an included tutorial file.

*NB:*
- `@description`, `@summary`, `@author` are mandatory
- If function has parameters and returns something, then `@param` and `@return` become mandatrary
- If function is a generator, then `@generator` and `@yield` become mandatory
- A function is iether a contructor or a method. So, should have either `@constructor` or `@method`.
- Parameter(`@param`) type can be any JavaScript build-in types like `string`, `Object`,`Number`... [here](https://jsdoc.app/tags-param.html#:~:text=The%20parameter%20type%20can%20be,the%20documentation%20for%20that%20symbol.)

Let's show these in an example

**GOOD**
- Method
```
/** @method
* @description Takes in a personel data(tile(Mr),name(Jorn)) formate as 'Mr. John' 
* @summary Represents a personel
* @author Kevin
* @see {@link https://jsdoc.app/tags-see.html JSDoc }
* @param {string} title - The title of the personel
* @param {string} name - The name of the personel
*/
function PersonelInfo(title, author) {
    ...
}
```
- Class
```
/** @classdesc
 * Component is described here.
 *
 * @example ./extra.examples.md
 */
export default class Button extends React.Component {
  // ...
}
```

### Tags
### Methods
### Props
### Parentheses
### Lines