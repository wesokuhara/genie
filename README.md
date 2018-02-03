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

Often you will need to scroll to the top of a long page, that when navigated to stays scrolled down. Make sure to wrap it in `withRouter` to give it access to the Router's props.
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
Then render it at the top of your app, but below the Router:

```js
const App = () => (
  <BrowserRouter>
    <ScrollTopOnNavigation>
      ...
    </ScrollTopOnNavigation>
  </BrowserRouter>
);
```

## Redux 

[Redux Cheatsheet](https://devhints.io/redux)

[10 Tips for Better Redux Architecture](https://medium.com/javascript-scene/10-tips-for-better-redux-architecture-69250425af44)

## NPM

Show globally installed NPM packages: `npm ls -g --depth=0`

## Git

* Revert back to the last commit, removing any local changes: `git reset --hard HEAD`
* Undo latest commit, keeping any local changes: `git reset HEAD^`
* Edit the latest local commit message: `git commit --amend`
* Unstage a staged file: `git reset <FILE>`
* Revert a file to last committed local version: `git checkout -- <FILE>`

## Markdown

[Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
