# bs-reactstrap
This is Bucklescript bindings for [Reactstrap](https://reactstrap.github.io/). Currently they are autogenerated based on propTypes. Everything complex (basically not `string` or `bool`) is just type variable.

# Install
```
yarn add bs-reactstrap
```

# Setup
Add bs-reactstrap to bs-depenencies in your bs-config. bs!
```js
{
  /* ... */
  "bs-dependencies": [
    "bs-reactstrap"
  ],
  /* ... */
}
```

# Usage Example
```re
open BsReactstrap;

let component = ReasonReact.statelessComponent("SomeComponent");

let make = (~onChange, _children) => {
  ...component,

  render: _self => {
    <Button color="primary" size="lg" onClick=(_e => Js.log("Hi!"))>
      Hello
    </Button>
  }
};
```

Check [Reactstrap documentation](https://reactstrap.github.io/components/) for available props.
