### angular-global  

#### Why?
angular-global is probably a bad idea and you probably shouldn't use it. This package exposes all of your modules to the global scope. Allowing you ignore angulars tedious DI in favor of browserify.

#### Installation

```$ npm install ```

Then in your app you can do this

```
// example service
require('angular-global').app
  .service('exampleService', [function () {}])
```

```
// main file
require('path/to/exampleService')

require('angular').module('myApp', [
  require('angular-global').name
])
```
