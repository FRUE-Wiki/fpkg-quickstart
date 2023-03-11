# Searching for packages
##### Like most package managers, FPKG also has a search function.

To use the search function, you must be connected to the internet as, well, its searching the repositories.

To search for a package:
```
# fpkg -s package
```
Since nothing is being installed, it is possible to search without root permissions, but it is a good practice to use FPKG with something like `su`, `doas`, or `sudo`.
