# ⚡ PowerShell Hit Doc – The Ultimate Azure Automation Reference

*A Battle-Tested, Elegant Guide to Mastering PowerShell in Azure Environments*

Welcome to the **PowerShell Hit Doc** – your charming, exhaustive, and battle-tested reference guide for **Azure PowerShell automation**. This markdown handbook combines **practical scripting**, **custom object creation**, **data filtering**, **Excel exporting**, and deep PowerShell fluency into one focused and reusable source.

---

## 📚 Table of Contents

1. [🎯 Introduction & Objective](#-introduction--objective)
2. [📦 Required Modules](#-required-modules)
3. [🔁 Execution Flow Breakdown](#-execution-flow-breakdown)
4. [📜 Script Walkthrough](#-script-walkthrough)
5. [🧱 Custom Objects Explained](#-custom-objects-explained)
6. [🔍 Accessing and Filtering Nested Data](#-accessing-and-filtering-nested-data)
7. [🔄 Practical Deep Dive: Looping and Filtering](#-practical-deep-dive-looping-and-filtering)
8. [🧾 PowerShell Cheatsheet](#-powershell-cheatsheet)
9. [⚠️ Best Practices & Gotchas](#-best-practices--gotchas)
10. [📚 References & Resources](#-references--resources)
11. [🧪 Prompt Behind This Doc](#-prompt-behind-this-doc)

---

## 🎯 Introduction & Objective

**Objective**: Automate the export of Azure ExpressRoute Circuit Authorization data into Excel format, specifically circuits containing `EML` in their names. This demonstrates:

* Resource filtering
* Looping nested properties
* Building clean export structures with `[PSCustomObject]`
* Exporting to Excel using `Export-Excel`

---

## 📦 Required Modules

```powershell
Install-Module -Name Az -Force
Install-Module -Name ImportExcel -Scope CurrentUser
```

* `Az`: Azure PowerShell module.
* `ImportExcel`: Export data to `.xlsx` without needing Excel installed.

---

## 🔁 Execution Flow Breakdown

1. Fetch all ExpressRoute Circuits.
2. Filter only those with `EML` in their names.
3. Loop through each filtered circuit.
4. Access nested `.Authorizations` property.
5. Loop through each authorization and extract data.
6. Create structured PowerShell objects.
7. Export to Excel.

---

## 📜 Script Walkthrough

```powershell
$EMLCircuitList = Get-AzExpressRouteCircuit | Where-Object { $_.Name -like '*EML*' }
$exportList = @()

foreach ($Circuit in $EMLCircuitList) {
    $circuitName = $Circuit.Name
    if ($Circuit.Authorizations) {
        foreach ($auth in $Circuit.Authorizations) {
            $exportList += [PSCustomObject]@{
                CircuitName       = $circuitName
                AuthName          = $auth.Name
                AuthState         = $auth.AuthorizationUseStatus
                ProvisioningState = $auth.ProvisioningState
            }
        }
    }
}

$exportList | Export-Excel -Path 'C:\Temp\EMLExpressRouteCircuitAuthList.xlsx' -WorksheetName 'AuthList' -AutoSize -TableName 'AuthList'
```

---

## 🧱 Custom Objects Explained

Custom objects created using `[PSCustomObject]` are structured containers that allow you to output readable, exportable, and reusable tabular data.

### ✅ Why Use Them?

* Exporting to Excel/CSV/JSON becomes easy.
* Makes tabular output human-readable.
* Ensures consistent fields for automation pipelines.

### 💡 Syntax

```powershell
[PSCustomObject]@{
    Name  = 'Sample'
    Type  = 'Demo'
    Value = 123
}
```

---

## 🔍 Accessing and Filtering Nested Data

### Accessing First Circuit's Authorization:

```powershell
$emlCircuitList[0].Authorizations
```

### Get First Authorization Name:

```powershell
$emlCircuitList[0].Authorizations[0].Name
```

### Expand All Authorization Names:

```powershell
$emlCircuitList[0].Authorizations | Select-Object -ExpandProperty Name
```

---

## 🔄 Practical Deep Dive: Looping and Filtering

### Looping Circuits:

```powershell
foreach ($Circuit in $EMLCircuitList) {
    Write-Output $Circuit.Name
}
```

### Nested Loop on Authorizations:

```powershell
foreach ($Circuit in $EMLCircuitList) {
    foreach ($auth in $Circuit.Authorizations) {
        Write-Output $auth.Name
    }
}
```

### Null Checking:

```powershell
if ($Circuit.Authorizations) { ... }
```

---

## 🧾 PowerShell Cheatsheet

| Feature                | Example                               |
| ---------------------- | ------------------------------------- |
| Array Indexing         | `$arr[0]`                             |
| Dot Notation           | `$obj.Property`                       |
| Filter Items           | `Where-Object { $_.Name -eq 'Test' }` |
| Create Object          | `[PSCustomObject]@{ Name = 'Test' }`  |
| Nested Property Access | `$obj.Prop[0].SubProp`                |
| Excel Export           | `Export-Excel -Path 'file.xlsx'`      |

---

## ⚠️ Best Practices & Gotchas

* Always check for null before looping nested arrays.
* Use `[PSCustomObject]` instead of `New-Object` for better performance.
* Prefer `-ExpandProperty` to get clean values.
* Avoid `.Add()` on arrays — use `+=` or `[List[object]]` for big loops.

---

## 📚 References & Resources

* [PowerShell Docs](https://learn.microsoft.com/en-us/powershell/)
* [Az PowerShell Module](https://learn.microsoft.com/en-us/powershell/azure/overview)
* [ImportExcel GitHub](https://github.com/dfinke/ImportExcel)
* [Azure ExpressRoute Docs](https://learn.microsoft.com/en-us/azure/expressroute/expressroute-introduction)

---

## 🧪 Prompt Behind This Doc

> "Create a comprehensive and stylish markdown reference document in the format of a 'Hit Doc' — like a README, for PowerShell Azure scripting use case. Include sections for objective, modules used, full script, custom object explanation, deep dive into filtering and looping through nested properties, cheatsheet table, best practices, and a prompt at the end for replication. Use markdown syntax like a well-organized GitHub project."

---

**Happy Scripting! 💻⚙️**
