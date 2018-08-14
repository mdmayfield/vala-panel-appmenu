# Additional Dependencies

On Ubuntu MATE 18.04, in addition to the other build-essential type stuff I already had, I needed to install:

gobject-introspection libbamf3-dev libdbus-glib-1-dev libffi-dev libgirepository1.0-dev libpeas-dev libstartup-notification0-dev libvala-0.40-0 libwnck-3-dev libwnck-common libwnck22 libxres-dev valac valac-0.40-vapi

# Install from fresh 18.04.1

(Unverified - TODO)
```
sudo apt install gobject-introspection libbamf3-dev libdbus-glib-1-dev libffi-dev libgirepository1.0-dev libpeas-dev libstartup-notification0-dev libvala-0.40-0 libwnck-3-dev libwnck-common libwnck22 libxres-dev valac valac-0.40-vapi git build-essential cmake
git clone https://github.com/rilian-la-te/vala-panel-appmenu.git
cd vala-panel-appmenu/
mkdir build
cd build
git submodule init && git submodule update
cmake -DENABLE_MATE=ON -DENABLE_XFCE=OFF -DENABLE_BUDGIE=OFF -DENABLE_VALAPANEL=OFF -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=RelWithDebInfo ..
sudo make install
```

Didn't work? Installing also libdbusmenu-glib-dev libgtk2.0-dev libmate-panel-applet-dev


```
sudo apt install budgie-core-dev build-essential cmake exo-utils gobject-introspection gir1.2-budgie-1.0 git libbamf3-dev libbudgie-plugin0 libbudgietheme0 libdbus-glib-1-dev libexo-1-0 libexo-2-0 libexo-common libexo-helpers libffi-dev libgarcon-1-0 libgarcon-common libgirepository1.0-dev libgtk2.0-dev libmate-panel-applet-dev libpeas-dev libraven0 libstartup-notification0-dev libvala-0.40-0 libvalapanel-dev libvalapanel0 libwnck-3-dev libwnck-common libwnck22 libxfce4panel-2.0-4 libxfce4panel-2.0-dev libxfce4ui-1-0 libxfce4ui-2-0 libxfce4ui-common libxfce4util-common libxfce4util-dev libxfce4util7 libxfconf-0-2 libxfconf-0-dev libxml2-utils libxres-dev valac valac-0.40-vapi xfce4-panel xfce4-panel-dev xfconf
```

# WIP notes for different distros
```
UNIVERSAL:

git
build-essential
cmake

libdbusmenu-glib-dev
libgtk2.0-dev
gobject-introspection
libbamf3-dev
libdbus-glib-1-dev
libffi-dev
libgirepository1.0-dev
libpeas-dev
libstartup-notification0-dev
libwnck-3-dev
libwnck-common
libwnck22
libxres-dev
libvala-0.40-0
valac
valac-0.40-vapi

BUDGIE:
budgie-core-dev
gir1.2-budgie-1.0
libbudgie-plugin0
libbudgietheme0
libraven0

MATE:
libmate-panel-applet-dev


XFCE:
exo-utils
libexo-1-0
libexo-2-0
libexo-common
libexo-helpers
libgarcon-1-0
libgarcon-common
libxfce4panel-2.0-4
libxfce4panel-2.0-dev
libxfce4ui-1-0
libxfce4ui-2-0
libxfce4ui-common
libxfce4util7
libxfce4util-common
libxfce4util-dev
libxfconf-0-2
libxfconf-0-dev
xfce4-panel
xfce4-panel-dev
xfconf


Vala Panel:
libvalapanel0
libvalapanel-dev

Unknown:
libxml2-utils
```
