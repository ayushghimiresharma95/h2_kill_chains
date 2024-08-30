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

Campaign analysis entails the temporal research of several cross-encroachment kill chains to establish resemblances and recurring characteristics across attacks, identifying them as part of a broader threat campaign. Defenders recognize these repetitive indicators and develop action plans in anticipation of future attacks.

This methodology aims to analyze the tactics, techniques, and procedures (TTPs) of adversaries, determining how a specific actor operates and what goals they pursue. This allows defenders to evaluate their defense posture, identify vulnerabilities, and strategically plan security measures to protect assets from ongoing threats.
