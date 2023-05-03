# Dynamic switch parameter

Dynamic switches specified before positional parameter arguments with omitted
parameter names swallow these arguments and make a command invalid, either due
to incorrect syntax or shifted arguments. In the latter case a command may even
work without errors with incorrect input parameters.

Workarounds

- Specify dynamic switches with values `-ReadOnly:$true`.
- Or specify dynamic switches after positional parameters.
- Or do not omit parameter names of positional parameters.

Scripts

- [dynamic.switch.fails.ps1](dynamic.switch.fails.ps1) shows how a dynamic switch causes an error.
- [dynamic.switch.works.ps1](dynamic.switch.works.ps1) is the above script corrected.

---

- Stack Overflow [Dynamic switches before positional parameters may not work as expected](http://stackoverflow.com/q/25560038/323582)
- Invoke-Build [#4](https://github.com/nightroman/Invoke-Build/issues/4)
- PowerShell [#19495](https://github.com/PowerShell/PowerShell/issues/19495)
- Microsoft Connect 960194
