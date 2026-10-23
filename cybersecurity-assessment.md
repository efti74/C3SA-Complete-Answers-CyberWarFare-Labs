# Cybersecurity Assessment: 30 Multiple-Choice Questions

A 30-question assessment covering cybersecurity fundamentals, networking, virtualization, application security, Linux and Windows security, AWS cloud security, and endpoint detection.

## Instructions

- Read each question carefully.
- Select the most appropriate answer from the four options provided.
- For code and configuration questions, review the examples before answering.
- Use commands and techniques only in systems or networks you own or are explicitly authorized to test.

## Questions

### Question 1

What is Initial Access in the context of cybersecurity?

A. The process of logging into a computer or network for the first time.  
B. The first stage of a cyberattack where an attacker gains unauthorized entry into a system.✔️  
C. The initial step taken by a user to establish a secure connection to a remote server.  
D. The first step in conducting a vulnerability assessment on a network  

### Question 2

How do you categorise the file-attacks based on the following options?

A. An attack where a malicious file is downloaded onto a victim's computer and executed.  
B. An attack where malware is embedded within a file and spreads when the file is opened.  
C. An attack where the attacker gains access to sensitive information stored in files on a compromised system.  
D. An attack that leverages legitimate system tools or processes to execute malicious code without leaving traces on the file system.✔️  

### Question 3

What is a hypervisor in virtualization technology?

A. A software application used for creating virtual machines.  
B. A physical hardware device used to enhance virtual machine performance.  
C. A protocol used for secure communication between virtual machines.  
D. A software component that manages and controls virtual machines on a physical / virtual server.✔️  

### Question 4

What is the difference between Bridge Mode and NAT Mode in virtualization?

A. Bridge Mode enables direct network communication between virtual machines, while NAT Mode provides network address translation for virtual machines.✔️  
B. Bridge Mode provides network address translation for virtual machines, while NAT Mode enables direct network communication between virtual machines.  
C. Bridge Mode allows virtual machines to share the host's IP address, while NAT Mode assigns separate IP addresses to each virtual machine.  
D. Bridge Mode assigns separate IP addresses to each virtual machine, while NAT Mode allows virtual machines to share the host's IP address.  

### Question 5

In the context of web security, what is the implication of "pass the cookie" attack, suppose if an attacker has accessed the session cookie of a website on a client browser that was securely authenticated using MFA (Multi-Factor Authentication)?

A. The attacker can use the stolen session cookie to gain unauthorized access to the specific website.✔️  
B. MFA prevents session cookies from being stolen, so the attack is not possible even if the cookie is accessed.  
C. The stolen session cookie becomes useless for the attacker since MFA provides an additional layer of security.  
D. MFA only protects against password-based attacks, so the attacker can still utilize the stolen session cookie.  

### Question 6

Identify the vulnerability:

```python
import os

def run_command(command):
    try:
        output = os.popen(command).read()
        print("Output:\n", output)
    except:
        print("Error executing command.")
  
command = input("Enter a command: ")
run_command(command)
```

Question: What vulnerability is present in the above Python code?

A. Cross-Site Scripting (XSS)  
B. Remote File Inclusion (RFI)  
C. Remote Code Execution (RCE)✔️  
D. SQL Injection  

### Question 7

Identify the vulnerability:

```python
import os

def read_file(file_name):
    try:
        with open(file_name, "r") as file:
            file_contents = file.read()
            print("File Contents:\n", file_contents)
    except FileNotFoundError:
        print("File not found.")
    except Exception as e:
        print("Error reading file:", str(e))
  
file_name = input("Enter a file name: ")
read_file(file_name)
```

Question: What vulnerability is present in the above Python code?

A. Cross-Site Scripting (XSS)  
B. File Inclusion (FI)✔️  
C. Remote Code Execution (RCE)  
D. SQL Injection  

### Question 8

What is an IDN homograph attack in the context of cybersecurity?

A. An attack that involves intercepting and manipulating data packets between two devices.  
B. An attack that targets insecure network protocols to gain unauthorized access.  
C. An attack that leverages visually similar characters from different character sets to create deceptive domain names.✔️  
D. An attack that exploits vulnerabilities in web browsers to execute arbitrary code.  

### Question 9

In a network traffic analysis using Wireshark, you need to filter and display only HTTP traffic originating from a specific IP address. Which filter expression should you use?

A. ip.src == "specific IP address" && http  
B. ip.dst == "specific IP address" && http  
C. http.request && ip.addr == "specific IP address"✔️  
D. http.response && ip.addr == "specific IP address"  

### Question 10

