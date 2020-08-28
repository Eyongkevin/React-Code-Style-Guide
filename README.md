# Adipster React Code Style Guide 

As a team, we need to make sure our code is easy to read, understand, and modify. To achieve that, we put in place this guide which should be followed strictly.

>**NB**: This guide is to help new developers understand the React code style and best practices we adopt here at Adipster(**Web-Dev Team**).

## Table of contents

1. Bacis Rules
    - Import
    - Naming
    - Alignment
    - Declaration
    - Initialization
    - Spacing
    - Commenting
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
### Tags
### Methods
### Props
### Parentheses
### Lines