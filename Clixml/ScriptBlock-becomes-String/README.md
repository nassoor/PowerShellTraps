# `ScriptBlock` becomes `String`

If a `ScriptBlock` is exported by `Export-Clixml` then it is represented by the
special XML element `SBK` in the result file. This may look like a script block
is designed to be persisted with its type preserved. This is not the case. When
the data are imported by `Import-Clixml` a script block is rehydrated as `String`.

The script [Test-1.ps1](Test-1.ps1) shows the issue.

***

- Stack Overflow [CliXml Serialization/Deserialization lose type](http://stackoverflow.com/q/29211568/608772)
- [PowerShell/issues/4218](https://github.com/PowerShell/PowerShell/issues/4218)
- Microsoft Connect 1202386