Which of the following code snippets correctly demonstrates the creation and sending of a TCP packet using Python Scapy?

**A.**

```python
from scapy.all import *

packet = IP(dst="192.168.0.1")/TCP(dport=80)
send(packet)
```  

**B.**✔️

```python
from scapy.all import *

packet = IP(src="192.168.0.1", dst="10.0.0.1")/TCP(sport=1234, dport=80)
send(packet)
```  

**C.**

```python
from scapy.all import *

packet = Ether()/IP(dst="192.168.0.1")/TCP(dport=80)
sendp(packet)
```  

**D.**

```python
from scapy.all import *

packet = IP(dst="192.168.0.1")/TCP(dport=80)
sendp(packet, iface="eth0")
```  

### Question 11

What is the main difference between a reverse shell and a bind shell?

A. The direction of the network connection established.✔️  
B. The encryption used for communication  
C. The operating systems they are compatible with  
D. The type of payload used in the shellcode  

### Question 12

What is the main difference between stagers, singles, and stages in the context of shellcode payloads?

A. The size of the payload generated.  
B. The number of network connections established.✔️  
C. The obfuscation techniques used in the payload.  
D. The type of payloads used for different exploitation scenarios.  

### Question 13

What is the main difference between a Meterpreter and a normal shell?

A. Meterpreter provides advanced post-exploitation capabilities, while a normal shell only offers basic command execution.✔️   
B. Meterpreter can only be used on Windows systems, while a normal shell is compatible with multiple operating systems.  
C. Meterpreter establishes an encrypted connection between the attacker and the target, while a normal shell uses plaintext communication.  
D. Meterpreter requires additional privileges to execute, while a normal shell can be obtained with basic user privileges.  

### Question 14

In Linux, what does the file permission "rw-r--r--" represent?

A. The file is readable and writable by the owner, and readable by the group and others.✔️  
B. The file is readable and writable by the owner, and readable by the group, but not accessible by others.  
C. The file is readable and writable by the owner only, and not accessible by the group and others.  
D. The file is readable by the owner, group, and others, but not writable by anyone.  

### Question 15

GTFO bins are a collection of Unix binaries commonly used for privilege escalation or bypassing restrictions. Which of the following statements about GTFO bins is correct?

A. GTFO bins are pre-compiled binaries specifically designed for hacking purposes.  
B. GTFO bins are legitimate system binaries that can be misused for privilege escalation or bypassing restrictions.✔️  
C. GTFO bins are primarily used for network scanning and port enumeration.  
D. GTFO bins are exclusively used in Windows environments for malicious activities.  

### Question 16

Which of the following statements about the "schtasks" command is correct?

A. The "schtasks" command can only be executed by users with administrative privileges.  
B. The "schtasks" command allows you to create, modify, and delete scheduled tasks on Windows systems.✔️  
C. The "schtasks" command is used to view the list of active processes running on the system.  
D. The "schtasks" command is exclusive to Windows Server editions and cannot be used on Windows client operating systems.  

### Question 17

Which command can be used with the "netsh" command in Windows to extract the WiFi password of a network?

A. netsh wlan show profile name="NetworkName" key=clear✔️  
B. netsh wlan show password name="NetworkName"  
C. netsh wlan view profile name="NetworkName" key=clear  
D. netsh wlan retrieve password name="NetworkName"  

### Question 18

The PowerShell execution policy in Windows serves a crucial role in controlling script execution. Which of the following statements about the PowerShell execution policy is NOT accurate?

A. The execution policy "Restricted" prevents the execution of all scripts on the system, including signed and unsigned scripts.  
B. The execution policy "RemoteSigned" allows the execution of local scripts without digital signatures but requires remote scripts to be signed.  
C. The execution policy "AllSigned" mandates that all scripts, whether local or remote, must be digitally signed to be executed.  
D. The execution policy "Unrestricted" grants unrestricted execution of all scripts without any restrictions or digital signature requirements.✔️  

### Question 19

Consider the following scenarios. Identify the most suitable cloud service model (SaaS, PaaS, or IaaS) for each scenario.
1 An organization wants to use a customer relationship management (CRM) software without the need for managing servers or infrastructure. They prefer a ready-to-use solution accessible over the internet.
2 A development team wants to build and deploy a web application without worrying about underlying infrastructure, operating systems, or runtime environments. They require a platform that provides development tools, database management, and scalability options.
3 A company needs complete control over the operating system, network configuration, and software installations. They want to migrate their existing applications to the cloud while retaining full administrative control.
4 A startup requires an email service to handle their communication needs. They want a cost-effective solution that can scale with their growing business and eliminate the need for managing hardware or software maintenance.

