# Genie
Helpful reference commands and cheatsheets

* [React](#react)
* [Redux](#redux)
* [NPM](#npm)
* [Git](#git)
* [Markdown](#markdown)

## React 

[React Cheatsheet](https://devhints.io/react)

[React Router Scroll to Top on Navigation](https://github.com/ReactTraining/react-router/blob/master/packages/react-router-dom/docs/guides/scroll-restoration.md)

```js
import React, { Component } from 'react';
import { withRouter } from 'react-router-dom';

class ScrollTopOnNavigation extends Component {
  componentDidUpdate(prevProps) {
    if (this.props.location !== prevProps.location) {
      window.scrollTo(0, 0);
    }
  }

  render() {
    return this.props.children;
  }
}

export default withRouter(ScrollTopOnNavigation);
``` 


## Redux 

[Redux Cheatsheet](https://devhints.io/redux)

## NPM

Show globally installed NPM packages

```shell
npm ls -g --depth=0
```

## Git

* Revert back to the last commit, removing any local changes: `git reset --hard HEAD`
* Unstage a staged file: `git reset <FILE>`
* Revert a file to last committed local version: `git checkout -- <FILE>`

## Markdown

[Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
