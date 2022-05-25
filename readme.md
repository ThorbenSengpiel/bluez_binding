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
