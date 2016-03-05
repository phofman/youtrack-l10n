youtrack-l10n
=============

Custom translations for YouTrack


installation
============

If YouTrack is running as a service on Windows translation directory must be specified via JVM startup parameters.
Short info how to locate it could be found [here](https://confluence.jetbrains.com/display/YTD6/Providing+Java+Start+Parameters).

On Windows Server 2012 R2 the procedure is:

 * navigate into `C:\ProgramData\JetBrains\YouTrack\conf\youtrack` folder
 * copy `youtrack.jvmoptions.dist` as `youtrack.jvmoptions` (or create it empty if as everything inside is commented-out)
 * beware of `youtrack.jvmoptions.dist` as it's recreated each time YouTrack service restarts
 * inject extra options into the newly created file, for translation purposes it could be: `-Djetbrains.mps.webr.i18n.custom-translations=<translation_directory>` and directory must point, where `supportedLocales.xml` is placed

example: -Djetbrains.mps.webr.i18n.custom-translations=C:\YouTrack\translations
