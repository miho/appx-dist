# appx-dist

[ ![Download](https://api.bintray.com/packages/miho/UG/ugshell-dist/images/download.svg) ](https://bintray.com/miho/Appx/appx-dist/_latestVersion)

Bintray distribution infrastructure for the appx utility by Facebook

## How to Build appx-dist

### Requirements

- Java >= 1.8
- Internet connection (dependencies are downloaded automatically)
- IDE: [Gradle](http://www.gradle.org/) Plugin (not necessary for command line usage)
- local appx executable that shall be added to the distribution

### IDE

Open the `appx-dist` [Gradle](http://www.gradle.org/) project in your favourite IDE (tested with NetBeans 8.2) and build it
by calling the `assemble` task.

### Command Line

Navigate to the [Gradle](http://www.gradle.org/) project (e.g., `path/to/appx-dist`) and enter the following command

#### Bash (Linux/OS X/Cygwin/other Unix-like shell)

    sh gradlew assemble
    
#### Windows (CMD)

    gradlew assemble
    
### Distribution Layout

Distributions layout looks as follows:
```
.
└── appx
    └── bin
        └── appx[.exe]

```
Distributions are are packaged as `appx.zip`. The locations for distributions are:
```
.
└── src
    └── main
        └── resources
            └── eu
                └── mihosoft
                    └── vappx
                        └── appxdist
                            ├── linux
                            │   |── x64
                            │   |   └── appx.zip
                            |   └── x86
                            │       └── appx.zip
                            ├── osx
                            │   └── appx.zip
                            └── windows
                                |── x64
                                |   └── appx.zip
                                └── x86
                                    └── appx.zip
```
