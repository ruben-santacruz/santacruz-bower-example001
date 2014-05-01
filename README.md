## Introduction

This simple repo tries to test the following:
- Let's say that I create a package to be used with Bower, as the one created in this sample repo.
- When in an upcoming version (as `0.0.2`) a file of the package is removed as we did here with `doc2.html` (because we don't need it anymore), what happens to a project that uses version `0.0.1` of the package and runs `bower update`? Do the old file stay in the `bower_components` folder? Let's check it!

## Usage
This package is registered with Bower, so to perform the test we can install it via Bower:
- Create an empty folder and run `bower init` to create a `bower.json` scaffold.
- Install the first version (`0.0.1`), that is: the one that uses `doc2.html`. `bower install santacruz-bower-example001#0.0.1 --save`
- Have a look at the webpage and the files installed.
- Now we want to update to version `0.0.2` that doesn't use `doc2.html`: edit `bower.json` to use version `0.0.2`:
```JSON
{
  ...
  "dependencies": {
    "santacruz-bower-example-001": "0.0.2"
  }
}

```
- Run `bower update`
- See the results.

## Conclusion

Bower automatically cleaned up the `bower_components` folder, this is: it deleted the `doc2.html` when we updated to version `0.0.2`.
________
*Tested with Bower v1.3.2* 


