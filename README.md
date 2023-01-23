Instructions for building picom-pijulius on void linux using xbps-src:

    Setup the void-packages repo:

❯ git clone --depth=1 https://github.com/void-linux/void-packages

❯ cd void-packages

❯ ./xbps-src binary-bootstrap

❯ echo XBPS_ALLOW_RESTRICTED=yes >> etc/conf


    Download the template repo and copy into srcpkgs:

❯ git clone https://github.com/evfeal/picom-pijulius-template

❯ mv picom-pijulius-template ./srcpkgs/picom-pijulius

    Build & install the package:

❯ ./xbps-src pkg picom-pijulius
❯ sudo xbps-install --repository=hostdir/binpkgs picom-pijulius

Note #1: if you have xtools installed you can install the package by running xi -f picom-pijulius (instead of using xbps-install).

Note #2: before installing the package make sure to remove all other compton|picom packages with sudo xbps-remove picom compton.
