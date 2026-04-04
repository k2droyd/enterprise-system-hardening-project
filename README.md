# enterprise-system-hardening-project
Cybersecurity project simulating enterprise system hardening using CIS benchmarks

This project simulates a real-world post-acquisition security assessment, where a mid-size retail company acquires a competitor with outdated and inconsistent security practices.

As part of this project, I assumed the role of a Cybersecurity Analyst responsible for evaluating and recommending system hardening controls prior to merging the two environments.

🏢 Simulated Environment
The acquired company environment includes:
  Windows Server 2019
    - Active Directory Domain Controllers
  Windows 10 Endpoints
    - Mixed user roles (POS and non-POS users)
  Oracle Linux POS Infrastructure
    - 4 Linux servers running Oracle 11g databases
  Microsoft IIS Web Servers
    - Primarily internal (intranet-facing)


🎯 Project Objective:
The goal of this project was to develop a system hardening plan aligned with CIS Benchmarks to:
  - Reduce attack surface prior to network integration
  - Strengthen authentication and access controls
  - Improve logging and monitoring capabilities
  - Protect high-risk systems (e.g., POS infrastructure)


⚠️ Key Risks Identified
During this simulated assessment, several potential risks were identified:
  - Weak configurations enabling unauthorized access or lateral movement
  - Insufficient logging, limiting incident detection and response
  - Insecure services increasing exposure to internal and external threats
  - POS systems handling sensitive data without hardened controls



🛠️ Hardening Recommendations

Windows Server 2019 (Domain Controllers – Level 2)

  Control: Limit TCP Retransmissions
    
    - CIS Benchmark: 18.5.10 (Level 2)
    
    - Configuration: TcpMaxDataRetransmissions = 3
  
  Purpose within project:
   
    - Simulates reducing system strain during abnormal network conditions
    
    - Demonstrates awareness of availability-focused hardening controls

  
  Control: Enable Advanced Audit Policies
  
  Purpose within project:
  
    - Improves visibility into authentication events
    
    - Supports detection of suspicious activity in an enterprise environment

  
  Control: Restrict Administrative Privileges
  
  Purpose within project:
  
    - Applies least privilege principles
    
    - Reduces risk of credential abuse and privilege escalation


Microsoft IIS Web Servers (Level 1)
  
  Control: Configure Host-Based Firewall
  
  Purpose within project:
  
    - Demonstrates segmentation and traffic control
    
    - Limits unnecessary exposure of services

  
  Control: Enforce HTTPS (TLS 1.2+)
  
  Purpose within project:
    
    - Protects internal communications
    
    - Simulates secure web service configuration

  
  Control: Disable Unused Features (Directory Browsing)
  
  Purpose within project:
    - Reduces attack surface
    - Prevents unintended data exposure


Oracle Linux POS Servers (Level 2)
  
  Control: Enable auditd Logging
  
  Purpose within project:
  
    - Demonstrates implementation of system-level logging
    
    - Enables tracking of unauthorized access attempts

  
  Control: Disable Root SSH Login
  
  Purpose within project:
    
    - Enforces secure administrative access practices
    
    - Reduces risk of direct root compromise

  
  Control: File Integrity Monitoring (AIDE)
  
  Purpose within project:
   
    - Simulates detection of unauthorized system changes

    - Supports integrity validation of critical files


Windows 10 (POS Users – Level 2)

  
  Control: Restrict Printer Driver Installation
  
    - Setting: Enabled
  
  Purpose within project:
   
    - Demonstrates endpoint control enforcement
    
    - Reduces risk from unauthorized driver installations

  
  Control: Application Control (AppLocker)
  
  Purpose within project:
    
    - Simulates application whitelisting
    
    - Prevents execution of unauthorized software


Windows 10 (Non-POS Users – Level 1)
  
  Control: Minimum Password Length
   
    - Setting: 14+ characters
  
  Purpose within project:
    - Strengthens authentication security
    - Demonstrates implementation of baseline policies

  
  Control: Screen Lock Enforcement
  
  Purpose within project:
   
    - Reduces risk of unauthorized physical access
    
    - Applies standard endpoint security practices



  📊 Risk Prioritization

Domain Controllers

  Risk Level: Critical
 
  Priority: High


POS Infrastructure

  Risk Level: Critical
  
  Priority: High


Web Servers

  Risk Level: High
  
  Priority: High


Endpoints

  Risk Level: Medium
  
  Priority: Medium


