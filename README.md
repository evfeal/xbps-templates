Instructions for building a template on void linux using xbps-src:

    Setup the void-packages repo:

❯ git clone --depth=1 https://github.com/void-linux/void-packages

❯ cd void-packages

❯ ./xbps-src binary-bootstrap

❯ echo XBPS_ALLOW_RESTRICTED=yes >> etc/conf


    Download the template repo and copy into srcpkgs:

❯ git clone https://github.com/evfeal/xbps-templates

❯ mv templates/{template} ./srcpkgs/{template}

    Build & install the package:

❯ ./xbps-src pkg {package}
❯ sudo xbps-install --repository=hostdir/binpkgs {package}

Note #1: if you have xtools installed you can install the package by running xi -f {package} (instead of using xbps-install).
