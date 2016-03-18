youtrack-l10n
=============

Custom translations for YouTrack.
Checkout the [official guide](https://youtrack-support.jetbrains.com/hc/en-us/articles/206545789-Translating-YouTrack-UI) before starting updating any file in this repository.


installation
============

If YouTrack 6.5+ is running as a service on Windows translation directory must be specified via JVM startup parameters.
Short info how to locate it could be found [here](https://confluence.jetbrains.com/display/YTD6/Providing+Java+Start+Parameters).

On Windows Server 2012 R2 the procedure is:

 * navigate into `C:\ProgramData\JetBrains\YouTrack\conf\youtrack` folder
 * copy `youtrack.jvmoptions.dist` as `youtrack.jvmoptions` (or create it empty if as everything inside is commented-out)
 * beware editing of `youtrack.jvmoptions.dist` as it's recreated each time YouTrack service restarts
 * inject extra options into the newly created file, for translation purposes it could be: `-Djetbrains.mps.webr.i18n.custom-translations=<translation_directory>` and directory must point, where `supportedLocales.xml` is placed

example: `-Djetbrains.mps.webr.i18n.custom-translations=C:\YouTrack\translations`


how to
======

Detailed guide about meaning of the files and fields is provided [here](https://confluence.jetbrains.com/display/YTD65/Translating+YouTrack+UI).
