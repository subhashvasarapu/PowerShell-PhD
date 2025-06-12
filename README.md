# 🧠 PowerShell-PhD – A Complete PowerShell Learning Repository

*A structured, ultra-granular, example-driven reference repo for mastering PowerShell with real-world Azure and Windows automation.*

---

## 📚 Table of Contents

### 🚀 Core PowerShell Concepts (Fundamentals)

* [Introduction to PowerShell](docs/fundamentals/introduction.md)
* [Variables](docs/fundamentals/variables.md)

  * [Variable Types](docs/fundamentals/variables-types.md)
  * [Scope: Global, Script, Local](docs/fundamentals/variables-scope.md)
  * [Automatic Variables](docs/fundamentals/variables-auto.md)
  * [Environment Variables](docs/fundamentals/variables-env.md)
  * [Preference Variables](docs/fundamentals/variables-preference.md)
* [Data Types](docs/fundamentals/data-types.md)

  * [String](docs/fundamentals/types-strings.md)
  * [Integer, Float, Decimal](docs/fundamentals/types-numbers.md)
  * [Boolean](docs/fundamentals/types-booleans.md)
  * [DateTime](docs/fundamentals/types-datetime.md)
  * [Null, \$null](docs/fundamentals/types-null.md)
  * [PSCustomObject vs Object\[\]](docs/fundamentals/types-objects.md)
* [Operators](docs/fundamentals/operators.md)

  * [Arithmetic](docs/fundamentals/operators-arithmetic.md)
  * [Assignment](docs/fundamentals/operators-assignment.md)
  * [Comparison](docs/fundamentals/operators-comparison.md)
  * [Logical](docs/fundamentals/operators-logical.md)
  * [Type (-is, -as)](docs/fundamentals/operators-type.md)
  * [Containment (-in, -contains)](docs/fundamentals/operators-containment.md)
  * [Match (-match, -like)](docs/fundamentals/operators-match.md)
  * [Range & Unary](docs/fundamentals/operators-range-unary.md)
  * [Bitwise Operators](docs/fundamentals/operators-bitwise.md)

### 🔁 Control Flow (Conditionals + Loops)

* [Conditionals](docs/control-flow/index.md)

  * [If Statement](docs/control-flow/if.md)
  * [If-Else](docs/control-flow/if-else.md)
  * [If-ElseIf-Else](docs/control-flow/if-elseif-else.md)
  * [Switch Statement](docs/control-flow/switch.md)
  * [Ternary Logic Simulation](docs/control-flow/ternary.md)

