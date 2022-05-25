# About

This project generates an .so file which realizes the binding between glib and the bluez daemon. It generates the required Classes
to utilizes the gdbus-api via the glib-type system.

# Generation of generated-code.c and .h

The files are automatically generated via the gdbus-codegen(https://www.freedesktop.org/software/gstreamer-sdk/data/docs/latest/gio/gdbus-codegen.html) tool from the given given xml. The  
xml was published by tinyb (https://github.com/intel-iot-devkit/tinyb/tree/master/src).

Die generierten Dateien sind aktuell mit zusätzlichen printfs versehen, um ein Debuggen zu ermöglichen.

# Required dependencies

- GLib as an immediate dependency to communicate via the GDBus-API with the bluetoothd daemon.
  Documentation can be found under https://developer.gnome.org/glib/

## Installation of dependencies
### Ubuntu
```
    apt-get install libglib2.0-dev
```
### Fedora (Not tested yet)
```
    dnf install glib2-devel    
```
# How to build
```
mkdir target
cd target
cmake ..
cmake --build /path/from/root/to/target --verbose
```
