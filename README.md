# GNS3 on Ubuntu for Network Simulations

## Introduction
This project documents my attempt to set up [GNS3](https://www.gns3.com/) on Ubuntu for network simulations. While the setup was not fully successful, this repository serves as a record of the process, challenges encountered, and lessons learned. I hope this documentation helps others who are embarking on similar projects.

## Objective
The goal of this project was to:
- Install and configure GNS3 on Ubuntu for simulating complex network setups.
- Set up the GNS3 virtual machine (VM) and integrate it with the local server.
- Troubleshoot common installation and configuration issues.

## Environment
- **Operating System**: Ubuntu 22.04 LTS
- **Tools**:
  - GNS3 (GUI and Server)
  - VMware Workstation 
- **Resources Consulted**:
  - [Official GNS3 Documentation](https://docs.gns3.com/)
  - Various community forums and tutorials.

## Steps Taken
### 1. Updating and Preparing the System
- Updated and upgraded the system:
  ```bash
  sudo apt update && sudo apt upgrade -y
  ```

### 2. Installing GNS3
- Added the official GNS3 PPA:
  ```bash
  sudo add-apt-repository ppa:gns3/ppa
  ```
- Installed GNS3 and related tools:
  ```bash
  sudo apt install gns3-gui gns3-server
  ```

### 3. Installing VMware Workstation Pro 
- Downloaded VMware Workstation Pro for hosting virtual appliances: 
  from https://support.broadcom.com/group/ecx/downloads
- Installed VMware Workstation Pro 
  ```bash
  sudo chmod +X VMware-Workstation-Full-17.6.3-24583834.x86_64.bundle
  sudo ./VMware-Workstation-Full-17.6.3-24583834.x86_64.bundle
  ```

### 4. Installing GNU Compiler Collection (GCC) (Required for Kernel Modification by VMware Workstation) 
  ``` bash 
  gcc --version
  sudo apt install gcc
  ``` 

### 4. Configuring GNS3
- Set up the GNS3 server using GNS3-GUI:
  ```bash
  gns3
  ```
- Attempted to connect GNS3 to the VMware Workstation 

### 5. Troubleshooting 
- Researched dependency conflicts and VM connectivity issues.

## Challenges Encountered
- **Dependency Conflicts**: Errors during installations due to mismatched dependencies.
- **VM Connectivity Issues**: Difficulty in connecting the GNS3-server to the GNS3-VM.
- **Server Errors**: GNS3-server and GNS3-VM not being on the same network or subnet 

## Lessons Learned
- The importance of checking compatibility between GNS3 versions and the host system.
- A deeper understanding of troubleshooting Ubuntu dependency issues. 
- The need for better preparation and familiarity with virtualization tools.

## Next Steps
- Plan to revisit the project with alternative approaches.
- Explore GNS3 on a Windows host to check for similar issues and solutions 
- Seek input from the GNS3 community and forums.

## How You Can Help
If you have experience with GNS3 on Ubuntu or have faced similar challenges, I would greatly appreciate your feedback or suggestions. Feel free to:
- Open an issue with your recommendations.
- Submit a pull request with fixes or alternative configurations.

## License
This project is licensed under the [MIT License](LICENSE).

## Acknowledgments
Special thanks to the GNS3 community and contributors for their extensive documentation and support resources.
