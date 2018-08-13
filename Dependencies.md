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

Didn't work? Installing also libdbusmenu-glib-dev libgtk2.0-dev
