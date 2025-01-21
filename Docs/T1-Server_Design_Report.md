# Project Task 1: Server Design Report

## Introduction

### Role and responsibilities

A few roles and key responsibilities of my position in the information and communication technology (ICT) department at ITWorks include:

-   Comprehensive knowledge and experience surrounding IT infrastructure
    components, including cisco network and server equipment, data
    centres, security, IP telephony and windows 10 end user devices.

-   Demonstrated high level of experience in analysing technical issues
    on complex ICT systems and networks.

-   Demonstrated experience in undertaking ICT projects autonomously
    under limited supervision and contributing within a team
    environment.

-   Demonstrated ability to be proactive and improvement orientated,
    achieve goals, and deliver outcomes.

-   Demonstrated capability to research and solve problems within
    specific timeframes

-   Be a team player and have a customer service focused approach in
    your work

-   Contribute to the promotion and implementation of ITWorks principles
    and practices and in particular Equal Opportunity, Work Health and
    Safety by adhering to the provisions of various Acts and associated
    legislation.

-   Complying with policies and procedures when working for clients on
    projects at their premises.

Some key aspects of my role are that I am currently working for the network design team at ITWorks as a network administrator. I help support the ITWorks network, and I am required to complete server solution and implementation projects for clients

### Planning and implementation tasks

I will be implementing a new server solution for Pcoint- a vendor that specialises in the sale of computers and laptops. Pcoint would like to move their server model to an open-source solution for its file, print and website server. Pcoint has requested that I plan, design and implement the server solution for the Pcoint office administration team. 

Pcoint has also requested that at the end of the project, all components of the server configuration are to be documented and handed over to the administration manager Alicia Smith. I will thus be liaising with her during the project in order to obtain approval for the design and project sign off.

Pcoint has allocated a budget of \$5000.00 for this project and has already purchased a generic server. 

**The associated tasks with the planning and implementation of the server solution include:**

-   Migrating the business to an open-source server solution for its
    file, print and website server

-   Migrate the server to CentOS 7.9.2009

-   All components of the server configuration must be documented and
    handed over to the administration manager

-   Must liaise with Mrs. smith to obtain approval and project sign off.

-   Required to undergo a post implementation clean-up of the worksite,
    including any rubbish removal and movement of office furniture or
    ICT equipment.

**Including the resolution of the following inefficiencies:**

-   One Windows 10 workstation hosts the company website which is
    updated via a USB drive and provides some shared data and print
    services

-   Poor performance of the website is affecting productivity

-   There are no centrally managed network services (DNS, DHCP, FTP,
    NTP, mail, SMB, printing or web)

**No provision for:**

-   web caching or website filtering

-   user authentication or security for file management via
  directory services

-   monitoring of access or performance

-   regular schedule for updating services or applications

-   back up schedule

-   disaster recovery

---

## WHS and contractor responsibilities

### Induction completion

Below is an identified WHS induction badge that was received upon completion of the WHS induction:

