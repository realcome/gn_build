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


This project use clang enviroment.
** clang is not support utf16 encoding.([is Bug for clang??](https://bugs.llvm.org/show_bug.cgi?id=32127)).

Fuck clang!!!!!!!!!!!!!!
