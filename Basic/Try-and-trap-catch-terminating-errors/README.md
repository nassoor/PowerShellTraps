# `try` and `trap` catch terminating errors

`try` and `trap` catch only terminating and [semi-terminating](../Errors-of-unusual-type) errors.
Thus, if the current error action preference is not *Stop* then non-terminating
errors are not caught. Note that the default PowerShell error action preference
is *Continue*.

In order to catch all errors use

```powershell
    $ErrorActionPreference = 'Stop'
```

Scripts

- [test.1.1.try.ps1](test.1.1.try.ps1) - `try` does not catch an error.
- [test.1.2.try.ps1](test.1.2.try.ps1) - `try` catches an error.
- [test.2.1.trap.ps1](test.2.1.trap.ps1) - `trap` does not catch an error.
- [test.2.2.trap.ps1](test.2.2.trap.ps1) - `trap` catches an error, then `continue`.
- [test.2.3.trap.ps1](test.2.3.trap.ps1) - `trap` catches an error, then `break`.

---

- [Errors-of-unusual-type](../Errors-of-unusual-type)
- Stack Overflow [Try/catch does not seem to have an effect](http://stackoverflow.com/q/1142211/323582)
