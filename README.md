QuickLauncher
=============

A minimal Qt based menu to quickly find and execute Maya commands and user scripts.  
Quicklauncher relies on PySide/PySide2/PySide6 and works on Autodesk Maya 2014 or greater. (last tested on Maya 2025)

![quicklauncher](https://cloud.githubusercontent.com/assets/2292742/20506707/8b19023c-b034-11e6-8598-a480924f8740.gif)


## Installation
1. get the [latest release](https://github.com/csaez/quicklauncher/releases) 
2. copy `quicklauncher.py` to your maya script directory. e.g. `%UserProfile%\Documents\maya\2026\scripts` on windows

## Usage

```python
import quicklauncher
quicklauncher.show()
```

You can also select the folder in which `quicklauncher` will look for user scripts (repo).

```python
import quicklauncher
quicklauncher.select_repo()
```



## advanced

import quicklauncher as ql

``` python
# show menu
ql.show()

# repository dialog
ql.select_repo()

# ... or go deeper using the API
ql.get_repo()
ql.set_repo(repository_path)

ql.get_scripts()  # {script_name: script_fullpath, ...}
ql.list_scripts() # [script_name, ...]
ql.run_script(script_name)

ql.get_commands()  # {cmd_name: cmd_object, ...}
ql.list_commands() # [cmd_name, ...]
ql.run_cmd(cmd_name)
```


> **TIP:** You can refresh the list of available scripts without restarting Maya by simply
> reloading the python module in the script editor (or add a little python script that does
> this to your repo so it's available from the menu itself).
>
> ```python
> import quicklauncher
> reload(quicklauncher)
> ```

## Contributing

- [Check for open issues](https://github.com/csaez/quicklauncher/issues) or open a fresh issue to
  start a discussion around a feature idea or a bug.

- Fork the [quicklauncher repository on Github](https://github.com/csaez/quicklauncher) to start
  making your changes (make sure to isolate your changes in a local branch when possible).

- Write a test which shows that the bug was fixed or that the feature works as expected.

- Send a pull request and bug me until it gets merged. :)


Make sure to add yourself to `CONTRIBUTORS.md`!
