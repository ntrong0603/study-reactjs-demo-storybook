# STORYBOOK
Website: https://storybook.js.org

# Step 1:
## Add @storybook/react
Add ``` @storybook/react ``` to your project. To do that, run:
```bash
npm install @storybook/react --save-dev
npm install @storybook/addon-info --save-dev
```
## Add react, react-dom, @babel/core, and babel-loader
Make sure that you have ```react```, ```react-dom```, ```@babel/core```, and ```babel-loader``` in your dependencies as well because we list these as a peer dependencies:
```bash
npm install react react-dom --save
npm install babel-loader @babel/core --save-dev
```
# Step 2:
Then add the following NPM script to your `package.json` in order to start the storybook later in this guide:
```bash
{
  "scripts": {
    "storybook": "start-storybook"
  }
}
```
