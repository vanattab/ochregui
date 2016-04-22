OchreGui is a collection of class libraries built on top of Libtcod (the "Doryen Library http://doryen.eptalys.net/libtcod/) to aid in adding "graphical" user interfaces to a roguelike game.

These libraries are built in C# using .Net 3.5.

The core library currently has the following features:
  * User input polling and messaging for the mouse and keyboard.  Handle these messages by either subscribing to events or deriving a custom class from one of the various components.
  * An application/window framework handling libtcod initialization, messaging, and the main game loop.  Override base class methods to add implementation specific startup, logic update, drawing, and cleanup code.
  * Various ready-to-use controls that can be added to the window (buttons, check boxes, text entry boxes, list boxes, menus, and panels are currently provided by the core library).
  * All of the controls/components/windows are built to be subclassed to provide custom behavior.
  * Scheduling and timing built in to the design - with a single line of code set up a method to be called every N milliseconds, useful for animation.
  * The appearance of controls can be changed in various ways, from simply overriding the default colors used by the framework to complete custom handling of the drawing.
  * Tooltips
  * and more...
  * and more to come (hopefully)...

What this library does not have (compared to other fully featured GUI libraries):
  * Recursively defined controls (controls cannot be added to other controls - only the Window acts as a control container)
    * However, controls can be created/controlled by other other controls and by a Manager object
  * Movable and resizable controls, multiple windows, modal windows, dialog boxes, and other advanced user interface features
    * However, controls can be removed/added to a window at any time, simulating dynamic behavior; and the Window can be changed at any time (the Demo project does this for the various pages)
  * Tons of (correct) documentation
    * However, this is at least _some_ documentation in both the source files (so it works with intellisense) and as a separate compiled help (.chm) file
  * Graphics ;)


**Notes:**
  * You will need the usual dependencies of libtcod in a system path or in the same directory as the executable in order to run the demo and samples.
  * I _think_ this will work under linux, but I have not tested this.
  * This library is currently using version 1.5.1 of libtcod.net

THIS IS AN "ALPHA" VERSION - there are certainly bugs and poorly optimized code present in here somewhere.  Also, the interface of the API may undergo changes as testing continues.

Screenshot:

<img src='http://img294.imageshack.us/img294/8854/screenshothp.png' height='50%' width='50%' />


<img src='http://img44.imageshack.us/img44/9921/screen2mw.png' height='50%' width='50%'>