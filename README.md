# JFx_Gradle_MusicPlayer
A Simple JAVAFX Music Player using javafx media package.
Builds and runs fine on Windows Platform.
Running the same project on linux system throws exception.
"Caused by: com.sun.media.jfxmedia.MediaException: Could not create player!".
Program uses simple java io to perform read and write of the playlist.
Uses XML file ("playlistXMLSource") to read and write the path of the music files and playlist name.
Program reads XML source file when Controller is initialized. If not found then creates a new one.
Reading metadata of the music tracks is done on different Thread using Platform.runlater().
Sometimes metadata is not retrieved when a large number of files are imported to the playlist.
I Guess there is a bug in the implementation of the importing of files into the playlist.
