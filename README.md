# Jasmine JSX

A version of Jasmine 2.2.0 that works with Adobes' ExtendScript.  ExtendScript is a JavaScript variant that allows you to create and run scripts that extend Adobe's suite of create products.

To use Jasmine JSX:

 * Install Adobe [ExtendScript Toolkit](https://creative.adobe.com/products/estk).
 * Download this project and open the file `specRunner.jsx`.
 * Run the script and watch the spec files in the JavaScript console run.

 ## Adding Jasmine JSX into your project

 Right now I'm using it like a node module (though it isn't really a node module).  I list the git project as a dependency from git...

```
"dependencies": {
    "jasminejsx": "git://github.com/tmaslen/jasminejsx.git#master"
},
```

 Then after `npm install`ing I make a new spec runner JSX file in the root of my project.  I then create a `spec` directory in there too and hook the spec runner file up to this new directory and the jasminejsx module.  The contents of the file looks like this:

```
#include "node_modules/jasminejsx/jasmine/boot.jsx"
#include "spec/example.spec"
runJasmine();
```