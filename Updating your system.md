##### Keeping your system up-to-date is very important. FPKG helps this by being very fast to update* and delivering updates on a _somewhat_ reasonable schedule

##### Update your system normally
To update your system normally, you can fetch the new repos with:
```
# fpkg -up
```
The `-u` option will call for an update. And `-p` will tell `-u` to update repositories. Never use `-p` by itself, since it doesn't have a purpose *yet*.

And then to upgrade all packages
```
# fpkg -ui
```
The `-i` option combined with `-u` tells FPKG to install upgrades. Now, obviously if you haven't ran `fpkg -up` before `fpkg -ui`, you won't have any updates to install.



** *the speed of the updates depend on your internet connection speed* 

*For expert users, you may want to check out [[Updating individual packages]]*

*Back to homepage: [[FPKG Quick Start Guide]]*