A. Scenario 1: SaaS, Scenario 2: PaaS, Scenario 3: IaaS, Scenario 4: SaaS  
B. Scenario 1: PaaS, Scenario 2: SaaS, Scenario 3: IaaS, Scenario 4: SaaS✔️  
C. Scenario 1: SaaS, Scenario 2: IaaS, Scenario 3: PaaS, Scenario 4: SaaS  
D. Scenario 1: PaaS, Scenario 2: IaaS, Scenario 3: SaaS, Scenario 4: PaaS  

### Question 20

When configuring security groups in AWS, which statement about their behavior is correct?

A. Security groups act as virtual firewalls at the instance level, controlling inbound and outbound traffic based on rules.✔️  
B. Security groups are associated with subnets and control network traffic between different subnets in a VPC.  
C. Security groups are used to restrict access to IAM users and manage user permissions within an AWS account.  
D. Security groups provide network load balancing capabilities to distribute incoming traffic across multiple instances.  

### Question 21

Consider the following scenario related to security groups in AWS. Choose the most appropriate solution based on security group configuration
Scenario: You are setting up security groups for an application in an AWS environment. The application consists of multiple web servers that need to receive HTTP traffic from the internet, and an RDS database instance that needs to be accessible only from the web servers. Additionally, SSH access to the web servers should be limited to a specific IP range for administration purposes.
Which security group rules configuration would be the most suitable for this scenario?

A. Web Server Security Group:
Inbound Rule: Allow HTTP (Port 443) from 0.0.0.0/0
Inbound Rule: Allow SSH (Port 22) from 0.0.0.0/0
Outbound Rule: Allow all traffic to any destination
Database Security Group
Inbound Rule: Allow MySQL (Port 3306) from the web server security group
Outbound Rule: Allow all traffic to any destination  
B. Web Server Security Group:
Inbound Rule: Allow HTTP (Port 80) from 0.0.0.0/0
Inbound Rule: Allow SSH (Port 22) from the specific IP range
Inbound Rule: Allow MySQL (Port 3306) from the RDS instance endpoint
Outbound Rule: Allow all traffic to any destination
Database Security Group:
Inbound Rule: Allow all traffic from the web server security group
Outbound Rule: Allow all traffic to any destination  
C. Web Server Security Group:✔️
Inbound Rule: Allow HTTP (Port 80) from 0.0.0.0/0
Inbound Rule: Allow SSH (Port 22) from the specific IP range
Outbound Rule: Allow all traffic to any destination
Database Security Group:
Inbound Rule: Allow MySQL (Port 3306) from the web server security group
Outbound Rule: Allow all traffic to any destination  
D. Web Server Security Group:
Inbound Rule: Allow HTTP (Port 80) from 0.0.0.0/0
Inbound Rule: Allow SSH (Port 22) from the specific IP range
Inbound Rule: Allow MySQL (Port 3306) from the RDS instance endpoint
Outbound Rule: Allow all traffic to any destination
Database Security Group:
Inbound Rule: Allow MySQL (Port 3306) from the web server security group
Outbound Rule: Allow all traffic to any destination  

### Question 22

Scenario: You are setting up an Amazon EC2 instance in AWS for hosting a web application. The application requires high availability, scalability, and the ability to distribute incoming traffic across multiple instances to ensure optimal performance and fault tolerance.
Based on the given scenario, which AWS service or feature would you use to achieve these requirements?

A. AWS CloudFront  
B. AWS Elastic Load Balancer (ELB)✔️  
C. AWS Auto Scaling  
D. AWS Virtual Private Cloud (VPC)  

### Question 23

Scenario: You are designing the network architecture for a company's cloud infrastructure on AWS. The company has multiple departments with different security requirements. The finance department deals with sensitive financial data and needs to be isolated from other departments. The development department needs access to external resources for software updates, but you want to restrict their access to specific approved sources only.
Based on the given scenario, which AWS service or feature would you use to meet these security requirements and ensure network isolation and controlled access?

A. AWS Virtual Private Cloud (VPC)✔️  
B. AWS Identity and Access Management (IAM)  
C. AWS Security Groups  
D. AWS Network Access Control Lists (ACLs)  

### Question 24

Scenario: You are working as a security administrator for a company that utilizes AWS services for their cloud infrastructure. The company has recently experienced a security breach due to unauthorized access to their AWS resources. To prevent such incidents in the future, you have been tasked with implementing strong security measures using AWS Identity and Access Management (IAM).
Based on the given scenario, which IAM feature or practice should be implemented to enhance security and prevent unauthorized access?

