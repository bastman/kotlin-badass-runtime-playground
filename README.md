# kotlin-badass-runtime-playground
how to package / distribute java applications?

Let's explore the badass-runtime plugin. 
create custom runtime images for non-modular applications in javaland.

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

```
# how to distribute image as zip ?
./gradlew runtimeZip
```
```
# how to bundle as MacOS app?
Uses the jpackage tool to create a platform-specific application image.


$ ./gradlew jpackageImage

or 

$ ./gradlew jpackage

creates: build/jpackage/{app}.dmg
```
