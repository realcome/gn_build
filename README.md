### GN BUILD For Personal Project

The first step is to [install Chromium's depot_tools](http://www.chromium.org/developers/how-tos/install-depot-tools). We use depot_tools to pull in our other dependencies (e.g., gn).

Once you've installed depot_tools, create a .gclient file in an empty directory with the following contents:

```
solutions = [{
  'managed': False,
  'name': 'src',
  'url': 'https://github.com/realcome/gn_build.git',
  'deps_file': 'DEPS',
}]
```
