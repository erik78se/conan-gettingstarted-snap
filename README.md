# md5example - snap

This is a snap of the [conan getting started] md5 example.

Once, built, the binary and dependent libraries are packaged 
in the snap to be installed with snap.

`$ sudo snap install md5example_0.1_amd64.snap`

## Running
Once installed, you can test it as

`$ md5example.md5-launch`


## Building

Install lxd (to make build fast)
```
sudo snap install snapcraft lxd
```

build with snapcraft
```
snapcraft --use-lxd 
```

### Details of build/snap

The build pulls the [conan getting started] repo, installs conan, installs dependencies with conan and builds.

It places dependencies (conan install -g deploy) in the snap aswell.

The md5 binary has the LD_LIBRARY_PATH set to use the dependencies.


[conan getting started]: https://docs.conan.io/en/latest/getting_started.html
