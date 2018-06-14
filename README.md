### GN BUILD For Personal Project

The first step is to [install Chromium's depot_tools](https://storage.googleapis.com/chrome-infra/depot_tools.zip). We use depot_tools to pull in our other dependencies (e.g., gn).

Once you've installed depot_tools, create a ```.gclient``` file in an empty directory with the following contents:

```
solutions = [{
  'managed': False,
  'name': 'src',
  'url': 'https://github.com/realcome/gn_build.git',
  'deps_file': 'DEPS',
}]
```
And then run ```gclient sync```
