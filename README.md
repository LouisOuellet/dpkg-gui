# DPKG-GUI

It's not always easy for new linux users to get used to the command line. DPKG-GUI offers a simple GUI to install DEB packages. The GUI is provided using yad and polkit. Both of which can be installed by installing DPKG-GUI.

## Requirements

All package required can easily be install by running ```./dpkg-gui -i```.

## Usage

```bash
./dpkg-gui -?
Invalid option: ?

Usage: dpkg-gui [options]

Options:

-v                     => Enable Debug Mode
                          Input commands sent are stored in log/dpkg-gui/
-i                     => Install Script as Binary
-r                     => Remove Binary
```

## How To
### Update the script

First update the local repository using:
```bash
git pull origin main
```

And update the bin file using

```bash
./dpkg-gui -r && ./dpkg-gui -i
```
### Add a desktop shortcut

From the repository directory execute:
```bash
cp DEB\ Installer.desktop ~/Desktop/DEB\ Installer.desktop
```

Then you can edit the parameters (```Exec=dpkg-gui```) of the command using nano.

## Changlelog

 * [2020-10-07] - Created a basic installer script using yad and polkit
 * [2020-10-07] - Added a desktop file to copy on the client's Desktop
