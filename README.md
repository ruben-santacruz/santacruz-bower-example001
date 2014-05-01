This simple repo tries to test the following:
- Let's say that I create a package to be used with Bower, as the one created in this sample repo.
- When in an upcoming version (let's say 0.0.2) a file of the package is removed as we did here with doc2.html (because we don't need it anymore), what happens to a project that uses v.0.0.1 of the package and runs `bower update`? Do the old file stay in the bower_components folder? Let's check it!

