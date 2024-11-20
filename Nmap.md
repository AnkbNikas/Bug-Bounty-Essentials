Nmap: 

Nmap (Network Mapper) is an essential tool in the bug bounty world for several reasons:

1.	Host Discovery: Nmap allows you to identify active devices on a network, which is crucial for mapping the target environment.
	
2.	Port Scanning: You can scan open ports on a host to identify services and applications that might be vulnerable.

3.	Version Detection: Nmap can determine the versions of services running on open ports, which helps in identifying specific vulnerabilities.

4.	Operating System Fingerprinting: Nmap can guess the operating system of the target host, providing additional information that can be useful for finding vulnerabilities.

5.	Custom Scripts: Using the Nmap Scripting Engine (NSE), you can run custom scripts to detect specific vulnerabilities and automate security tasks.
These capabilities make Nmap a powerful tool for security researchers looking to identify and exploit vulnerabilities in bug bounty programs.

[Legal Issues | Nmap Network Scanning](https://nmap.org/book/legal-issues.html)

nmap -A -F -T1 10.10.10.223 -v

-A: Enables all detection options, including service versions, scripts, and more.
-F: Performs a fast scan of the most common ports (100 by default).
-T1: Sets the scan speed to "slow," which can be useful to avoid detection.
-v: Increases the verbosity of the command, providing more information about the scan.