* [Loops Overview](https://github.com/subhashvasarapu/PowerShell-PhD/tree/main/Loops%20Overview)

  * [For Loop](docs/control-flow/loops-for.md)
  * [ForEach Loop](docs/control-flow/loops-foreach.md)
  * [ForEach-Object (Pipeline)](docs/control-flow/loops-foreach-object.md)
  * [While Loop](docs/control-flow/loops-while.md)
  * [Do-While Loop](docs/control-flow/loops-do-while.md)
  * [Do-Until Loop](docs/control-flow/loops-do-until.md)
  * [Infinite Loops & Breaking](docs/control-flow/loops-infinite.md)
  * [Nested Loops](docs/control-flow/loops-nested.md)
  * [Loop Labels, break, continue](docs/control-flow/loops-break-continue.md)
  * [Loop with Timers](docs/control-flow/loops-timer.md)
  * [Looping Through Files](docs/control-flow/loops-files.md)
  * [Looping with Index and Value](docs/control-flow/loops-index.md)

### 🧰 Scripting & Advanced Fundamentals

* [Functions](docs/functions/index.md)

  * [Basic Functions](docs/functions/basic.md)
  * [Parameter Sets](docs/functions/parameters.md)
  * [Advanced Functions (CmdletBinding)](docs/functions/cmdletbinding.md)
  * [Dynamic Parameters](docs/functions/dynamic-parameters.md)
  * [Function Validation](docs/functions/validation.md)
  * [Return Values & Output](docs/functions/return.md)
  * [Function Scope & Closure](docs/functions/scope.md)

* [Collections: Arrays, Lists, HashTables](docs/fundamentals/collections.md)

  * [Arrays](docs/fundamentals/collections-arrays.md)
  * [ArrayList](docs/fundamentals/collections-arraylist.md)
  * [Multi-Dimensional Arrays](docs/fundamentals/collections-multidim.md)
  * [HashTables](docs/fundamentals/collections-hashtable.md)
  * [Ordered Dictionary](docs/fundamentals/collections-ordereddict.md)
  * [Dictionaries vs HashTables](docs/fundamentals/collections-dictionary.md)

* [String Manipulation](docs/fundamentals/strings.md)

  * [Concatenation, Replace](docs/fundamentals/strings-basic.md)
  * [Substring, IndexOf, Split](docs/fundamentals/strings-advanced.md)
  * [Regex](docs/fundamentals/strings-regex.md)
  * [String Formatting](docs/fundamentals/strings-formatting.md)
  * [String Interpolation](docs/fundamentals/strings-interpolation.md)

* [Pipeline](docs/fundamentals/pipelines.md)

  * [Pipeline Basics](docs/fundamentals/pipeline-objects.md)
  * [Where-Object, Select-Object](docs/fundamentals/pipeline-where-select.md)
  * [Group-Object, Sort-Object](docs/fundamentals/pipeline-group-sort.md)
  * [Measure-Object](docs/fundamentals/pipeline-measure.md)
  * [Pipeline Performance](docs/fundamentals/pipeline-performance.md)

* [Error Handling](docs/fundamentals/error-handling.md)

  * [Try/Catch/Finally](docs/fundamentals/error-trycatch.md)
  * [ErrorAction, ErrorVariable](docs/fundamentals/error-preferences.md)
  * [\$Error and \$LASTEXITCODE](docs/fundamentals/error-systemvars.md)
  * [Custom Error Throwing](docs/fundamentals/error-throw.md)

### ⚙️ Advanced Topics

* [Custom Objects](docs/advanced/custom-objects.md)
* [Working with Classes](docs/advanced/classes.md)
* [Modules: Create/Import](docs/advanced/modules.md)
* [Remoting & Sessions](docs/advanced/remoting.md)
* [Background Jobs & Runspaces](docs/advanced/jobs.md)
* [Secure Strings & Credentials](docs/advanced/credentials.md)
* [Reflection & .NET Access](docs/advanced/reflection.md)
* [Registry Access](docs/advanced/registry.md)
* [File System Management](docs/advanced/filesystem.md)
* [Logging & Transcripts](docs/advanced/logging.md)
* [Data Formats: JSON/XML/CSV](docs/advanced/dataformats.md)
* [Scheduled Tasks and Automation](docs/advanced/scheduler.md)
* [Event Triggers](docs/advanced/event-triggers.md)
* [Code Profiling and Benchmarking](docs/advanced/performance.md)

### ☁️ PowerShell + Azure & Windows

* [Install Az Module](docs/azure/az-module.md)
* [Azure Resources Management](docs/azure/resources.md)
* [Runbooks & Automation Accounts](docs/azure/runbooks.md)
* [Azure AD with PowerShell](docs/azure/ad.md)
* [Graph API Access](docs/azure/graph.md)
* [Windows AD: Users, GPO, OUs](docs/windows/ad.md)
* [Managing Services, Processes](docs/windows/services.md)
* [Scheduled Tasks](docs/windows/scheduler.md)
* [Event Logs & Viewer](docs/windows/events.md)
* [Exporting to Excel](docs/windows/export-excel.md)
* [Managing Local Accounts](docs/windows/local-users.md)
* [Windows Defender & Security](docs/windows/security.md)

### 🧪 Troubleshooting & Debugging

* [Using \$?, \$Error](docs/debugging/errors.md)
* [Breakpoints, Step Debugging](docs/debugging/breakpoints.md)
* [Set-PSBreakpoint](docs/debugging/set-breakpoints.md)
* [Transcript & Logging](docs/debugging/logging.md)
* [Verbose and Debug Streams](docs/debugging/streams.md)

### 🛠️ Developer Environment & Tools

* [PowerShell Profiles](docs/tools/profiles.md)
* [VS Code Integration](docs/tools/vscode.md)
* [ImportExcel Module](docs/tools/importexcel.md)
* [Reusable Functions](docs/tools/snippets.md)
* [GitHub CLI + Git](docs/tools/git.md)
* [PSScriptAnalyzer](docs/tools/analyzer.md)
* [Task Scheduler GUI & Cmdlets](docs/tools/scheduler.md)

### 📦 Sample Scripts Gallery

* [Looping Demos](samples/loops-examples.ps1)
* [Azure CSV Export](samples/export-azure-resources.ps1)
* [Custom Object to Excel](samples/customobject-export.ps1)
* [Regex Pattern Match](samples/regex-match.ps1)
* [Schedule Task Setup](samples/schedule-task.ps1)
* [Error Handling Demos](samples/error-handling.ps1)
* [Service Restart with Logging](samples/service-restart.ps1)
* [Pipeline Performance Test](samples/pipeline-performance.ps1)

---

## 📁 Folder Structure Map

```
powershell-phd/
├── README.md
├── docs/
│   ├── fundamentals/
│   │   ├── introduction.md
│   │   ├── variables.md
│   │   ├── variables-types.md
│   │   ├── variables-scope.md
│   │   ├── variables-auto.md
│   │   ├── variables-env.md
│   │   ├── data-types.md
│   │   ├── types-strings.md
│   │   ├── types-numbers.md
│   │   ├── types-booleans.md
│   │   ├── types-datetime.md
│   │   ├── types-null.md
│   │   ├── operators.md
│   │   ├── operators-arithmetic.md
│   │   ├── operators-assignment.md
│   │   ├── operators-comparison.md
│   │   ├── operators-logical.md
│   │   ├── operators-type.md
│   │   ├── operators-containment.md
│   │   ├── operators-match.md
│   │   ├── operators-range-unary.md
│   │   ├── collections.md
│   │   ├── collections-arrays.md
│   │   ├── collections-arraylist.md
│   │   ├── collections-multidim.md
│   │   ├── collections-hashtable.md
│   │   ├── collections-ordereddict.md
│   │   ├── strings.md
│   │   ├── strings-basic.md
│   │   ├── strings-advanced.md
│   │   ├── strings-regex.md
│   │   ├── pipelines.md
│   │   ├── pipeline-objects.md
│   │   ├── pipeline-where-select.md
│   │   ├── pipeline-group-sort.md
│   │   ├── pipeline-performance.md
│   │   ├── error-handling.md
│   │   ├── error-trycatch.md
│   │   ├── error-preferences.md
│   │   ├── error-systemvars.md
│
│   ├── control-flow/
│   │   ├── index.md
│   │   ├── if.md
│   │   ├── if-else.md
│   │   ├── if-elseif-else.md
│   │   ├── switch.md
│   │   ├── loops.md
│   │   ├── loops-for.md
│   │   ├── loops-foreach.md
│   │   ├── loops-foreach-object.md
│   │   ├── loops-while.md
│   │   ├── loops-do-while.md
│   │   ├── loops-do-until.md
│   │   ├── loops-infinite.md
│   │   ├── loops-nested.md
│   │   ├── loops-break-continue.md
│
│   ├── functions/
│   │   ├── index.md
│   │   ├── basic.md
│   │   ├── parameters.md
│   │   ├── cmdletbinding.md
│   │   ├── dynamic-parameters.md
│   │   ├── validation.md
│   │   ├── return.md
│
│   ├── advanced/
│   │   ├── custom-objects.md
│   │   ├── classes.md
│   │   ├── modules.md
│   │   ├── remoting.md
│   │   ├── jobs.md
│   │   ├── credentials.md
│   │   ├── reflection.md
│   │   ├── registry.md
│   │   ├── filesystem.md
│   │   ├── logging.md
│   │   ├── dataformats.md
│
│   ├── azure/
│   │   ├── az-module.md
│   │   ├── resources.md
│   │   ├── runbooks.md
│   │   ├── ad.md
│   │   ├── graph.md
│
│   ├── windows/
│   │   ├── ad.md
│   │   ├── services.md
│   │   ├── scheduler.md
│   │   ├── events.md
│   │   ├── export-excel.md
│
│   ├── debugging/
│   │   ├── errors.md
│   │   ├── breakpoints.md
│   │   ├── set-breakpoints.md
│   │   ├── logging.md
│
│   ├── tools/
│   │   ├── profiles.md
│   │   ├── vscode.md
│   │   ├── importexcel.md
│   │   ├── snippets.md
│   │   ├── git.md
│
├── samples/
│   ├── loops-examples.ps1
│   ├── export-azure-resources.ps1
│   ├── customobject-export.ps1
│   ├── regex-match.ps1
│   ├── schedule-task.ps1
│
├── assets/
│   └── (images, diagrams, visual aids – assumed placeholder)

```


**Happy Scripting – Keep Automating ⚙️🚀**
