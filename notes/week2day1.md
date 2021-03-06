# Tkinter and XML

## Tkinter - event driven GUI Interface
Even driven programming is based on the user
* Callbacks, event handlers


### Main Functions

``` python
if __name__ == '__main__:
    main()
```

### Window
* Base level GUI

import tkinter
win = tkinter.Tk()

### Tkinter (revisited)
Python Wrapper
* Python library wrapped around TK (written in C)
GUI = Graphical User Interace
Tkinter = TK interface

*Event driven* meaning code response to events that occurs in the programaround
You can't handle events outside the program

GUI Programs are composed of widgets
* Widgets are any GUI Objects
    * Frames
    * Buttons
    * Text Fields
    * Canvas
    * Labels
bar = tkinter.Menu(root)



### Layout Functions
Called on widgets

frame.pack()
* putting widgets into a window (parent widget) is called **layout**

Layout Manager handles
* Pack() - order or pack
* grid() - coordinate system
* place() - specific placement

## XML
Extensible Markup Language

* Meta language for data description. Backwards compatible
```XML
<GraphicsCommands>
<Command color = '#000000'>BeginFill</Command>

<MyTagName></MyTagName>
```

XML has a top level tag with children nodes
```XML
<GraphicsCommand>
    <Command></Command>
    <Command></Command>
</GraphicsCommand>
```
### Reading XML
import xml.dom.minidom
* XML
    * dom.py (module)
        * minidom (function)


### Code to extract commands
```XML
xmldoc = xml.doc.minidom("circle-example.xml")
graphicsCommands = xmldoc.getElementsByTagName("GraphicsCommands")[0]
```





    
