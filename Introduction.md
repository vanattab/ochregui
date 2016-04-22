# What #

OchreGui is a small set of class libraries written in C# for use with the fine Doryen Library for creating rogue-like games.  OchreGui aims to provide a convenient solution to easily and quickly implement a user interface for a roguelike game or application.  Currently, there are 3 libraries available:

  * OchreGui.dll - the core library, contains all of the classes having to do with the user interface
  * Utility.dll - a small utility library used in combination with OchreGui.  Offers data types such as Point, Rect, Size, Dice, and some others.
  * OchreExt.dll - a WIP for an extended control library.  See [Plans](Plans.md) for more.

See the ClassOverview page for more details.

Also, I try to keep the compiled help file (OchreGui.chm) up-to-date, and it can be found here: http://code.google.com/p/ochregui/source/browse/trunk/%20ochregui/OchreGui.chm

NOTE: In order to view OchreGui.chm on Windows, the help file must be on a local disk.  Also, you may need to right-click on the file, choose properties, and click on "Unblock" in the general tab.

## Design Philosophy ##

A couple quick notes:
  * I prefer immutable data types in C#, so you find many here (particularly in the Utility library).  They are, at least, _weakly_ immutable, since C# does not have (IMO) good support for such at the moment.
  * I try to be as conservative as possible with access modifiers for methods and properties to simplify the programming interface.  However, until I actually use the library for something significant, I am not sure how robust and/or usable the interface actually is, and am assuming that certain design decisions will need to be changed.
  * None of this has been optimized, and I see no need to try and optimize until I feel there is a bottleneck somewhere.  As such, I throw around data, box/unbox values, take brute force approaches, etc. in order to simplify the code.
  * I assume that the C# developer is working in a fully featured IDE with intellisense and code completion - therefore, I do not go out of my way to abbreviate terms.  In short, I strive for clarity over brevity for type, method, and property names.

# Why #

In the process of tinkering with libtcod over the years, I seem to always get hung up when trying to add some sort of user interface to a game.  I grew tired of the mess of UI code laying around, and decided to bundle it together into a cohesive unit.  I also decided I may as well document some of it and release it as open source in case anyone else has similar goals.


# How #

Adding the library to an existing libtcod.net project _should_ be as simple as adding Utility.dll and OchreGui.dll as references.  In order to run the binaries, you must have all the proper libtcod dependencies for your OS, as well as have the necessary .net or mono installed to run .NET 3.5 applications.

This library currently uses version 1.5.1 of libtcod.net.