# kotlin-badass-runtime-playground
explore the badass-runtime plugin. create custom runtime images for non-modular applications in javaland.

see:
- https://badass-runtime-plugin.beryx.org/releases/latest/
- https://github.com/beryx-gist/badass-runtime-example

Note: installers can be created as well (task: jpackageImage, requires java 14+)

```

# use java sdk from .sdkman
sdk env

# build image
./gradlew runtime

# run
cd build/image/bin
./kotlin-badass-runtime-playground

or simply:

./build/image/bin/kotlin-badass-runtime-playground


# suggest modules
./gradlew suggestModules
```
