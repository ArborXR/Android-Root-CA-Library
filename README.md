An Android module (`.aar`) that can be added to any project to enable user-installed trusted root certificates.

## Prebuilt release

See the [Releases](https://github.com/ArborXR/Android-Root-CA-Library/releases) page to download a prebuilt .aar file.

## Using with Unity

Simply add the `RootCertificateSecurityConfig.aar` release file anywhere in the `Assets` folder.  It should work with Unity 2018.x and later.

## Using with other projects

Use the appropriate module-linking functionality of your build system to add the `RootCertificateSecurityConfig.aar` file, or import this
prjoect into your Gradle system.  Alternatively,  just have a look at the `AndroidManifest.xml` and `network_security_config.xml` file
in this project and add them directly to your own.
