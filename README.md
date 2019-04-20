# STORYBOOK
Website: https://storybook.js.org

# Step 1: Add dependencies
## Add @storybook/react
Add ``` @storybook/react ``` to your project. To do that, run:
```js
npm install @storybook/react --save-dev
npm install @storybook/addon-info --save-dev
```
## Add react, react-dom, @babel/core, and babel-loader
Make sure that you have ```react```, ```react-dom```, ```@babel/core```, and ```babel-loader``` in your dependencies as well because we list these as a peer dependencies:
```bash
npm install react react-dom --save
npm install babel-loader @babel/core --save-dev
```
# Step 2: Add a npm script
Then add the following NPM script to your `package.json` in order to start the storybook later in this guide:
```bash
{
  "scripts": {
    "storybook": "start-storybook"
  }
}
```
## Step 3: Create the config file
For a basic Storybook configuration, the only thing you need to do is tell Storybook where to find stories.

To do that, create a file at `.storybook/config.js` with the following content:
```bash
import { configure } from '@storybook/react';

function loadStories() {
  require('../stories/index.js');
  // You can require as many stories as you need.
}

configure(loadStories, module);
```
## Step 4: Write your stories
Now create a `../stories/index.js` file, and write your first story like this:
```bash
import React from 'react';
import { storiesOf } from '@storybook/react';
import { Button } from '@storybook/react/demo';

storiesOf('Button', module)
  .add('with text', () => (
    <Button>Hello Button</Button>
  ))
  .add('with emoji', () => (
    <Button><span role="img" aria-label="so cool">😀 😎 👍 💯</span></Button>
  ));  
```
Each story is a single state of your component. In the above case, there are two stories for the demo button component:
```bash
Button
  ├── with text
  └── with emoji
```
## Finally: Run your Storybook
`npm run storybook`