![Imgur](https://imgur.com/q4BaAuA.png)

--- 

### WHS Hazards

Below are identified WHS hazards that were collated using the Business scenario document:

| Hazard                         | Risk Control Measure                                                                                                                                                        | Implementation                                                                                                                                                                               |  
| ------------------------------ | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |  
| Tripping hazard - stacks of A4 paper                | Eliminate the tripping hazard by moving these stacks of A4 paper to a safer location                                                                                        | Ensure or assess all walkways for other tripping hazards in order to prevent future injury from said hazards                                                            |
| Chained power leads            | Do not run leads and chain power leads as this could cause entanglement of power cords                                                                                      | Assess office cubicles and allow for easy access to all available power points in order to prevent this risk from occurring.                                                                 |  
| Excessive use of manual labour | Do not lift heavy loads without an understanding on safe manual labour practices, lifting heavy items could cause chronic injury if lifting practices are done incorrectly. | Train all staff on manual labour and encourage the promotion of safe manual labour techniques, including the dispersion of flyers, posters and infographics throughout the entire workplace. |  

## Installation and compatibility considerations

### Installation media

-   How will you obtain the CentOS V7.9.2009 installation files?

I will be obtaining the installation files for CentOS v7.2.2009 via the CentOS website, more specifically- [this URL](https://wiki.centos.org/Manuals/ReleaseNotes/CentOS7.2009). And also, [this URL](http://isoredirect.centos.org/centos/7/isos/x86_64/)

-   The media you will use for installation and two problems you might encounter in preparing or using the media during installation:

The media that I will be using for installation of the centOS operating system is DVD (.iso files downloaded off of the CentOS Website). Some problems that may be encountered with downloading centOS via .iso file include:

-   The .iso file might not download properly due to a poor internet
    connection.

-   The .iso file will not mount successfully due to a small data
    corruption. For example, if only a small section of data was not
    downloaded properly, the entire iso file will not be usable.

Some known issues with this version's installation include:

-   Corrupt file system -- SystemD will attempt a fsck. If the problem
    is too serious for an automatic fix, the user will be prompted to
    run fsck manually from an emergency shell.

-   Non-existent device/uuid referenced in /etc/fstab- system will wait
    for a set amount of time, waiting for the device to become
    available. If the device does not become available, the user is
    dropped to an emergency shell after the timeout.

### Installation contingencies

Below are installation contingencies as well as resources for getting assistance with CentOS V7.9.2009:


### Compatibility considerations
| Problem                                                    | Resolution                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Error message indicating no disks detected on boot**      | Could either be   an issue with the .iso file, or with anaconda. It is recommended that the   .iso file is re-downloaded using a more stable internet connection/ more   reliable website (websites such as official documentation- centOS etc.)                                                                                                    |
|                                                                |                                                                                                                                                                                                                                                                                                                                                   |
| **CentOS installation runs in low resolution or text mode**    | You can attempt   to perform the installation using the basic graphics driver. And then   reinstall the gui at a later date. To do this, either select Troubleshooting   > Install CentOS in basic graphics mode in the boot menu, or   edit the installation program’s boot options and   append inst.xdriver=vesa at the end of the command line. |
|                                                            |                                                                                                                                                                                                                                                                                                                                                     |
| **The GRUB2 boot loader is accidently deleted**             | You will have to   reinstall GRUB2 boot loader in order to have a graphical interface. Here are   the steps:                                                                                                                                                                                                                                        |
|                                                            |                                                                                                                                                                                                                                                                                                                                                     |
|                                                            | **Step-1   (Check the default location GRUB2 configuration files)**                                                                                                                                                                                                                                                                                  |
|                                                            | Code:   [root@techbrown ~]# rpm -qc grub2-tools                                                                                                                                                                                                                                                                                                     |
|                                                            |                                                                                                                                                                                                                                                                                                                                                     |
|                                                            | **Step-2   (Remove the Default GRUB2 configuration file)**                                                                                                                                                                                                                                                                                          |
|                                                            | Code:   [root@techbrown ~]# rm -rf /etc/default/grub                                                                                                                                                                                                                                                                                                |
|                                                            |                                                                                                                                                                                                                                                                                                                                                     |
|                                                            | **Step-3   (Remove the grub2-tools configuration files)**                                                                                                                                                                                                                                                                                             |
|                                                            | Code:   [root@techbrown ~]# rm -rf /etc/grub.d/*                                                                                                                                                                                                                                                                                                    |
|                                                            |                                                                                                                                                                                                                                                                                                                                                     |
|                                                            | **Step-4   (Reinstall the GRUB2 using yum command)**                                                                                                                                                                                                                                                                                                    |
|                                                            | Code:   [root@techbrown ~]# yum reinstall grub2-tools                                                                                                                                                                                                                                                                                               |
|                                                            |                                                                                                                                                                                                                                                                                                                                                     |
|                                                            | **Step-5   (Regenerate and save the GRUB2 configuration file)**                                                                                                                                                                                                                                                                                         |
|                                                            | Code:[root@techbrown   ~]# grub2-mkconfig -o /boot/grub2/grub.cfg                                                                                                   |
|                                                            |                                                                                                                                                                    |
| **A driver is causing the system not to boot**               | A malfunctioning  driver can prevent a system from booting normally during installation. When   this happens, you can disable (or blacklist) the driver by customizing the   boot command line.                                                                                                                                                    |
|                                                            |                                                                                                                                                                                                                                                                                                                                                     |
|                                                            | **Firstly, we will have to check if the module is loaded in the kernel:**                                                                                                                                                                                                                                                                            |
|                                                            |                                                                                                                                                                                                                                                                                                                                                     |
|                                                            | - Lsmod \| grep -I module_name (where module_name is replaced with our module that we want to   check)                                                                       |                                                                                                                                                                                                                                                                           |
|                                                            | - We then can disable this kernel module at runtime:                                                                                                                                                                                                                                                                                                  |
|                                                            | - Modprobe –remove module_name                                                                                                                                                                                                                                                                                                                        |
|                                                            |                                                                                                                                                                                                                                                                                                                                                     |
|                                                            | **Next, in order to blacklist this module, we have to create a new   file under /etc/modprobe.d:**                                                                                                                                                                                                                                                        |                   
|                                                            |                                                                                                                                                                                                                                                                                                                                                       | 
|                                                            | - Echo “blacklist module_name” >>   /etc/modprobe.d/module_name-blacklist.conf                                                                                                                                                                                                                                                                        |
|                                                            | - Echo “install module_name /bin/false” >>   /etc/modprobe.d/module_name-blacklist.conf                                                                                                                                                                                                                                                               |
|                                                            | - This basically causes /bin/false to be run instead of that module.                                                                                                                                                                                                                                                                                  |
|                                                            | - We next take a backup copy of initramfs:                                                                                                                                                                                                                                                                                                            |
|                                                            | - Cp /boot/initramfs-$(uname -r).img /boot/initramfs-$(uname   -r).img$(date +%m-%d-%H%M%S).bak                                                                                                                                                                                                                                                       |
|                                                            | - And then we rebuild initramfs:                                                                                                                                                                                                                                                                                                                      |
|                                                            | - Dracut –omit-drivers module_name -f                                                                                                                                                                                                                                                                                                                 |
|                                                            |                                                                                                                                                                                                                                                                                                                                                     |
|                                                            | **After this, we then update GRUB2 to blacklist the kernel module:**                                                                                                                                                                                                                                                                                   |
|                                                            |                                                                                                                                                                                                                                                                                                                                                     |
|                                                            | - Grep GRUB_CMDLINE_LINUX /etc/sysconfig/grub                                                                                                                                                                                                                                                                                                         |
|                                                            | - GRUB_CMDLINE_LINUX=”novga console=tty50,115200 rhgb quiet   console=tty0 rd.lvm.lv=rhel/root rd.lvm.lv=rhel/swap   blacklist_name.blacklist=1 rd.driver.blacklist=blacklist_name”                                                                                                                                                                   |
|                                                            | - We then rebuild the grub2 config files:                                                                                                                                                                                                                                                                                                             |
|                                                            | - Grub2-mkconfig -o /boot/grub2/grub.cfg                                                                                                                                                                                                                                                                                                              |
|                                                            | - And verify that the kernel module has been blacklisted:                                                                                                                                                                                                                                                                                             |
|                                                            | - Lsmod \| grep -I module_name                                                                                                                                                                                                                                                                                                                        |
|                                                            | - We should get a blank output, therefore the module has been blacklisted!                                                                                                                                                                                                                                                                          |   
|                                                            |                                                                                                                                                                                                                                                                                                                                                     |                 
|                                                            |                                                                                                                                                                                                                                                                                                                                                     |
| **Resources for getting help with   CentOS V7.9.2009**        |     
|                                                            |                                                                                                |
| Command line help available in the operating system itself | Commands such as   -help or manual pages such as man ls                                                                                                                                                                                                                                                                                             |
| Online help                                                | IRC Wiki article   , centOS mailing lists and forums |

--- 

1\.  Operating systems supported by both Microsoft IIS and Apache web
    server applications:

Microsoft IIS can only run on windows (windows server 2019, 2016, 2012
R2, 2012, 2008 R2, 2008, 2003 as well as windows 10, enterprise and
education, 10 pro, semi-annual channel, windows 8.1 and 7.)

whilst apache can run on Unix, Linux, MacOS, centOS and Windows
(windows 2000 or greater), though apache is best suited for Linux, it can run on windows too, meaning that Windows is the only operating system that can both support IIS and Apache web server



2\.  Some websites that give guidance through the process of migrating
    from IIS to Apache:

<https://www.mattwoodward.com/2010/02/25/moving-from-iis-to-apache-its-easier-than-you-think/>

<https://blog.afoolishmanifesto.com/posts/migrating-from-iis-to-apache/>

<https://www.slideshare.net/KurtBrust/suselinuxmigrationguideiistoapache>



3\.  Techniques to resolve the index file extension problem once you have
    migrated the Pcoint website from the Windows 10 PC:

Moving files from one server to another can be easy if you use Samba, an
open-source implementation of Microsoft's file sharing protocol.

-   You can migrate from IIS to apache using the konqurer application.
    To migrate from IIS to apache you have to:

-   Make sure file sharing is enabled on your windows server

-   On the linux server, log in as root

-   Temporarily grant access to the document root. Launch konsole and
    type-

-   Sudo chmod 777 /srv/www/server

-   Sudo mkdir /srv/www/serverhosts

-   Sudo chmod 777 /srv/www/serverhosts

(example directories used, you will replace those directories with the
location of your website files)

-   Use the built in graphical tools with konquerer to copy the files:

-   Click the desktop icon named network browsing and click on windows
    network. You should see a list of domains

-   Click on the domain of the server you are migrating from.

-   Click on the server you are migrating to.

-   Enter the user name and password of an administrative user

-   Open aanother konquerer window (control-N) and browse to the aapache
    document root location (/srv/www/websitedocs) for example.

-   At the windows server winddow, highlight the IIS folders that you
    shared and want to move and drag them over to /srv/www/websitedocs

-   At the popup menu that appears, select copy here.

---

## Data migration requirements

Data that needs to be migrated to the new server include the already
existing C:\\PcointShare file contents, including the file directory.
The file tree structure is as follows:

- \- Accounts

- C:\\ - Pcoint Share - HR

- \- Office Admin

Below is the file structure as a logical topology:

![Imgur](https://imgur.com/md6OjXz.png)

Allocated permissions are based on given prerequisites:

### Manager

- C:\\PcointShare\\Office Admin -- Read/Write

- C:\\PcointShare\\Accounts -- Read Only

- C:\\PcointShare\\HR -- Read only

### Office Administration

- C:\\PcointShare\\Office Admin -- Read/Write

- C:\\PcointShare\\Accounts -- Read Only

- C:\\PcointShare\\HR -- No access (may require access control list)

### Human Resources (HR)

- C:\\PcointShare\\Office Admin -- Read Only

- C:\\PcointShare\\Accounts -- No access (may require access control list)

- C:\\PcointShare\\HR -- read/write

And there is a location for website files that are required to be
migrated too. These website files are located at the directory
C:\\inetpub\\wwwroot\\pcoint

### Sub folders

- C:\\PcointShare\\Office Admin

- PcointShare\\Office Admin\\accountoverduetemplate.docx

- PcointShare\\Office Admin\\invoicetemplate.docx

- C:\\PcointShare\\Accounts

- PcointShare\\Accounts\\clientorders.xlsx

- PcointShare\\Accounts\\hardware inventory.xlsx

- C:\\PcointShare\\HR

- PcointShare\\hr\\employeerecords.accdb

- PcointShare\\hr\\payruns.xlsx

- C:\\inetpub\\wwwroot\\pcoint

-   inetpub\\wwwroot\\pcoint\\css

    -   inetpub\\wwwroot\\pcoint\\css\\animate.min.css

    -   inetpub\\wwwroot\\pcoint\\css\\bootstrap.min.css

    -   inetpub\\wwwroot\\pcoint\\css\\jquery.mCustomScrollbar.min.css

    -   inetpub\\wwwroot\\pcoint\\css\\jquery-ui.css

    -   inetpub\\wwwroot\\pcoint\\css\\meanmenu.css

    -   inetpub\\wwwroot\\pcoint\\css\\nice-select.css

    -   inetpub\\wwwroot\\pcoint\\css\\normalize.css

    -   inetpub\\wwwroot\\pcoint\\css\\owl.carousel.min.css

    -   inetpub\\wwwroot\\pcoint\\css\\responsive.css

    -   inetpub\\wwwroot\\pcoint\\css\\slick.css

    -   inetpub\\wwwroot\\pcoint\\css\\style.css

-   inetpub\\wwwroot\\pcoint\\images

    -   inetpub\\wwwroot\\pcoint\\images\\about_img.png

    -   inetpub\\wwwroot\\pcoint\\images\\leptop.png

    -   inetpub\\wwwroot\\pcoint\\images\\loading.png

    -   inetpub\\wwwroot\\pcoint\\images\\logo.png

    -   inetpub\\wwwroot\\pcoint\\images\\mane_img.png

    -   inetpub\\wwwroot\\pcoint\\images\\menu_icon.png

    -   inetpub\\wwwroot\\pcoint\\images\\te1.png

    -   inetpub\\wwwroot\\pcoint\\images\\te2.png

    -   inetpub\\wwwroot\\pcoint\\images\\top_img.png

-   inetpub\\wwwroot\\pcoint\\js

    -   intetpub\\wwwroot\\pcoint\\js\\boostrap.bundle.min.js

    -   intetpub\\wwwroot\\pcoint\\js\\custom.js

    -   intetpub\\wwwroot\\pcoint\\js\\jquery.mCustomScrollbar.contact.min.js

    -   intetpub\\wwwroot\\pcoint\\js\\jquery.min.js

    -   intetpub\\wwwroot\\pcoint\\js\\jquery.validate.js

    -   intetpub\\wwwroot\\pcoint\\js\\jquery-3.0.0.min.js

    -   intetpub\\wwwroot\\pcoint\\js\\plugin.js

    -   intetpub\\wwwroot\\pcoint\\js\\popper.min.js

-   i inetpub\\wwwroot\\pcoint\\index.html

### Installing NTFS-3G Drivers on CentOSv7.9.2009

As a requirement for migrating these files from windows to
CentOSv7.9.2009, it is required that the NTFS-3G driver be installed on
centOS in order for these file structures to be retained:

Step 1: update yum database using the following command- sudo yum
makecache

Step 2: after updating the yum database, we can install ntfs-3g using
yum by running the following command- sudo yum -y install ntfs-3g

Step 3: after we have installed ntfs-3g, we can now mount the ntfs
partition with this command- sudo mount /dev/sdb1 /mnt/ntfs-disk

Step 4: we have to make this mount permenant as centOS will not remount
this partition upon reboot. We have to edit the fstab file via nano
/etc/fstab and to add the following line (adding your own parameter)
/dev/sdb1 /mnt/ntfs-disk ntfs-3g rw,umask=0000,defaults 0 0

Step 5: then run this final command- mount /mnt/ntfs-disk

[Source](https://manjaro.site/how-to-enable-ntfs-support-on-centos-7/)
[Source](https://wiki.centos.org/TipsAndTricks/NTFS)

--- 

## User accounts and groups

### ICT User Account

An account for ICT Admin access to be created and used for managing user and directory access. All shared directories are to be owned using this account. Account naming = ictadmin

### User account naming convention

First five characters of the last name, and first two characters of first name e.g. john smith = smithjo

### Group naming conventions

Group names should be prefixed by grp followed by a meaningful that name that describes the group in lower case. e.g. grpadministration

### Password Requirements

Minimum of two days between password changes

Maximum of thirty days before password expiration

Seven days of warning

Five days of grace period before inactivation

Last change date should be current days date

Account expires in four years

Must adhere to the following password security requirements:

Between 8 to 16 characters in length

Must contain characters from at least three of the following four categories:

-   Lowercase characters (a-z)

-   Uppercase characters (A-Z)

-   Numerals (0-9)

-   Symbols, including: !@#\$%\^&\*-+=\[\]{}\|\\/:;'"\<\>()

---

### Group Permissions summary table 

| **Role**                   | **Groups** +   **permissions**                     | **User accounts**      | **Passwords**  |
|-------------------------|---------------------------------------------|--------------------|------------|
| **Manager**                 | -        Grpofficeadmin- read/write         | -          smithal | ^_1ZjyZ*5m |
|                         | -        Grpaccounts- read                  |                    |            |
|                         | -        Grphr- read                        |                    |            |
| **Office   Administration** | -        Grpofficeadmin- read/write         | kumraaa            | -c>+Rf1.f, |
|                         | -        Grpaccounts- read                  |                    |            |
|                         | -        Grphr- no permissions given        | makerpe            | cZ9~+-Y.9v |
|                         |                                             |                    |            |
|                         |                                             |                    |            |
| **Accounts**                | -        Grpofficeadmin- read               | pedrana            | }zrDf,Y^s7 |
|                         | -        Grpaccounts- read/write            |                    |            |
|                         | -        Grphr- no permissions given        |                    |            |
| **HR**                      | -        Grpofficeadmin- read               | stamojo            | *!u-H1}YqJ |
|                         | -        Grpaccounts- no permissions given  |                    |            |
|                         | -        Grphr- read/write                  |                    |            |
| **ICTADMIN**                | -        Grpofficeadmin- read/write/execute | Ictadmin           | z-8:#eFa4o |
|                         | -        Grpaccounts- read/write/execute    |                    |            |
|                         | -        Grphr- read/write/execute          |                    |            |
| **ROOT**                    |                                             |                    | ,_NXy7?bHL |

---

### File system format and partition layout

| File system format                	| Standard   partition, XFS file system                      	|
|-----------------------------------	|------------------------------------------------------------	|
| **Partition**                         	| Size                                                       	|
| **/boot**                             	| At least 1GiB                                              	|
| **/ (root)**                          	| At least 1 GiB                                             	|
|  **/srv/PcointShare/**                	| 29 GiB                                                     	|
|         -        PcointShare/Office Admin 	                                                            	|
|         -        PcointShare/Accounts     	                                                            	|
|         -        PcointShare/HR           	                                                            	|
|  |  |
| **Swap**                              	| 4GiB (mirroring   RAM)                                     	|
| **/var/www/**                       	| At least 10GiB   for apache web server and pending updates 	|
| **/home**                           	| 5GiB                                                       	|

---

The current location for content to be migrated at this time is:

C:\\PcointShare

-   C:\\PcointShare\\Office Admin

-   C:\\PcointShare\\HR

-   C:\\PcointShare\\Accounts

As well as the website files directory: C:\\inetpub\\wwwroot\\pcoint

These files will be migrated to the following directories:

Srv/PcointShare

-   PcointShare/Office Admin

-   PcointShare/Accounts

-   PcointShare/HR

As well as:

-   /var/www/inetpub/wwwroot/pcoint

The difference between file system formats is that the current file
system format structure is NTFS, whereas these files will need to be
reformatted to fit the standard partition/ xfs file format that centOS
uses.

---

### Shared directories and permissions

| Directory path              	| Owner    	| Permissions 	| Group owner    	| Permissions 	| Other permissions 	|
|-----------------------------	|----------	|-------------	|----------------	|-------------	|-------------------	|
| **/pcointshare/**               	| ictadmin 	| rwx         	| grpmanager     	| Rwx         	| ---               	|
| **/pcointshare/accounts**       	| ictadmin 	| rwx         	| grpaccounts    	| Rwx         	| ---               	|
| **/pcointshare/hr**           	| ictadmin 	| rwx         	| grphr          	| Rwx         	| --- (ACL)         	|
| **/pcointshare/office admin** 	| ictadmin 	| rwx         	| grpmanager     	| rwx         	| ---               	|
|                             	|          	|             	| grpofficeadmin 	| rwx         	|                   	|

---

### Shared printers

| Printer share name 	| Brand  	| Model          	|
|--------------------	|--------	|----------------	|
| **MainOffice1**        	| Ricoh  	| MP C2500       	|
| **MainOffice2**      	| Xerox  	| Phaser 3200MFP 	|

---

### The 3-2-1 backup strategy

The 3-2-1 backup strategy states that there should be 3 copies of your
data that is located on; at least two different media (either disk or
ssd or tape-based archiving media), and with one copy of your data
located at an offsite facility (cloud data storage etc.). this offsite
copy will be used for disaster recovery.

---

## Network services configuration

### Network interfaces

Two 1GB NICs (Leased line T1 0 1.544Mbs)
Network interface 1 = Host only -- 192.168.20.2

Network interface 2 = NAT -- DHCP

---

| Network Interface     	| IP address   configuration 	| Subnet mask   	|
|-----------------------	|----------------------------	|---------------	|
| Network interface one 	| 192.168.20.2               	| 255.255.255.0 	|
| Network interface two 	| DHCP                       	| 255.255.255.0 	|

---

### Network services configuration

| Network service                      	| Configuration   requirements                                                                                                                              	|
|--------------------------------------	|-----------------------------------------------------------------------------------------------------------------------------------------------------------	|
| **DNS domain name**                      	| HBpcoint.com                                                                                                                                              	|
|  |  |
| **DHCP subnet,   subnet mask and range** 	| DHCP Subnet:   192.168.20.0/24                                                                                                                            	|
|                                      	| Subnet Mask: 255.255.255.0                                                                                                                                	|
|                                      	| Range: 192.168.20.10-20                                                                                                                                   	|
|  |  |
| **Web server URL**                       	| www.HBpcoint.com                                                                                                                                          	|
|  |  |
| **Proxy server**                        	| Staff must   authenticate to access the internet through a web browser                                                                                    	|
|  |  |
| **SAMBA printer share**                  	| Printers must be   shared and accessible by Windows 10 PCs by way of sharing in Samba for the   pcoint workgroup.                                         	|
|  |  |
| **FTP**                                  	| Only the Website   administrator Alicia Smith is allowed access to upload files to the   server.  Access is only for the   location of the website files. 	|
|                                      	| A banner is also to be c onfigured warning the user about   unauthorised access.                                                                          	|
|                                      	|                                                                                                                                                           	|
| **Mail**                                 	| Mail transfer, delivery and user   agent to be installed and configured for pcoint domain.                                                                	|
|                                      	|                                                                                                                                                           	|
| **NTP**                                  	| Standard UTC  +9:30                                                                                                                                       	|
|  |  |
| **Firewall /   Security**                	| Only allow ports   open for network services required for the server                                                                                      	|
|                                      	| ClamAV is required for malware protection                                                                                                                 	|
|  |  |
| **System and application updates**       	| Configure   automatic updates of applications and operating system                                                                                        	|
|  |  |
| **System logs**                         	| Time   synchronisation and time zone configuration correct for current location                                                                           	|
|                                      	| All emergency messages to be automatically emailed to Alicia   Smith.                                                                                     	|
|                                      	| Monthly rotating of log files is to be configured.                                                                                                        	|
|                                      	|                                                                                                                                                           	|
|                                      	| Must include documentation for the following logs in final server   documentation:                                                                        	|
|                                      	| ·       system                                                                                                                                            	|
|                                      	| ·       security and authentication                                                                                                                       	|
|                                      	| ·       mail                                                                                                                                              	|
|                                      	| ·       web access                                                                                                                                        	|
|                                      	|                                                                                                                                                           	|
| **Performance   monitoring**             	| Server   performance monitoring tool/s must be installed                                                                                                  	|
|                                      	|                                                                                                                                                           	|
|                                      	| 100% of web server requests must be served under 40ms                                                                                                     	|
|                                      	|                                                                                                                                                           	|
|                                      	| Memory usage must not exceed 40%                                                                                                                          	|
|                                      	|                                                                                                                                                           	|
| **Backup**                              	| Configure and   implement backup service for the server with incremental backups daily after   business hours.                                            	|
|                                      	| Full server backups to be scheduled Friday every week after   business hours. Utilise the 3-2-1 backup strategy.                                          	|

--- 

## Design prototype

Here is a logical topology of the migrated
Pcoint Server after implementation:

![Imgur](https://imgur.com/75NxTpV.png)

--- 

## Testing plan

### ITWorks Test Plan

| Function                                                                                         	| Procedure                                                                                                                                                                    	| Expected results                                                                                                                	| Actual result 	| Comments 	|
|--------------------------------------------------------------------------------------------------	|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------	|---------------------------------------------------------------------------------------------------------------------------------	|---------------	|----------	|
| **Testing ACL/   Permissions for files for a single user (john stamos)**                            	| Log in to john   stamos’ account and test to see if john stamos’ account can access the office   admin file under PcointShare. Write and save a test.txt file in this folder 	| Successful access   to pcointshare/office admin/ folder, successful save attempt of test.txt file   in pcointshare/office admin 	|               	|          	|
|                                                                                                  	|                                                                                                                                                                              	|                                                                                                                                 	|               	|          	|
|                                                                                                  	| Test to see if other files that office admin are not can be   accessed under john stamos’ account. Try and safe a test.txt file in the   accounts folder.                    	|                                                                                                                                 	|               	|          	|
|                                                                                                  	|                                                                                                                                                                              	|                                                                                                                                 	|               	|          	|
|                                                                                                  	|                                                                                                                                                                              	| Successful access   to accounts file, unsuccessful access when trying to save test.txt in   /pcointshare/accounts               	|               	|          	|
|                                                                                                  	|                                                                                                                                                                              	|                                                                                                                                 	|               	|          	|
|                                                                                                  	|                                                                                                                                                                              	| Full denial of   access to HR folder.                                                                                           	|               	|          	|
| **Test that Alicia   smith can access permitted files on pcoint share**                             	| Log in as Alicia   smith                                                                                                                                                     	| Successful access   and append of test.txt file on    /pcointshare/office admin                                                 	|               	|          	|
|                                                                                                  	|                                                                                                                                                                              	|                                                                                                                                 	|               	|          	|
|                                                                                                  	| Attempt to access /pcointshare/office admin and create a text file   ‘test.txt’ on that directory                                                                            	|                                                                                                                                 	|               	|          	|
|                                                                                                  	|                                                                                                                                                                              	|                                                                                                                                 	|               	|          	|
|                                                                                                  	| Access accounts and HR files under /pcointshare/accounts                                                                                                                     	| Successful access   for both accounts and HR files under /pcointshare/                                                          	|               	|          	|
|                                                                                                  	| /pcointshare/HR                                                                                                                                                              	|                                                                                                                                 	|               	|          	|
|                                                                                                  	|                                                                                                                                                                              	|                                                                                                                                 	|               	|          	|
| **Access internet   through web proxy by testing authentication for a single user (john   stamos)**  	| Log in to John   stamos’ account and open the proxy (squidproxy), when prompted to log in,   enter john stamos’ details- username and password.                              	| Successful access to internet   after authentication through squidproxy                                                         	|               	|          	|
|                                                                                                  	|                                                                                                                                                                              	|                                                                                                                                 	|               	|          	|
|                                                                                                  	| Check for internet access before and after                                                                                                                                   	|                                                                                                                                 	|               	|          	|
| **Test that the   website loads**                                                                    	| Log in to Alicia   smiths account access the                                                                                                                                 	| Successful access   of the website                                                                                              	|               	|          	|
|                                                                                                  	|  website   www.HBserver1.pcoint.com                                                                                                                                          	|                                                                                                                                 	|               	|          	|
|                                                                                                  	|                                                                                                                                                                              	| Pinging website   IP returns  connection, refreshing the   website page is successful.                                          	|               	|          	|
|                                                                                                  	| Refresh the page and ping the websites IP                                                                                                                                    	|                                                                                                                                 	|               	|          	|

---

### Implementation plan and budget

|                  Item Number                  	|                                                                      Task/s                                                                     	| Estimated Time   for completion (hrs) 	| Service Type   & Down time (Disruptions) (hrs) 	|
|:---------------------------------------------:	|:-----------------------------------------------------------------------------------------------------------------------------------------------:	|:-------------------------------------:	|:----------------------------------------------:	|
| Stage 1: Planning                             	|                                                                                                                                                 	|                                       	|                                                	|
|                       1                       	| Creating   documentation                                                                                                                        	|                   2                   	|             Documentation – 0   HRS            	|
|                       2                       	| Conduct WHS   Assessment                                                                                                                        	|                   2                   	| Documentation – 0   HRS                        	|
| Stage 2: Server installation   preparation    	|                                                                                                                                                 	|                                       	|                                                	|
|                       1                       	| Obtain CentOS   v7.9.2009 install files                                                                                                         	|                  0.5                  	|              Installation- 0   HRS             	|
|                       2                       	| Backup the data   that needs to be migrated to the new server                                                                                   	|                   1                   	| Backup – 0 HRS                                 	|
| Stage 3: Server installation                  	|                                                                                                                                                 	|                                       	|                                                	|
|                       1                       	| Boot centOS   v7.9.2009 onto the pcoint server with the allocated file system and partition   layout.                                           	|                   1                   	|            Implementation –   0 HRS            	|
|                       2                       	| Set a root user password and   create an ictadmin account during the installation of the operating system.                                      	|                  0.25                 	|             Implementation – 0 HRS             	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
| Stage 4: Server configuration                 	|                                                                                                                                                 	|                                       	|                                                	|
|                       1                       	| Create the user   accounts and assign passwords as planned.                                                                                     	|                   1                   	|            Implementation –   0HRS             	|
|                       2                       	| Configure password aging on all   office administration accounts as per the Password Configuration   organisational requirements.               	|                   1                   	|              Implementation- 0 HRS             	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                       3                       	| Create the groups and add the   accounts as per Pcoints organisational requirements                                                             	|                   1                   	|             Implementation – 0 HRS             	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                       4                       	| Restore the Pcointshare data to   the /pcointshare partition and configure permissions as documented                                            	|                   1                   	|               Implementation – 0               	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                       5                       	| Configure network interfaces and   IP addresses for both interfaces                                                                             	|                   1                   	|             Implementation- 1 hour             	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                       6                       	| Install and configure the   printers.                                                                                                           	|                   1                   	|             Implementation – 2 HRS             	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                       7                       	| Update the operating system and   all application packages and configure updates to automatically install daily   including the kernel package. 	|                   1                   	|              Implementation- 3 HRS             	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                       8                       	| Install ClamAV on the pcoint   server and update the virus definitions database.                                                                	|                   1                   	|             Implementation – 4 HRS             	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                       9                       	| Configure the hostname and DNS   for the pcoint server and test connectivity.                                                                   	|                   1                   	|             Implementation – 5 HRS             	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
| Stage 5: Testing and benchmarking             	|                                                                                                                                                 	|                                       	|                                                	|
|                       1                       	| Perform allocated test   functions.                                                                                                             	|                   1                   	|              Implementation- 6 HRS             	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                       2                       	| Install Cockpit and Apache Bench   to monitor performance of system resources and the web server.                                               	|                   2                   	|              Implementation- 8 HRS             	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                       3                       	| Email to be   produced and sent to PCoint office manager Manager outlining the results of   benchmarking.                                       	|                   1                   	|             Documentation – 1   HRS            	|
|                       4                       	| Implement changes to   benchmarking.                                                                                                            	|                   1                   	|             Implementation- 9   HRS            	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|              Documentation – 1 HRS             	|
| Stage 6: Server configuration   documentation 	|                                                                                                                                                 	|                                       	|                                                	|
|                       1                       	| Review and submit finalised   report                                                                                                            	|                   1                   	|            Implementation –   10 HRS           	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|              Documentation – 1 HRS             	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
|                                               	|                                                                                                                                                 	|                                       	|                                                	|
| Stage 7: Post implementation                  	|                                                                                                                                                 	|                                       	|                                                	|
|                       1                       	| State contractor   responsibilities required before signing out of pcoint website                                                               	|                   1                   	|             Documentation – 1   HRS            	|
|                       2                       	| Conduct post   implementation clean-up of the Pcoint site, including wastage.                                                                   	|                   1                   	|             Documentation – 1   HRS            	|

---

## Cost Analysis

Below is the cost analysis for the project, the cost of the project is
within the budget of \$5000.00:

![Imgur](https://imgur.com/tLMXCsw.png)

## Communication strategy

It was discussed that there should be a proper communication strategy in
place for scenarios that encompass- server downtime, internet downtime,
server maintenance and other issues that may cause downtime for the
Pcoint server.

The strategy that will be implemented include contacting Pcoint
management- Alicia smith, and from there Alicia Smith is able to notify
all staff on the downtime as well as expected time of downtime/
disruption.

---

## Design approval

I hereby sign this document as approved, including server configuration
to be implemented, implementation plan, budget and cost benefit
analysis, and testing plan.

Harry Bournias
