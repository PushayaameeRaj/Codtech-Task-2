NAME: PUSHAYAAMEE RAJ 
COMPANY: CODTECH IT SOLUTIONS 
ID: CT08DS7904 
DOMAIN NAME: CYBER SECURITY AND ETHICAL HACKING 
DURATION: SEPTEMBER TO OCTOBER 2024 
MENTOR: MUZAMMIL

OVERVIEW OF THE PROJECT:

TASK TWO: VULNERABILITY SCANNING TOOL
Creating a simple vulnerability scanning tool that scans a network or website
for common security vulnerabilities such as open ports, outdated software
versions, and misconfigurations.

The script provided is a simple vulnerability scanning tool designed to perform three basic checks:

Open Port Scanning: Scans the target system for open TCP ports within the range of 1-1024.
HTTP Headers Check: Sends an HTTP request to a target URL and examines the headers for potential outdated software versions, such as Apache or PHP.
DNS Check: Resolves the domain name to its corresponding IP address, ensuring the target domain is correctly translated into a machine-readable address.

This tool is useful in cybersecurity assessments, particularly in identifying common vulnerabilities in a target system or website, such as open ports or outdated software that could be exploited by attackers.

Steps of Implementation: 

Step 1: Importing Required Libraries
The script begins by importing two essential Python libraries:
socket: Used for networking operations like establishing connections and performing DNS lookups.
requests: Allows HTTP requests to be sent, which is used to examine the HTTP headers of a web server.

Step 2: Defining the Function to Scan Open Ports
The scan_open_ports function iterates through ports from 1 to 1024 on the target system. It attempts to establish a TCP connection on each port using the socket library.
If the connection is successful (result == 0), the port is considered open and added to the open_ports list.
After iterating through all ports, the script prints the list of open ports or notifies if no open ports were found.

Step 3: Checking HTTP Headers for Outdated Software Versions
The check_http_headers function sends an HTTP GET request to the specified URL using the requests library. It then examines the server's response headers for specific software versions:
Apache/2.2: Outdated Apache web server version.
PHP/5: Outdated PHP version.
If these outdated versions are detected, the script prints a warning. If the HTTP request fails, the function catches the exception and prints an error message.

Step 4: Performing a DNS Check
The check_dns function attempts to resolve the target domain name to its corresponding IP address using the socket.gethostbyname() method. 
If the domain cannot be resolved, an error message is displayed.

Step 5: Main Function to Execute the Checks
In the __main__ block, the script performs the following actions:
Port Scanning: Calls the scan_open_ports() function with the target domain.
HTTP Headers Check: Calls the check_http_headers() function with the target URL.
DNS Resolution: Calls the check_dns() function to resolve the target domain.
This allows the user to test the target for open ports, check for outdated server software, and verify DNS resolution.

Conclusion
This script provides a basic framework for detecting potential vulnerabilities in a target system. 
It demonstrates simple techniques such as port scanning, examining HTTP headers for outdated software, and performing DNS checks—important steps in security auditing.




