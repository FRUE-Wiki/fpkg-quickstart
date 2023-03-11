#### Installing and removing packages
- To install a package, use the `-i` option. 
   Example:
```
# fpkg -i package
```
  And its as easy as that. The `-i` option will search for the package in the default repository, and then fetch it. Once it's fetched, FPKG will extract the package with `tar` and run the `install.sh` in the package's folder.

- To remove a package, use the `-r` option.
   Example:
```
# fpkg -r package   
```
   When FPKG removes a package, it runs the `remove.sh` script in the package's folder. This makes it easier to code FPKG, and easier to package programs.

#### What is `install.sh` and `remove.sh` ?
`install.sh` and `remove.sh` are scripts used by FPKG to install, and well, remove a package. These are created by the package maintainer, and they shouldn't be tampered with.

#### Examples:

Example `install.sh` file:
```
export EXEC=binary-file
mv /var/tmp/fpkg/$PACKAGE/$EXEC /bin
mv /var/tmp/fpkg/$PACKAGE/opt/ /opt/$PACKAGE
mv /var/tmp/fpkg/$PACKAGE /var/fpkg/packages/
echo "Install $PACKAGE success!"
export INSTALL_SUCCESS="1"
```

Example `remove.sh` file:
```
export EXEC=binary-file
rm /bin/$EXEC
rm -r /opt/$PACKAGE
rm -rf /var/fpkg/packages/$PACKAGE
echo "Remove $PACKAGE success!"
export REMOVE_SUCCESS="1"
```

*If you want to package your own software, see [[Packaging your own Software for FPKG]]*
*Back to homepage: [[FPKG Quick Start Guide]]*