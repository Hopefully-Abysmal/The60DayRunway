Apparently as fitbit was acquired by google, google's enshittification continues on! They have yet to and will not be releasing an SDK for Sense 2 and Versa 4. As such my hand is forced to use the following: 'https://github.com/cmengler/fitbit-app-versa4/tree/main' an unofficial sideloading strategy.

## The Ways of the sideload (differentiations using windows)
In Windows PowerShell, the `export` command does not work the same way as it does in Unix-like systems (Linux or macOS), where it is used to set environment variables. In PowerShell, you can set environment variables with a slightly different syntax. Here’s how to set the `FITBIT_QA_COMMANDS` environment variable in PowerShell:

```powershell
$env:FITBIT_QA_COMMANDS = "1"
```

Similarly, if you wish to set `FITBIT_DEVBRIDGE_DUMP`, you would use:

```powershell
$env:FITBIT_DEVBRIDGE_DUMP = "1"
```

