# Kernel and OS basics

## Root & System vs. regular sues
- root (linux) and system (windows) user have full control over the system
- can issue any commands to kernel. 
- can tell kernel to self destroy iteslf if wanted or wipe out all files on disk

## Local Shell vs. Remote Shell
- local shell: terminal application running on your local machine
- remote shell: terminal session connected to a remote machine over a network (e.g., SSH)
- remote shell allows you to execute commands on a different computer as if you were physically present there
    - does termius use ssh? how can it easily move directory between local and ssh connection? 
- if one local shell and asked whoami, it will return local user
- but if go on ssh, and do whoami, it will return remote username 



## clients vs servers
- client: software or device that requests services or resources from a server
- server: software or device that provides services or resources to clients

## Interacting in Shell(terminal)
- -h for help (default option if no other option is provided) for any command.
- nmap - network mapper, used for network discovery and security auditing
    - why run this tool from terminal? 
        - its efficient rather than having cool interfaces and getting the information you want.

## Metasploit exploit
- metasploit is a penetration testing framework that helps security professionals identify and exploit vulnerabilities in computer systems
- understand what attackers can do once they gain access to a system. 
- it has database of known vulnerabilities and exploits that can be used to test the security of a system.
- if a target machine has known vulnerabilities, metasploit can be used to exploit those vulnerabilities and gain access to the system.
- the hard part is to find the vulnerabilities, once found, using metasploit is easy.
- the attacker that is trying to achieve is a shell (terminal) on the target machine.
- 