# ABP-Dex2Jar Plugin
An Eclipse plugin of Dex2Jar.

Original project source from: https://code.google.com/p/dex2jar/

## Building Dex2Jar
Adapted from: https://code.google.com/p/dex2jar/wiki/BuildFromSource

1) `git clone git@github.com:EnSoftCorp/abp-dex2jar.git`

2) `cd abp-dex2jar`

3) `mvn install`

## Building ABP-Dex2Jar

After building Dex2Jar using maven, extract the contents of `/dex-tools/dex2jar-0.0.x.x-SNAPSHOT.zip` to a folder.  In Eclipse select `File` &gt; `New` &gt; `Other...` &gt; `Plug-in Development` &gt; `Plug-in from Existing JAR Archives` &gt; `Next` &gt; `Add External...`.

Select the `.jar` files in the `dex2jar-0.0.x.x-SNAPSHOT/lib` folder and press `Next`.  Enter `com.googlecode.dex2jar` for the Project name.  Enter `com.googlecode.dex2jar` for the Plugin-in ID. Enter the version number followed by `.qualifier` (ie `0.9.16.qualifier`) for the Plug-in version.  Enter `EnSoft Corp.` for the Plug-in vendor.  Press `Finish`.

Edit the plugin manifest and export the following packages `com.googlecode.dex2jar.tools`, `com.googlecode.dex2jar.util`, `com.googlecode.dex2jar.v3` and any others required by your dependent project.  You can get a good idea of what packages to export by looking at the shell scripts included with the compiled JAR files.