# [Installation/Update of Atom in debian-linux-ubuntu](https://github.com/atom/atom#debian-linux-ubuntu)

1. Download atom-amd64.deb from the [Atom releases page](https://github.com/atom/atom/releases).
```
cd && mkdir -p .atomtmp && cd .atomtmp
wget https://github.com/atom/atom/releases/download/v1.19.0-beta7/atom-amd64.deb
```
2. Run sudo dpkg --install atom-amd64.deb on the downloaded package.
NB. To avoid any issue in the installation, you have to "sudo apt-get update" and "sudo apt-get upgrade" your machine
```
sudo dpkg --install atom-amd64.deb
```

OUTPUT
```
$ sudo dpkg --install atom-amd64.deb
[sudo] password for map479-admin:
Selecting previously unselected package atom-beta.
(Reading database ... 344309 files and directories currently installed.)
Preparing to unpack atom-amd64.deb ...
Unpacking atom-beta (1.19.0-beta7) ...
Setting up atom-beta (1.19.0-beta7) ...
Processing triggers for gnome-menus (3.10.1-0ubuntu2) ...
Processing triggers for desktop-file-utils (0.22-1ubuntu1) ...
Processing triggers for bamfdaemon (0.5.1+14.04.20140409-0ubuntu1) ...
Rebuilding /usr/share/applications/bamf-2.index...
Processing triggers for mime-support (3.54ubuntu1.1) ...
```


3. delete temporal files
```
cd && rm -rf .atomtmp
```
3. Launch Atom using the installed atom command.



# List of Useful Atom Packages

- Markdown Preview  
- Terminal plus: A terminal package for Atom, complete with themes and more.  
- language-r: A language description and snippets for R  
- split-diff: Diffs text between two split panes.



## ISSUES

The following issue is because the machine has not been updated neither upgraded.
```
$ sudo dpkg --install atom-amd64.deb
[sudo] password for map479:
Selecting previously unselected package atom.
(Reading database ... 238644 files and directories currently installed.)
Preparing to unpack atom-amd64.deb ...
Unpacking atom (1.18.0) ...
dpkg: dependency problems prevent configuration of atom:
 atom depends on git; however:
  Package git is not installed.

dpkg: error processing package atom (--install):
 dependency problems - leaving unconfigured
Processing triggers for gnome-menus (3.13.3-6ubuntu3.1) ...
Processing triggers for desktop-file-utils (0.22-1ubuntu5) ...
Processing triggers for bamfdaemon (0.5.3~bzr0+16.04.20160701-0ubuntu1) ...
Rebuilding /usr/share/applications/bamf-2.index...
Processing triggers for mime-support (3.59ubuntu1) ...
Errors were encountered while processing:
 atom
```
However, it works!