A. Monitoring and reviewing IAM user activity  
B. Implementing multi-factor authentication (MFA)  
C. Regularly rotating access keys and credentials  
D. Enforcing the principle of least privilege✔️  

### Question 25

You are the system administrator for a company's AWS environment, and you need to create an IAM policy to grant permissions for a specific task. Below is an example of an IAM policy. Can you decode it and identify the permissions granted?
Example IAM Policy:

```json
{
        "Version": "2012-10-17",
        "Statement": [
            {
                "Effect": "Allow",
                "Action": [
                    "s3:GetObject",
                    "s3:PutObject"
                ],
                "Resource": "arn:aws:s3:::example-bucket/*"
            },
            {
                "Effect": "Deny",
                "Action": "s3:DeleteObject",
                "Resource": "arn:aws:s3:::example-bucket/*"
            },
            {
                "Effect": "Allow",
                "Action": "s3:ListBucket",
                "Resource": "arn:aws:s3:::example-bucket"
            }
        ]
    }
```

Based on the provided IAM policy, what permissions are granted to the user?

A. Read, write, and delete objects in the "example-bucket" S3 bucket.  
B. Delete objects in the "example-bucket" S3 bucket, but cannot read or write objects.  
C. List the contents of the "example-bucket" S3 bucket, but cannot read, write, or delete objects.  
D. Read and write objects in the "example-bucket" S3 bucket, but cannot delete objects.✔️  

### Question 26

You are managing AWS IAM roles for a company's cloud infrastructure. Below is an example of an IAM role. Can you decode it and identify its configuration?

```text
Role Name: EC2S3AccessRole
    Assume Role Policy Document:
    {
    "Version": "2012-10-17",
    "Statement": [
        {
        "Effect": "Allow",
        "Principal": {
            "Service": "ec2.amazonaws.com"
        },
        "Action": "sts:AssumeRole"
        }
    ]
    }
    Permissions Attached: AmazonS3ReadOnlyAccess
```

Based on the provided IAM role, what can you infer about its configuration?

A. The role allows EC2 instances to assume this role and has full access to Amazon S3.  
B. The role allows users to assume this role and has read-only access to Amazon S3.  
C. The role allows EC2 instances to assume this role and has read-only access to Amazon S3.✔️  
D. The role allows users to assume this role and has full access to Amazon S3.  

### Question 27

Which of the following can be classified as log telemetry in terms of endpoint detection?

- A) Process execution logs
- B) Network traffic captures
- C) Memory dumps
- D) File system changes

Select the correct option:

A. A and B only  
B. B and C only  
C. A, C, and D only✔️  
D. All of the above  

### Question 28

Which of the following statements about the Windows Firewall is true?
A) It operates at the application layer of the TCP/IP stack.
B) It allows administrators to define security rules based on MAC addresses
C) It supports both inbound and outbound traffic filtering.
D) It provides protection against physical security threats.
Select the correct option:

A. A and B only  
B. B and C only  
C. C only✔️  
D. A, C, and D only  

### Question 29

Decode the values in the following Snort rule:
`alert tcp any any -> any any (msg:"LFI Attack Detected"; content:"GET"; content:".php?file="; sid:2001;)`

A. The rule triggers an alert for TCP traffic from any source IP and port to any destination IP and port.  
B. The rule triggers an alert for any protocol traffic from any source IP and port to any destination IP and port.  
C. The rule triggers an alert for TCP traffic from any source IP and port to any destination IP and port, with the payload containing "GET".  
D. The rule triggers an alert for TCP traffic from any source IP and port to any destination IP and port, with the payload containing ".php?file=".✔️  

### Question 30

A company recently experienced a data breach in which sensitive customer information was compromised. The breach has raised concerns about the effectiveness of the company's security measures. The security team is now implementing “osquery” to enhance their attack detection capabilities and strengthen their overall security posture.
Question:
In the given post-breach scenario, which osquery query can be used to identify potential signs of a persistent attacker on compromised devices?

A. `SELECT * FROM processes WHERE name = "malware.exe"`  
B. `SELECT * FROM users WHERE last_login > DATE_SUB(NOW(), INTERVAL 7 DAY)`  
C. `SELECT * FROM file WHERE path = "/var/log/audit.log" AND content LIKE "%suspicious_keyword%"`✔️  
D. `SELECT * FROM services WHERE state = "running" AND startup_mode != "auto"`  

## Disclaimer

This assessment is intended for educational use and authorized security training only. Do not use security tools, commands, or techniques against systems without permission.

---

*This document presents the questions and answer choices from the supplied source. It does not include an answer key.*
