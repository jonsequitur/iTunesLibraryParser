iTunesLibraryParser [![Build status](https://ci.appveyor.com/api/projects/status/tsebsc61mqylaejq?svg=true)](https://ci.appveyor.com/project/asciamanna/ituneslibraryparser)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/20f1e8648cc74b158fbbb09528fd9e2e)](https://app.codacy.com/app/asciamanna/iTunesLibraryParser?utm_source=github.com&utm_medium=referral&utm_content=asciamanna/iTunesLibraryParser&utm_campaign=badger)

[![NuGet version](https://img.shields.io/nuget/v/ITunesLibraryParser.svg)](https://www.nuget.org/packages/iTunesLibraryParser/)

===================
The iTunes Library Parser is implemented in C# utilizing LINQ-To-XML (in memory). Given the location of a iTunesMusicLibrary.xml file it parses the PropertyList format, which is defined by the Document Type Declaration (DTD) defined here [http://www.apple.com/DTDs/PropertyList-1.0.dtd](http://www.apple.com/DTDs/PropertyList-1.0.dtd). Currently it returns a collection of tracks and collection of playlists. More features will be added periodically.

## Nuget

The nuget package is [available here](https://www.nuget.org/packages/iTunesLibraryParser/)

## Usage
```
var library = new ITunesLibrary("iTunesLibrary.xml");

var tracks = library.Tracks 
// returns all tracks in the iTunes Library

var playlists = library.Playlists
// returns all playlists in the iTunes Library
```

## Performance Testing
I have tested the parser against a library of 14,500 tracks and 100 playlists. Each request takes less than 900ms to complete.

## Coming Soon
Additional features will be coming soon like filtering tracks by track criteria, returning albums, and returning compilation albums.

## Project Dependencies
NUnit 3.10.1  
Moq 4.8.2

## Contact
**Anthony Sciamanna**
<br/>
**Web:** [http://www.anthonysciamanna.com](http://www.anthonysciamanna.com)  
**Twitter:** [@asciamanna](http://www.twitter.com/asciamanna)
