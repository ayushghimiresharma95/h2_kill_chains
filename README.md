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

Kill chain analysis helps analysts understand and anticipate cyber intrusions by examining all phases of an attack, from delivery to exploitation. Instead of responding only after an exploit has occurred, defenders should analyze earlier stages to prevent future attacks. This approach helps identify and counteract the tools and methods attackers use, forcing them to constantly adapt.

Analyzing both successful and unsuccessful intrusions enables defenders to detect threats earlier in the kill chain and maintain a tactical advantage by staying ahead of adversaries. This proactive strategy improves resilience by anticipating and mitigating future threats.

## Campaign Analysis

Campaign analysis entails the temporal research of several cross-encroachment kill chains to establish resemblances and recurring characteristics across attacks, identifying them as part of a broader threat campaign. Defenders recognize these repetitive indicators and 
develop action plans in anticipation of future attacks.
This methodology aims to analyze the tactics, techniques, and procedures (TTPs) of adversaries, determining how a specific actor operates and what goals they pursue. This allows defenders to evaluate their defense posture, identify vulnerabilities, and strategically plan security measures to protect assets from ongoing threats.

# Installing Debian 12 (Bookworm) on VirtualBox

## 1. Install and Configure VirtualBox

### 1.1 Downloading VirtualBox

1. Visit the [VirtualBox website](https://www.virtualbox.org/).
2. Download the VirtualBox installer for your OS (Windows, macOS, or Linux).

### 1.2 Installing VirtualBox

1. Run the installer (`VirtualBox-<version>-Win.exe` for Windows).
2. Follow the setup wizard, keeping default settings.
3. Complete the installation and launch VirtualBox.

### 1.3 Configuring VirtualBox

1. Open VirtualBox and go to `File > Preferences`.
2. Verify default settings for general, input, and network options.

## 2. Set Up a Debian 12 Virtual Machine

### 2.1 Downloading the Debian 12 ISO

1. Visit the [Debian website](https://www.debian.org/).
2. Download the Debian 12 (Bookworm) "netinst" ISO for `amd64`.

### 2.2 Creating a New Virtual Machine

1. Click "New" in VirtualBox.
2. Name the VM `Debian 12 Bookworm`, set `Type: Linux` and `Version: Debian (64-bit)`.
3. Allocate `2048 MB` RAM and create a `20 GB` virtual hard disk (VDI, dynamically allocated).

### 2.3 Configuring VM Settings

1. Open VM settings:
   - System: Uncheck "Floppy", allocate `2 CPUs`.
   - Display: Set video memory to `128 MB`.
   - Storage: Add Debian ISO to the optical drive.
   - Network: Ensure "Adapter 1" is attached to "NAT".
2. Click "OK" to save settings.

## 3. Install Debian 12 (Bookworm)

### 3.1 Starting the Virtual Machine

1. Select the Debian VM and click "Start".
2. In the boot menu, select "Graphical Install".

### 3.2 Running the Debian Installer

1. Follow prompts to set language, location, and keyboard.
2. Configure network: Set hostname (`debian`), leave domain blank.
3. Set root and user passwords.

### 3.3 Partitioning the Disk

1. Select "Guided - use entire disk".
2. Choose the virtual disk and "All files in one partition".
3. Confirm and write changes to the disk.

### 3.4 Base System and Package Installation

1. Install the base system.
2. Configure package manager: Select a mirror and skip the proxy.
3. Install `Debian desktop environment` and `standard system utilities`.

### 3.5 Install GRUB Boot Loader

1. Install GRUB to the primary drive (`/dev/sda`).
2. Reboot after installation completes.

## 4. Post-Installation Steps

1. Log in with the user account.
2. Update the system:
   ```bash
   sudo apt update
   sudo apt upgrade -y

