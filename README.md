# Example app testing an opensource component

## Installation

```
git clone git@github.com:jakewies/test-opensource-component.git

yarn

yarn build
```

## Link package to a local test environment

I'm testing out my component in a separate local project. I'm doing this using `yarn link`.

In this project:

```
yarn link
```

Navigate to local test project where you can consume this example:

```
yarn link test-opensource-component
```

Then you can `import` the component using:

```
import TestComponent from 'test-opensource-component`
```

On initial render of the page, I'm receiving an error that looks like this:

```
Warning: Failed context type: Invalid context `__styled-components-stylesheet__` supplied to `Component`.
    in styled.h1 (at grid.js?entry:13)
    in main
    in grid__Main (at grid.js?entry:12)
    in div (at Page.js:8)
    in Page (at grid.js?entry:11)
    in App (at _document.js?entry:9)
    in StyleSheetManager
    in Unknown
    in AppContainer
    in Container
    in div
    in App
```

Everything still works, and I'm assuming this is because it's a warning. I'm just not sure how to resolve or why it's happening in the first place.
