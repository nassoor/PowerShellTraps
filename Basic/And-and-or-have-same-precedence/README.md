# Operators `-and` and `-or` have the same precedence

Logical operators `-and` and `-or` have the same precedence, unlike in other
programming languages where logical `AND` has higher precedence.

This C# expression is evaluated to true

```csharp
    true || true && false
```

This similar PowerShell expression is evaluated to false

```powershell
    $true -or $true -and $false
```

To avoid this trap, especially on translating code from other languages to PowerShell, use parenthesis

```powershell
    $true -or ($true -and $false)
```

Scripts

- [Test-CSharp.ps1](Test-CSharp.ps1) tests the above C# expression.
- [Test-PowerShell.ps1](Test-PowerShell.ps1) tests the similar PowerShell expression, the result is different.

---

- [Operators-with-equal-precedence](../Operators-with-equal-precedence)
- Microsoft Connect 285170
