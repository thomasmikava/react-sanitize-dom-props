# React Sanitize DOM Props

This package helps to remove extra properties from object and leave only ones that are valid for passing to dom.

### Usage

```js
import { pickHTMLProps } from "react-sanitize-dom-props";
const props = {
    onClick: () => {},
    className: "container",
    foo: "bar"
}

const sanitizedPorps = pickHTMLProps(props, /* strict */ false);
/* {
    onClick: () => {},
    className: "container",
} */
```


```js
import { isValidHTMLProp } from "react-sanitize-dom-props";

isValidHTMLProp("onClick" /* strict */ false); // true
isValidHTMLProp("onClick" /* strict */ true); // true
isValidHTMLProp("onclick" /* strict */ false); // true
isValidHTMLProp("onclick" /* strict */ true); // false
```
