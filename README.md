# Ansible-Playbooks
A collection of useful Ansible playbooks and roles that I have created, modified, or used.

# Contributing
I am open to edits, having additional playbooks, and criticism. If you would like to edit, please follow the naming convention: system-verb-noun, such as tux-update-linux.yml for a playbook that updates Linux, or cent-update-httpd.yml for a playbook that only updates httpd on CentOS systems. Other than that, enjoy!

## Cloud

## Linux
### tux-install-dockerce.yml
This runs the neccessary commands to install docker-ce on a RedHat, Centos, Fedora, Debian, or Ubuntu system. Please note that this playbook presumes you are using systemd.
Credit where credit is due:
Some of the Ubuntu/Debian stuff I modified from [here.](http://clouds.freeideas.cz/subdom/clouds/2017/07/26/ansible-install-docker-ce/)

### tux-update-linux.yml
This updates linux on RedHat, CentOS, Fedora, Debian, or Ubuntu systems.

## Windows
### win-activate-windows.yml
This playbook accepts a variable, {{ activation-key }}, to activate Windows.

### win-configure-dnsalladapters.yml
This playbook accepts a variable, {{ dns-servers }}, to set the dns server for all adapters.

### win-create-directory.yml
This playbook accept a variable, {{ folder-path }}, to create a directory.

### win-disable-ieesc
This playbook uses the file located in Windows/files/win-disable-ieesc.ps1 to disable Internet Explorer Enhanced Security Configuration (IEESC) on a Windows Server. Please refer to the powershell script before running!

### win-disable-remoteuac.yml
This playbook disables remote uac via registry setting. This is useful when you have troubles using a vendor's remote session on a server.

### win-disable-windowsfirewall.yml
This playbook disables Windows Firewall for all profiles (domain, private, and public).

### win-enable-windowsfirewall.yml
This playbook enables Windows Firewall for all profiles (domain, private, and public).

### win-download-url.yml
This playbook accepts two variables, {{ file-url }} and {{ file-destination }}, to download a specified URL to a specified directory. This is intended for downloading files on Windows.

### win-enable-service.yml
This playbook accepts a variable, {{ service-name }}, and sets the specified service to autostart on boot and start immediately.

### win-install-software.yml
This playbook accepts a variable, {{ package }}, to use Chocolatey to install a package.

### win-install-windowsfeature.yml
This playbook accepts a variable, {{ win-feature }}, and installs the feature; rebooting if neccessary.

### win-join-windowsdomain.yml
This playbook accepts serveral variables, {{ domain }} {{ hostname }} {{ domainadmin }} {{ password }}. The {{ domain }} variable should be the FQDN of the AD domain you wish to join, the {{ hostname }} variable will set the target's name. The {{ domainadmin }} and {{ password }} variables are to specify the domain administrator account and password, which are required to join a domain.

### win-update-windows.yml
This playbook will download Windows Updates for all categories.

