# Design, Build, and Test Network Servers

## **Introduction**

Welcome to the **Design, Build, and Test Network Servers** project! This repository details the creation of a robust CentOS 7.9.2009-based network server. It includes server design, configuration, testing, and optimization, aimed at addressing operational inefficiencies, improving data security, and centralizing critical services.

---

## **Project Objectives**

1. **Server Deployment**: Set up a centralized server for file sharing, web hosting, and proxy services.  
2. **Security Enhancements**: Implement firewalls, ClamAV antivirus, and secure user authentication.  
3. **Data Protection**: Follow the 3-2-1 backup strategy for reliable disaster recovery.  
4. **System Monitoring**: Use automated tools to monitor performance and detect potential issues.  
5. **Documentation**: Provide clear, detailed documentation for seamless server management and scalability.  

---

## **Server Features**

### **1. File Sharing**  
Centralized file sharing is implemented using Samba, enabling fine-grained access control for different user groups.  
- **Directory Structure**:  
    ```plaintext
    /srv/PcointShare
        ├── Office Admin
        ├── Accounts
        └── HR
    ```
- **Key Features**:
  - ACL-based permissions for secure access.
  - Shared folders for departments with role-based access.
- **Configuration Snippet**:
    ```ini
    [PcointShare]
    path = /srv/PcointShare
    read only = no
    browsable = yes
    valid users = @grpaccounts, @grpofficeadmin
    write list = @grpofficeadmin
    ```

---

### **2. Web Hosting**  
The Apache HTTP server hosts Pcoint's website, ensuring reliable access and scalability.  
- **Setup Details**:
  - Website files are migrated to `/var/www/pcoint`.
  - Apache is configured to serve the website using the domain `www.pcoint.com`.
- **Configuration Snippet**:
    ```bash
    DocumentRoot "/var/www/pcoint"
    ServerName www.pcoint.com
    ```
- **Testing**:
  - Verify site accessibility through a browser.
  - Use benchmarking tools like Apache Bench to test server performance.

---

### **3. Backup Strategy**  
Data protection follows the **3-2-1 Rule**, ensuring three copies of data, two different storage types, and one offsite backup.  
- **Automated Backup Script**:
    ```bash
    #!/bin/bash
    tar -czf /backups/pcoint_$(date +%F).tar.gz /srv/PcointShare
    find /backups -type f -mtime +30 -delete
    ```
- **Schedule**:
  - Daily incremental backups.
  - Weekly full backups for comprehensive data safety.
- **Tools**:
  - Cron jobs to automate backup schedules.

---

### **4. Proxy and Security**  
Squid proxy and ClamAV are deployed to enhance security and control.  
- **Proxy**:
  - Squid enforces authenticated access to the internet.
  - Usage logging for audit and accountability.  
- **ClamAV**:
  - Configured to scan shared directories and incoming files for malware.  
  - Virus definitions updated regularly via `freshclam`.

---

## **Testing**

### **1. File Sharing**  
- Test user-specific access permissions on shared directories.  
- Confirm read/write access based on group assignments.

### **2. Web Hosting**  
- Verify that the website is accessible at `http://www.pcoint.com`.  
- Test page load times and server response using Apache Bench.  

### **3. Proxy**  
- Authenticate users through Squid and verify internet access.  
- Check logs for unauthorized access attempts.

---

## **Repository Structure**

```plaintext
📂 Design_Build_and_Test_Network_Servers
├── Configurations/
├── Scripts/
└── Documentation/
```

## **Lessons Learned**

1. **Configuration Management: Modularizing configurations reduces complexity and improves troubleshooting.**
2. **Linux Nuances: Understanding case sensitivity and system commands enhances server reliability.**
3. **Automation: Cron jobs and scripts simplify repetitive tasks, ensuring efficiency and consistency.**
4. **Documentation Importance: Clear documentation accelerates deployment and aids in future scalability.**
   
## **Conclusion**

This project demonstrates a structured approach to designing, configuring, and testing network servers. It highlights best practices for centralized services, robust security, and proactive monitoring. Use this repository as a guide to build efficient and secure server solutions tailored to your needs! Lets [dive in]() to the specifics for how this network server ticks! 
