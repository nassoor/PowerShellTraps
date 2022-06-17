# `Start-Process`

### `Start-Process` fails in a directory with brackets

If `Start-Process` is invoked with an item in a directory with brackets then it fails.

The script [Test-1-directory-with-brackets.ps1](Test-1-directory-with-brackets.ps1) shows the issue.

### Start-Process: ErrorAction is ignored

`Start-Process` may write terminating errors regardless of the specified
parameter `ErrorAction`.

The script [Test-2-ErrorAction-ignored.ps1](Test-2-ErrorAction-ignored.ps1) shows the issue.

---

- Microsoft Connect 1449458
