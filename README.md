# html-attribute-to-react

Get the React equivalent of any native HTML attribute.

## Why?
There are a number of attributes that work differently between React and HTML. For example:
* In React, most DOM properties and attributes should be camelCased
* `class` in HTML becomes `className` in React
* `aria-*` and `data-*` attributes stay the same

If you need to programmatically convert HTML to React, this package handles the attribute conversion for you.

## Installation
```
yarn add html-attribute-to-react --save
```

## Usage
```js
import htmlAttributeToReact from 'html-attribute-to-react';

htmlAttributeToReact('class');
// returns 'className'

htmlAttributeToReact('tabindex');
// returns 'tabIndex'

htmlAttributeToReact('aria-label');
// returns 'aria-label'

htmlAttributeToReact('some-custom-attribute');
// returns 'some-custom-attribute'
```

To get the full attribute map:
```js
import { attributes } from 'html-attribute-to-react';

attributes['class'];
// `className`
```