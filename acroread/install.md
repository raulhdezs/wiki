How to install Adobe Acrobat Reader on Ubuntu 20.04
===================================================
    
1. Update your system
        
```sh
    $ sudo apt-get update
```

2. Enable the i386 Architecture

```sh
    $ sudo dpkg --add-architecture i386
```

3. Install software dependencies for Adobe Reader

```sh
    $ sudo apt install libxml2:i386 libcanberra-gtk-module:i386 gtk2-engines-murrine:i386 libatk-adaptor:i386
```

4. Grab Adobe Acrobat Reader binary package

```sh
    $ wget -O ~/adobe.deb ftp://ftp.adobe.com/pub/adobe/reader/unix/9.x/9.5.5/enu/AdbeRdr9.5.5-1_i386linux_enu.deb
```

5. Install Adobe Acrobat Reader

```sh
    $ sudo dpkg -i /AdbeRdr9.5.5-1_i386linux_enu.deb
```

6. Remove binary package

```sh
    $ rm ~/adobe.deb
```

7. Launch Adobe Acrobat Reader

```sh
    $ acroread
```

**Reference:** [https://linuxhint.com/install-adobe-acrobat-reader-ubuntu/](https://linuxhint.com/install-adobe-acrobat-reader-ubuntu/)
