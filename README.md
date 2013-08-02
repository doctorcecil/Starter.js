Starter.js
==========

Start Javascript file when starting a new project

The main aspects of the file are:
-  Automatically adds screen width class to the body on initial load and when window is resized. This allows dimension targeting within selectors. This function ‘DeviceType.Init() is called within ‘Run.Init()’.
-	‘Selectors’, ‘classes’ and ‘values’ listed at the top and can be referenced throughout the file. An example is once a ‘selector’ has been created at the top, it won’t have to be created in a variable again. Same goes for ‘classes’ and ‘values’.
-	‘Resize’ function to keep Initial load and resize functions separate. The resize function is simply called in the ‘Run.Init()’
-	Simple example of calling a function if it is needed on a page. An example would be calling ‘Media.Init()’ if the ‘Image section was present within the HTML.
-	Simply include this file underneath a minified JQuery reference as I use JQuery within this file.

