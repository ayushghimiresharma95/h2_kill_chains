## A New Class of Threats

A new class of threats, dubbed as “Advanced Persistent Threat” (APT), are trained and well-resourced adversaries that target highly sensitive economic, proprietary, or national security information by conducting multi-year intrusion campaigns.

## Flaws in Conventional Incident Response Methods

Conventional incident response methods fail to mitigate the risk posed by APTs because they make two flawed assumptions:
1. Response should happen after the point of compromise.
2. The compromise was the result of a fixable flaw.

## Intelligence-Driven Defense

The paper describes an intelligence-driven, threat-focused approach to study intrusions from the adversary's perspective. This intelligence-driven computer network defense (CND) model incorporates threat-specific intrusion analysis and defensive mitigations.

### Risk Management Approach

This defense is a risk management approach that addresses the threat component of risk, incorporating analysis of adversaries, their capabilities, objectives, doctrine, and limitations. It also represents a new intrusion kill chain model to analyze intrusions and drive defensive actions.

### Indicators of Intrusion

An indicator is any piece of information that objectively describes intrusions. Indicators are categorized as:
- **Atomic**: Cannot be divided further.
- **Computed**: Data involved in an incident.
- **Behavioral**: A collection of computed and atomic indicators.

Analyzing these indicators can lead to identifying new actions and states.

## Intrusion Kill Chain

A kill chain is a systematic process to target and engage an adversary to create desired effects. The steps in the kill chain process are:

1. **Reconnaissance**: Research and identification of targets.
2. **Weaponization**: Exploiting the deliverable payload.
3. **Delivery**: Transmission of the weapon to the targeted environment.
4. **Exploitation**: Targeting an application or operating system's vulnerability.
5. **Installation**: Installing the weapon on the victim.
6. **Command and Control**: Compromised hosts signal outbound to an internet controller server to establish a channel, allowing intruders "hands-on" access inside the environment.
7. **Actions on Objectives**: Collecting, encrypting, and extracting information from the victim.

## Course of Action

The intrusion kill chain model helps organizations enhance their cyber defenses by aligning their security measures with the steps adversaries take during attacks. By using a matrix of actions—detect, deny, disrupt, degrade, deceive, and destroy—defenders can employ various strategies, such as intrusion detection systems and vigilant user behavior, to counteract different attack phases.

The goal is to achieve resilience against persistent threats, including zero-day exploits. Rather than focusing solely on preventing zero-day attacks, organizations should use all available indicators to detect and mitigate repeated attacker tactics. This strategy increases the difficulty and cost for adversaries to succeed, improving the organization's overall defensive posture.

## Intrusion Reconstruction

Kill chain analysis gives analysts insight into cyber attacks by looking at every step, from how they start to how they work. Rather than just reacting after an attack happens, security teams should look at earlier parts to stop future attacks. This approach helps spot and fight back against the tools and methods hackers use making them always change their tactics. Looking at both attacks that work and those that don't lets security teams catch threats earlier in the kill chain. This keeps them one step ahead of the bad guys. This forward-thinking plan makes systems stronger by getting ready for and stopping future threats before they happen.

## Campaign Analysis

Campaign analysis entails the temporal research of several cross-encroachment kill chains to establish resemblances and recurring characteristics across attacks, identifying them as part of a broader threat campaign. Defenders recognize these repetitive indicators and 
develop action plans in anticipation of future attacks.
This methodology aims to analyze the tactics, techniques, and procedures (TTPs) of adversaries, determining how a specific actor operates and what goals they pursue. This allows defenders to evaluate their defense posture, identify vulnerabilities, and strategically plan security measures to protect assets from ongoing threats.

Technical Report: Installing Debian 12 (Bookworm) on VirtualBox
1. Installing and Configuring VirtualBox
1.1 Downloading VirtualBox
I visited the official VirtualBox website: https://www.virtualbox.org/.

I navigated to the "Downloads" section: This section provided download links for different operating systems, such as Windows, macOS, and Linux distributions.

I selected the appropriate version: I chose the VirtualBox version for my operating system. For this report, I used the Windows version. I clicked on the link for "Windows hosts" to download the installer.

1.2 Installing VirtualBox
I ran the installer: I navigated to the folder where the installer was downloaded and double-clicked on VirtualBox-<version>-Win.exe.

I followed the installation wizard:

I clicked "Next" to proceed through the initial setup screens.
I chose the default installation location and clicked "Next."
I left the default options selected for creating shortcuts and registering file associations.
I clicked "Next" again and then "Yes" to approve network interface warnings.
I clicked "Install" to start the installation process.
The installation completed: Once the installation was finished, I clicked "Finish" to exit the installer. VirtualBox was now installed on my system.

1.3 Configuring VirtualBox
I launched VirtualBox: I double-clicked the VirtualBox shortcut on my desktop.

I configured the default settings: I navigated to File > Preferences and checked the default settings for general, input, and network options. I did not need to make any changes for this installation.

