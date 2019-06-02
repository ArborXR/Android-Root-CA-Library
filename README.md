An Android module (`.aar`) that can be added to any project to enable user-installed trusted root certificates in debuggable builds.

This is useful when inspecting traffic using [Charles Proxy](https://www.charlesproxy.com/) or [Fiddler](https://www.telerik.com/fiddler), 
as these tools [require a self-signed root certificate](https://www.telerik.com/blogs/how-to-capture-android-traffic-with-fiddler) to 
be installed on the device to enable them to decrypt traffic, man-in-the-middle style.  As of Android N, user-installed certificates like
this are not respected by applications except the system web browser, unless the application explicitly opts-in to it.

This module does exactly that, by providing a `network-security-config` resource that enables user-installed certificates _only in
debuggable builds_.

## Using with Unity

Simply add the `DebuggableRootCertificates.aar` release file anywhere in the `Assets` folder.  It should work with Unity 2018.x and later.

## Using with other projects

Use the appropriate module-linking functionality of your build system to add the `DebuggableRootCertificates.aar` file.  Alternatively,
just have a look at the `AndroidManifest.xml` and `network_security_config.xml` file in this project and add them directly to your own.
