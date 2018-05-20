# super-rentals

This README outlines the details of collaborating on this Ember application.
A short introduction of this app could easily go here.
##
Can run in Surge:

`jason_rental.surge.sh`
## Prerequisites

You will need the following things properly installed on your computer.

* [Git](https://git-scm.com/)
* [Node.js](https://nodejs.org/) (with npm)
* [Ember CLI](https://ember-cli.com/)
* [Google Chrome](https://google.com/chrome/)

## Installation

* `git clone <repository-url>` this repository
* `cd super-rentals`
* `npm install`

## Addons
[Check All Addons Here](https://emberobserver.com/)
* `ember install ember-cli-mirage`
> This is to mimic API interaction. 
It proxy HTTP request and return mock HTTP reponse, The data and endpoints 
will be setup here. 
```
Example: 
  In Mirage config.js:
  export default function() {
    this.namespace = '/api';
    this.get('/test', function() {
      return {
         data: [{
          id: 1
          type: test
        }]
      }
    }
  }
    
  In Adapter:
  export default DS.JSONAPIAdapter.extend({
    namespace: 'api'
  });
  
  In Model:
  export default Route.extend({
    model() {
      return this.get('store').findAll('rental');
    }
  });
```
[Check tutorial here](https://guides.emberjs.com/v3.1.0/tutorial/installing-addons/)
 
## Running / Development

* `ember serve`
* Visit your app at [http://localhost:4200](http://localhost:4200).
* Visit your tests at [http://localhost:4200/tests](http://localhost:4200/tests).

### Code Generators

Make use of the many generators for code, try `ember help generate` for more details

### Running Tests

* `ember test`
* `ember test --server`

### Linting

* `npm run lint:js`
* `npm run lint:js -- --fix`

### Building

* `ember build` (development)
* `ember build --environment production` (production)

### Deploying

Specify what it takes to deploy your app.

## Further Reading / Useful Links

* [ember.js](https://emberjs.com/)
* [ember-cli](https://ember-cli.com/)
* Development Browser Extensions
  * [ember inspector for chrome](https://chrome.google.com/webstore/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi)
  * [ember inspector for firefox](https://addons.mozilla.org/en-US/firefox/addon/ember-inspector/)