2. Setting Up a Debian 12 Virtual Machine
2.1 Downloading the Debian 12 ISO
I visited the Debian website: https://www.debian.org/.

I navigated to the "Getting Debian" section: I clicked on "Download" to access the Debian images.

I selected the Debian 12 (Bookworm) ISO: I chose the "amd64" architecture (64-bit) and downloaded the "netinst" ISO file, which is a minimal installation image.

2.2 Creating a New Virtual Machine
I clicked "New" in VirtualBox: In the VirtualBox main window, I clicked the "New" button to start the VM creation process.

I named the virtual machine:

I entered Debian 12 Bookworm as the name.
I set the Type to Linux.
I set the Version to Debian (64-bit).
I allocated memory (RAM) for the VM:

I chose 2048 MB (2 GB) of RAM, which is sufficient for a basic Debian installation.
I created a virtual hard disk:

I selected "Create a virtual hard disk now" and clicked "Create."
I chose the "VDI (VirtualBox Disk Image)" option and clicked "Next."
I selected "Dynamically allocated" to save disk space and clicked "Next."
I set the disk size to 20 GB and clicked "Create."
2.3 Configuring Virtual Machine Settings
I opened the VM settings: I selected the newly created Debian 12 VM and clicked "Settings."

I configured the system settings:

I went to the "System" tab.
Under "Motherboard," I unchecked "Floppy" to speed up boot time.
Under "Processor," I allocated 2 CPUs for better performance.
I configured the display settings:

I navigated to the "Display" tab.
I increased "Video Memory" to 128 MB for better graphical performance.
I added the Debian ISO to the VM:

I went to the "Storage" tab.
Under "Controller: IDE," I clicked on the "Empty" optical drive.
I clicked the disk icon next to "Optical Drive" and chose "Choose a disk file."
I selected the downloaded Debian 12 ISO file.
I configured the network settings:

I navigated to the "Network" tab.
I ensured that "Adapter 1" was enabled and attached to "NAT" for basic internet access.
I saved the settings: I clicked "OK" to save the changes.

3. Installing Debian 12 (Bookworm) on the Virtual Machine
3.1 Starting the Virtual Machine
I started the VM: I selected the Debian 12 VM and clicked "Start."

The Debian installer booted: The VM booted from the Debian ISO, and the Debian installer screen appeared.

3.2 Running the Debian Installer
I selected "Graphical Install": Using the arrow keys, I selected "Graphical Install" and pressed Enter.

I chose the installation language: I selected English and clicked "Continue."

I selected my location: I chose United States and clicked "Continue."

I configured the keyboard: I selected American English and clicked "Continue."

The installer detected the network hardware: The installer loaded the necessary drivers for network hardware.

I configured the network:

I set the hostname to debian and clicked "Continue."
I left the domain name blank and clicked "Continue."
I set up users and passwords:

I set the root password and clicked "Continue."
I created a new user account (username: user) and set a password for it.
I configured the clock: I selected Eastern for the time zone and clicked "Continue."

3.3 Partitioning the Disks
I chose a partitioning method: I selected "Guided - use entire disk" and clicked "Continue."

I selected the virtual disk: I chose the virtual disk (20 GB) and clicked "Continue."

I selected the partition scheme: I chose "All files in one partition" for simplicity and clicked "Continue."

I confirmed the partitioning: I selected "Finish partitioning and write changes to disk" and clicked "Continue."

I confirmed writing changes: I selected "Yes" to write the changes to the disk and clicked "Continue."

3.4 Installing the Base System
The installer installed the base system: The Debian installer proceeded to install the base system packages.
3.5 Configuring the Package Manager
I selected a mirror for the package manager:

I selected United States as the archive mirror country.
I selected a default Debian mirror server (e.g., deb.debian.org) and clicked "Continue."
I opted not to use a proxy: I left the proxy information blank and clicked "Continue."

3.6 Installing Additional Software
I participated in the package usage survey: I chose "No" for the survey and clicked "Continue."

I selected additional software:

I selected Debian desktop environment and standard system utilities and clicked "Continue."
The installer proceeded to download and install the selected packages.
3.7 Installing the GRUB Boot Loader
I installed the GRUB boot loader:
I selected "Yes" to install the GRUB boot loader to the primary drive and clicked "Continue."
I confirmed the device (/dev/sda) for the boot loader installation.
3.8 Finishing the Installation
The installation completed: The Debian installer finished installing all components.

I rebooted the virtual machine: I clicked "Continue" to reboot the system and complete the installation.

4. Post-Installation Configuration
Debian 12 booted successfully: After rebooting, the Debian 12 login screen appeared.

I logged in with the user account: I used the credentials created during the installation (username: user).

I updated the system:

I opened the terminal and ran the following commands to update the package lists and upgrade all packages:
bash
Copy code
sudo apt update
sudo apt upgrade -y
The system was updated: The package manager updated all installed packages to their latest versions
