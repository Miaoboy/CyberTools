# Auxiliary
category of modules that are used for a variety of tasks other than exploiting a specific vulnerability. Auxiliary modules are designed to perform functions such as scanning, enumeration, and network services testing. Unlike exploit modules, auxiliary modules do not attempt to gain control of a system but instead focus on gathering information or testing vulnerabilities.
```
root@ip-10-10-135-188:/opt/metasploit-framework/embedded/framework/modules# tree -L 1 auxiliary/
auxiliary/
├── admin
├── analyze
├── bnat   scanner which can detect Broken NAT (network address translation) implementations, which could result in an inability to reach ports on remote machines. Typically, these ports will appear in nmap scans as 'filtered'/'closed'.
├── client
├── cloud
├── crawler
├── docx
├── dos
├── example.py
├── example.rb
├── fileformat
├── fuzzers
├── gather
├── parser
├── pdf
├── scanner
├── server
├── sniffer
├── spoof
├── sqli
├── voip
└── vsploit
```
# Encoder 
Module used to obfuscate (encode) payloads to avoid detection by security solutions. Encoders transform the payload into a different format, making it harder for security tools to detect it while preserving its functionality.
```
root@ip-10-10-135-188:/opt/metasploit-framework/embedded/framework/modules# tree -L 1 encoders/
encoders/
├── cmd
├── generic
├── mipsbe
├── mipsle
├── php
├── ppc
├── ruby
├── sparc
├── x64
└── x86
```
# Evasion
Modules focus on avoiding detection during the entire attack process. This includes obfuscating the payload, modifying delivery methods, or exploiting weaknesses in security tools.
```
root@ip-10-10-135-188:/opt/metasploit-framework/embedded/framework/modules# tree -L 2 evasion/
evasion/
└── windows
    ├── applocker_evasion_install_util.rb
    ├── applocker_evasion_msbuild.rb
    ├── applocker_evasion_presentationhost.rb
    ├── applocker_evasion_regasm_regsvcs.rb
    ├── applocker_evasion_workflow_compiler.rb
    ├── process_herpaderping.rb
    ├── syscall_inject.rb
    ├── windows_defender_exe.rb
    └── windows_defender_js_hta.rb
```
# Exploit 
Modules are categorized based on their targets, such as operating systems, applications, or services
```
root@ip-10-10-135-188:/opt/metasploit-framework/embedded/framework/modules# tree -L 1 exploits/
exploits/
├── aix
├── android
├── apple_ios
├── bsd
├── bsdi
├── dialup
├── example_linux_priv_esc.rb
├── example.py
├── example.rb
├── example_webapp.rb
├── firefox
├── freebsd
├── hpux
├── irix
├── linux
├── mainframe
├── multi
├── netware
├── openbsd
├── osx
├── qnx
├── solaris
├── unix
└── windows
```
```
## Remote Exploits:
Exploits vulnerabilities in network services, allowing attackers to compromise a target remotely.
Example: exploit/windows/smb/ms17_010_eternalblue
Targets: Unpatched SMB servers (EternalBlue vulnerability).

## Local Exploits:
Requires prior access to the target. Exploits local vulnerabilities to escalate privileges or gain more access.
Example: exploit/linux/local/sudo_baron_samedit
Targets: Linux systems with a vulnerable sudo configuration.

## Web Application Exploits:
Targets web servers or applications to compromise backend systems.
Example: exploit/multi/http/struts_dmi_exec
Targets: Apache Struts framework with remote code execution (RCE) vulnerability.

## Client-Side Exploits:
Targets applications running on the victim's machine, such as browsers, PDF readers, or email clients.
Example: exploit/multi/browser/adobe_flash_hacking_team_uaf
Targets: Vulnerable Adobe Flash Player.
```
# NOPs (No Operation)
Instructions or padding used in exploit development to create "no-operation" filler code that does nothing when executed. They are often used to align payloads, avoid bad characters, or provide buffer space during exploitation.
```
root@ip-10-10-135-188:/opt/metasploit-framework/embedded/framework/modules# tree -L 1 nops/
nops/
├── aarch64
├── armle
├── cmd
├── mipsbe
├── php
├── ppc
├── sparc
├── tty
├── x64
└── x86 
```
# Payload 
Delivered to the target system after a vulnerability is successfully exploited. It defines what action is taken after the exploit succeeds, such as opening a reverse shell, injecting malicious code, or collecting sensitive information.
```
root@ip-10-10-135-188:/opt/metasploit-framework/embedded/framework/modules# tree -L 1 payloads/
payloads/
├── adapters - wraps single payloads to convert them into different formats
Example: a normal single payload can be wrapped inside a Powershell adapter, which will make a single powershell command that will execute the payload.
├── singles  - A single piece of code that runs independently that does not rely on a persistent connection or external dependencies.
Example: Adding a user to the system or changing system settings.
├── stagers  - A small payload that sets up a network connection between the attacker and the target.
Used to download and execute a larger "staged" payload.
Reduces the size of the initial payload.
Can bypass certain security mechanisms due to its small size.
└── stages  -  The actual payload delivered by the stager.
Performs the main malicious task, such as interacting with the system or stealing data.
```
# Post-exploitation 
Tools and scripts used after successfully compromising a target system. These modules focus on gathering information, maintaining access, or performing further actions on the compromised system.
```
root@ip-10-10-135-188:/opt/metasploit-framework/embedded/framework/modules# tree -L 1 post/
post/
├── aix
├── android
├── apple_ios
├── bsd
├── firefox
├── hardware
├── linux
├── multi
├── networking
├── osx
├── solaris
└── windows
```
