# React Sortable Tree Compact Theme

![theme appearance](https://user-images.githubusercontent.com/4413963/32144463-a7de23e0-bcfc-11e7-8054-1a83d561261e.png)

## Features

- You can click anywhere on a node to drag it.
- More compact design, with indentation alone used to represent tree depth.

## Usage

```sh
npm install --save react-sortable-tree-theme-compact
```

```jsx
import React, { Component } from 'react';
import SortableTree from 'react-sortable-tree';
import CompactTheme from 'react-sortable-tree-theme-compact';

export default class Tree extends Component {
  constructor(props) {
    super(props);

    this.state = {
      treeData: [{ title: 'src/', children: [{ title: 'index.js' }] }],
    };
  }

  render() {
    return (
      <div style={{ height: 400 }}>
        <SortableTree
          treeData={this.state.treeData}
          onChange={treeData => this.setState({ treeData })}
          theme={CompactTheme}
        />
      </div>
    );
  }
}
```
