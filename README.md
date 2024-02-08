# example-deb-package
Simple program as example debian package

[Inspired by this blog post](https://earthly.dev/blog/creating-and-hosting-your-own-deb-packages-and-apt-repo/)

### Debian package naming


- `package-name` is the name of our package, `hello-world` in our case,
- `version` is the version of the software, `0.0.1` in our case,
- `release-number` is used to track different releases of the same software version; it’s usually set to `1`, but hypothetically if there was an error in the packaging (e.g. a file was missed, or the description had an error in it, or a post-install script was wrong), this number would be increased to track the change, and
- `architecture` is the target architecture of the platform, `amd64` in this example; however if your package is architecture-independent (e.g. a python script), then you can set this to `all`.

```
<package-name>_<version>-<release-number>_<architecture>
```

