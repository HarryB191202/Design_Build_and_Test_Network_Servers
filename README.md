# Design Build and Test Network Servers

## **Introduction**

Welcome to the **Design, Build, and Test Network Servers** project! This repository outlines the process of creating a centralized network server using CentOS 7.9.2009. It covers server design, setup, testing, and optimization to meet business needs efficiently.

---

## **Project Objectives**

1. Deploy a CentOS 7.9.2009 server for file sharing, web hosting, and proxy services.  
2. Centralize and secure network services (DNS, DHCP, FTP).  
3. Implement a 3-2-1 backup strategy for data protection.  
4. Optimize server performance and automate security updates.

---

## **Server Features**

### **File Sharing**  
- Configured shared directories with Samba.  
- Directory structure:  
    ```plaintext
    /srv/PcointShare
        ├── Office Admin
        ├── Accounts
        └── HR
    ```
- Example configuration:  
    ```ini
    [PcointShare]
    path = /srv/PcointShare
    read only = no
    browsable = yes
    valid users = @grpaccounts, @grpofficeadmin
    write list = @grpofficeadmin
    ```

### **Web Hosting**  
- Hosted Pcoint’s website on Apache HTTP server.  
- Example setup:  
    ```bash
    DocumentRoot "/var/www/pcoint"
    ServerName www.pcoint.com
    ```

### **Backup Strategy**  
- Automated backups following the 3-2-1 rule:  
    ```bash
    tar -czf /backups/pcoint_$(date +%F).tar.gz /srv/PcointShare
    find /backups -type f -mtime +30 -delete
    ```

### **Proxy and Security**  
- Squid configured for authenticated internet access.  
- ClamAV deployed for malware protection.

---

## **Testing**

1. **File Sharing**: Verify user-specific access permissions.  
2. **Web Hosting**: Ensure the website loads at `http://www.pcoint.com`.  
3. **Proxy**: Test Squid authentication for internet connectivity.  

---

## **Repository Structure**

```plaintext
📂 Design_Build_and_Test_Network_Servers
├── Configurations/
├── Scripts/
└── Documentation/
```

## **Lessons Learned**

1. **Modular configurations simplify management and troubleshooting.**
2. **Linux case sensitivity requires attention to detail.**
3. **Automation tools save time and improve reliability.**
   
## **Conclusion**

This project demonstrates how to efficiently design, configure, and test network servers. Use the repository to access scripts, configurations, and detailed documentation to build your own robust server solution! Lets [dive in]() to the specifics for how this network server ticks! 
