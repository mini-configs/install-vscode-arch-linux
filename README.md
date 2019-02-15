### My vscode installation from AUR repo

``` sh
# clone the Visual Studio Code’s AUR repository:
$ cd Downloads/
[user@batman Downloads]$ tar xvf visual-studio-code-bin.tar.gz 
[user@batman Downloads]$ cd visual-studio-code-bin

# make a pacman package of Visual Studio Code:
[user@batman visual-studio-code-bin]$ makepkg -s
==> Making package: visual-studio-code-bin 1.30.2-1 (sex 15 fev 2019 17:29:40 -02)
==> Checking runtime dependencies...
==> Installing missing dependencies...
[sudo] password for user: 
resolving dependencies...
looking for conflicting packages...

Packages (1) lsof-4.91-1

Total Installed Size:  0,23 MiB

:: Proceed with installation? [Y/n] Y
    
    ...

(1/1) installing lsof                                  [#############################] 100%
:: Running post-transaction hooks...
(1/1) Arming ConditionNeedsUpdate...
==> Checking buildtime dependencies...
==> Retrieving sources...

  ...

==> Finished making: visual-studio-code-bin 1.30.2-1 (sex 15 fev 2019 17:32:38 -02)
# pacman package should be created at this point.


# install the generated pacman package with pacman package manager:
[user@batman visual-studio-code-bin]$ sudo pacman -U visual-studio-code-bin-1.30.2-1-x86_64.pkg.tar.xz 
loading packages...
resolving dependencies...
looking for conflicting packages...

Packages (1) visual-studio-code-bin-1.30.2-1

Total Installed Size:  185,49 MiB

:: Proceed with installation? [Y/n] Y
(1/1) checking keys in keyring                         [#############################] 100%
(1/1) checking package integrity                       [#############################] 100%
(1/1) loading package files                            [#############################] 100%
(1/1) checking for file conflicts                      [#############################] 100%
(1/1) checking available disk space                    [#############################] 100%
:: Processing package changes...
(1/1) installing visual-studio-code-bin                [#############################] 100%
Optional dependencies for visual-studio-code-bin
    gvfs: Needed for move to trash functionality [installed]
    libdbusmenu-glib: Needed for KDE global menu
:: Running post-transaction hooks...
(1/2) Arming ConditionNeedsUpdate...
(2/2) Updating the desktop file MIME type cache...

# remove the downloaded files and clean up your ~/Downloads directory:
[user@batman visual-studio-code-bin]$ cd ../ && sudo rm -rfv visual-studio-code-bin/
```
