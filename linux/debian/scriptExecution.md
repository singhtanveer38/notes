# Executing script without mentioning full path

If the user want to execute a script without mentioning full path, like ```~/someDirectory/someScript```, the following line can be added to the ```.bashrc``` file

```export PATH="$HOME/someDirectory:$PATH"```
