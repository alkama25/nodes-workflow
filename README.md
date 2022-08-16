# nodes-workflow

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

### Steps to build

Clone the repository from Github link provided.
Run npm run serve to run the project locally.

### Tech Stack 

Vue 2
JavaScript
SCSS

### Description

For detailed documentation please visit - https://v2.vuejs.org/

The structure of the project is:

    ## Assets
    1. Scss folder that has variables and scss file imported in App.vue

    ## Components
    1. NodesPanel having search input that renders all the nodes based on search results
    2. SingleNode component render nodes in the search results.
    3. WorkflowPanel displays the workflow created by searching and adding nodes from the list.

    ## Services
    1. nodeListService.js - contains the mocked response for node list.
