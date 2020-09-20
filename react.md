# React

## Portals

Render outside of the root element.

```jsx
const RenderPortal = ({domNode,children}){
    if( ! domNode ){
        return null
    }
    return ReactDOM.createPortal(
        this.props.children,
        domNode
    );
}

```

## Testing

- https://codesandbox.io/s/github/kentcdodds/react-testing-library-examples
