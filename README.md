# Getting Started with WPA Hacking

## Introduction

The slides above are from my talk to DC604 in July 2020 about WPA Hacking. I've included a sample capture file for people to practice with.

## Usage

You will need `hcxtools` and `hashcat`. The password is **bettyboop1** which appears in the **rockyou.txt** wordlist available from SecLists.

```bash
git clone https://github.com/oldrho/getting_started_with_wpa_hacking.git
cd getting_started_with_wpa_hacking
hcxpcapngtool -o hashes capture.pcapng
hashcat -m22000 hashes rockyou.txt
# Or
hashcat -m22000 hashes -a3 bettyboop1
```

## Links

**Wireshark**
https://www.wireshark.org/

**hcxdumptool**
https://github.com/ZerBea/hcxdumptool

**hcxtools**
https://github.com/ZerBea/hcxtools

**hashcat**
https://hashcat.net/hashcat/

**hashcat on github**
https://github.com/hashcat/hashcat

**A shortened rockyou.txt that contains the correct password**
https://github.com/danielmiessler/SecLists/blob/master/Passwords/Leaked-Databases/rockyou-45.txt