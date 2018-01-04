# Polymer App 

##### Prerequisites

Install [polymer-cli](https://github.com/Polymer/polymer-cli):

    npm install -g polymer-cli

##### Initialize project from template

    mkdir my-app
    cd my-app
    polymer init starter-kit

### Start the development server

This command serves the app at `http://localhost:8080` and provides basic URL
routing for the app:

    polymer serve --open


### Build

    polymer build

### Run tests

This command will run
[Web Component Tester](https://github.com/Polymer/web-component-tester) against the
browsers currently installed on your machine.

    polymer test

### Adding a new view

You can extend the app by adding more views that will be demand-loaded
e.g. based on the route, or to progressively render non-critical sections
of the application.  Each new demand-loaded fragment should be added to the
list of `fragments` in the included `polymer.json` file.  This will ensure
those components and their dependencies are added to the list of pre-cached
components (and will have bundles created in the fallback `bundled` build).