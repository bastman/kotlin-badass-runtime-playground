# kotlin-badass-runtime-playground
how to package / distribute java applications?

Let's explore the badass-runtime plugin. 
create custom runtime images for non-modular applications in javaland.

see:
- https://openjdk.java.net/jeps/343
- https://badass-runtime-plugin.beryx.org/releases/latest/
- https://github.com/beryx-gist/badass-runtime-example
- https://github.com/tonsV2/jibcmd
Note: installers can be created as well (task: jpackageImage, requires java 14+)

```
"The jpackage tool packages a Java application into a platform-specific package that includes all of the necessary dependencies. The application may be provided as a collection of ordinary JAR files or as a collection of modules. The supported platform-specific package formats are:
 
 Linux: deb and rpm
 macOS: pkg and dmg
 Windows: msi and exe
"
```

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
