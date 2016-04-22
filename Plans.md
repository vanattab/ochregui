## Immediate Plans ##

  1. Test, test, and more testing, both for bugs and for testing the usability of the programming interface itself.
  1. Add more to the OchreExt.dll (see below)
  1. Fix and flesh out some of the documentation, especially if there is any outside interest in this project.
  1. Thoroughly test on linux
  1. Add a simple drag and drop mechanism to the core lib
  1. Add more Sample projects, including a skeleton for an inventory system using drag&drop, a character creation skeleton, and, of course, the ultimate RL game with a friendly user interface...

## OchreExt.dll ##

This is where I will add "extended" controls for use with the library.  I figure a good way to test the core lib is to write an extension to it.  Planned controls for this library include:

  1. A spin box allowing a user to enter a numerical value, either by typing in the value or clicking up/down buttons.  The buttons will scroll the value up or down at a definable rate, and the numerical entry itself can be validated by min/max value.
  1. Some type of color picker, and perhaps an small utility application using color pickers to define the GUI color style
  1. A radio button group box
  1. A slider allowing a different method of specifying a numerical value.  I have a pretty good idea of how I want the interface to work, but I have yet to test any of it for feasibility.