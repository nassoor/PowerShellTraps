# Break and Continue with not matching label

A missing (misspelled) label used with `continue` or `break` is not an error.
In such cases PowerShell silently breaks the whole script being invoked. That
is why [.test.ps1](.test.ps1) has to call test scripts using `PowerShell.exe`. Otherwise
the whole testing would stop on the first issue, with no errors.

Scripts

- [break.missing.ps1](break.missing.ps1) contains `break missing`.
- [continue.missing.ps1](continue.missing.ps1) contains `continue missing`.

---

- Microsoft Connect 377964
