>[!summary]
>Setting up a Virtual Hard Disk (VHD) for first-time use involves multiple steps, from downloading the necessary files to configuring the development environment, including Hyper-V and Virtual Machine setup, and installing essential software for Dynamics 365 development.

#### Definitions
- VHD (Virtual Hard Disk): A file format representing a virtual hard disk drive that can encapsulate what is found on a physical hard disk drive, including disk partitions and a file system.

>[!info] Initial Setup Process

Locate and download the VHD files from the Asset library in Lifecycle Services. Use the IMPORT and Pick buttons to select and download the correct files for your version.

>[!bug] Hyper-V Configuration

Ensure Hyper-V is enabled on your system to run the VHD. This feature is essential for creating and running virtual machines on Windows.

>[!info] Setting Up the Virtual Machine

After downloading and assembling the VHD, configure a new virtual machine in Hyper-V. This includes defining memory, networking, and connecting the VHD file.

>[!tip] Development Environment Configuration

Post setup, install and configure key development tools such as Visual Studio and Microsoft SQL Server Management Studio to begin development and testing on Dynamics 365.

>[!attention] Resource Allocation

Consider the resource allocation for the VM, especially memory, as Dynamics 365 development environments can be resource-intensive.

>[!example] Comprehensive Setup Guide

1. **Download VHD**: Access Lifecycle Services, navigate to Asset library, and download the VHD files.
2. **Enable Hyper-V**: Activate Hyper-V features through Windows features settings.
3. **Create and Configure VM**:
   - Open Hyper-V, create a new VM, and attach the downloaded VHD.
   - Configure memory and network settings.
4. **Install Development Tools**:
   - Install Visual Studio and SQL Server Management Studio.
   - Configure these tools for your Dynamics 365 environment.
5. **Restore and Connect Database**:
   - If necessary, restore a database to the VM from a Production or Tier2 environment.
   - Connect to the database using SQL Server Management Studio for data querying.

>[!info] Enhancing Development Environment

After setting up the VHD and VM, explore additional tools like Microsoft Power BI Desktop and Insomnia for API management to enhance your development capabilities. Consider installing Microsoft Excel and other Office 365 applications for productivity and data management.