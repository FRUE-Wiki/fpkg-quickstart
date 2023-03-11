##### This is more of an expert kind of thing, but nonetheless it is possible.

This isn't a widely supported option, but if you prefer to update one package instead of all packages, you can do so with the following command:

```
# fpkg -up ; fpkg -d package ; fpkg -i /var/tmp/fpkg/downloads/$package
```

This command will:
- Fetch new repositiories
- Download the single package
- Install the single package (updated version)

Since this is updating a single package, it could possibly break the package since dependencies will not be upgraded along with it.

*Back to homepage: [[FPKG Quick Start Guide]]*