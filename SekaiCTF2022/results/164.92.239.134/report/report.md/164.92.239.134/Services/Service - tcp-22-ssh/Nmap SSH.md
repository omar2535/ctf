```bash
nmap -vv --reason -Pn -T4 -sV -p 22 --script="banner,ssh2-enum-algos,ssh-hostkey,ssh-auth-methods" -oN "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp22/tcp_22_ssh_nmap.txt" -oX "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp22/xml/tcp_22_ssh_nmap.xml" 164.92.239.134
```

[/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp22/tcp_22_ssh_nmap.txt](file:///home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp22/tcp_22_ssh_nmap.txt):

```
# Nmap 7.92 scan initiated Fri Sep 30 16:03:44 2022 as: nmap -vv --reason -Pn -T4 -sV -p 22 --script=banner,ssh2-enum-algos,ssh-hostkey,ssh-auth-methods -oN /home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp22/tcp_22_ssh_nmap.txt -oX /home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp22/xml/tcp_22_ssh_nmap.xml 164.92.239.134
Nmap scan report for 164.92.239.134
Host is up, received user-set (0.16s latency).
Scanned at 2022-09-30 16:03:44 PDT for 5s

PORT   STATE SERVICE REASON  VERSION
22/tcp open  ssh     syn-ack OpenSSH 8.2p1 Ubuntu 4ubuntu0.5 (Ubuntu Linux; protocol 2.0)
|_banner: SSH-2.0-OpenSSH_8.2p1 Ubuntu-4ubuntu0.5
| ssh2-enum-algos: 
|   kex_algorithms: (9)
|       curve25519-sha256
|       curve25519-sha256@libssh.org
|       ecdh-sha2-nistp256
|       ecdh-sha2-nistp384
|       ecdh-sha2-nistp521
|       diffie-hellman-group-exchange-sha256
|       diffie-hellman-group16-sha512
|       diffie-hellman-group18-sha512
|       diffie-hellman-group14-sha256
|   server_host_key_algorithms: (5)
|       rsa-sha2-512
|       rsa-sha2-256
|       ssh-rsa
|       ecdsa-sha2-nistp256
|       ssh-ed25519
|   encryption_algorithms: (6)
|       chacha20-poly1305@openssh.com
|       aes128-ctr
|       aes192-ctr
|       aes256-ctr
|       aes128-gcm@openssh.com
|       aes256-gcm@openssh.com
|   mac_algorithms: (10)
|       umac-64-etm@openssh.com
|       umac-128-etm@openssh.com
|       hmac-sha2-256-etm@openssh.com
|       hmac-sha2-512-etm@openssh.com
|       hmac-sha1-etm@openssh.com
|       umac-64@openssh.com
|       umac-128@openssh.com
|       hmac-sha2-256
|       hmac-sha2-512
|       hmac-sha1
|   compression_algorithms: (2)
|       none
|_      zlib@openssh.com
| ssh-auth-methods: 
|   Supported authentication methods: 
|     publickey
|_    keyboard-interactive
| ssh-hostkey: 
|   3072 70:01:39:b5:bd:6e:7a:3d:42:be:f1:84:ec:3a:15:f3 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDTJ0zGKrT4zpnYABmgzm58MH9da3fVsQxZ0/4rsG4h8qDVxwjpSBtBsom0QEj3Jplb+/kcqmEd4fubeyLjDtQmORxdJCQlvMcwSXc2Oqwfd5D9Gjt2jZoLY0f8mdvq87B3AobsxGzkcTzgrtQSRCXZYpisGw24QXj/NWRjeTJpwi9HyAhu7APjrwuUQdDV1wzj4qp4mkAd/UVDuhf6XKJK7+5Mxk3ZnltPi4Fy7Ur4xJhyoBdBi0f4AlGsyOZeQiuJhpAyTvsPM6v4gOZrpUEUN6Ts9/gIKK0aoYCHrCUO5bnc/TRy5diAA+zMGnT/KvhUtfeUENyBRB9AZQ8XlfwR38kISQDAR4M9NpYyxB/9ObUuT4/Vw/FYLLg+686cR5dggBfsXBstBdn+rDIywARL3kNqHbYSNkR23c/KOs0aSnxr+sAEt3AOouJQX/mITP68FgAWH31MEpznMVXzc0wIODrGptpyRvm5OtNS7CD9oZWOFl09njtVjaXCwd6Bxlk=
|   256 5f:22:fa:f2:cd:8a:66:f1:b7:f6:f7:40:4c:6b:78:52 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBOsoZjRYIfBfkcQRwZYjbfHpuLfZxn0ydzAqMKYXkUK1/r+HqHa8SP5PFM0+7gantRuN4xARmwTexhOhq27llYU=
|   256 83:83:7b:73:d4:9c:85:04:1b:2a:a0:c9:76:55:4b:67 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIAy7qfiCdiDEd4CdzAcWGqUepaS9sj4RNeeTA3a1dDJ+
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Fri Sep 30 16:03:49 2022 -- 1 IP address (1 host up) scanned in 5.09 seconds

```
