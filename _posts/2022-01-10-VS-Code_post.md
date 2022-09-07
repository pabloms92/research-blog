# VS Code
In this post I include useful shortcuts, a cheatsheet or setup for VS Code

## Shortcuts

Seen on [medium](https://betterprogramming.pub/15-useful-vscode-shortcuts-to-boost-your-productivity-415de3cb1910)

- Opens the palette to search for a file

```CTRL + P```

- Add cursors to all matching selections

``` CTRL + SHIFT + L```

- Add cursor to next matching selection

```CTRL + D ```

- Undo last cursor operation

```CTRL + U ```

- Select current line

```CTRL + L ```

- Move line up or down

```ALT + UP/DOWN ```

- Duplicate selection up or down

```SHIFT+ALT+UP/DOWN ```

- Open integrated terminal

```CTRL+ ` ```
> German keyboard is CTRL+ ö

- Toggle Sidebar

```CTRL+B ```


__```code .```__  opens VS Code from the terminal


## Default terminal
### Conda
from [here](https://medium.com/analytics-vidhya/efficient-way-to-activate-conda-in-vscode-ef21c4c231f2)

Activate your environment\
```conda activate``` *```<env_name> ```* \
Get the path to your environment running\
```where python```
The output should be something like\
```C:\Users\```*```<user_name>```*```\AppData\Local\Continuum\anaconda3\python.exe``` \
or in the case of an environment:\
```C:\Users\```*```<user_name>```*```\AppData\Local\Continuum\anaconda3\envs\```*```<env_name>```*```\python.exe``` \

```CTRL+SHIFT+P``` to open **Preference: Open User Settings (JSON)**.
- User settings  globally in VSCode
- Workspace settings on a specific project.

Set the `python.condaPath` variable to the desired path
Keep in mind that you may have to replace \\ by \\\\