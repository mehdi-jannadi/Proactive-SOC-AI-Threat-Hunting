# Privilege Escalation Detection

## 1. Objective

The objective of this scenario is to evaluate the SOC's ability to monitor and detect suspicious activities related to privilege escalation within the monitored environment.

Privilege escalation occurs when an attacker attempts to obtain higher privileges than those initially available, potentially gaining administrative access to a system.

## 2. Lab Environment

The experiment was conducted in the virtualized SOC laboratory using:

- **Windows 10:** Monitored machine equipped with Sysmon and a Wazuh agent.
- **Wazuh Manager:** Centralized event analysis and detection.
- **Wazuh Dashboard:** Security event visualization and alert investigation.

## 3. Scenario Description

A privilege escalation scenario was executed against the monitored environment to generate security events associated with changes in user privileges and administrative access.

The experiment focused on identifying suspicious activities that could indicate an attempt to obtain elevated privileges.

## 4. Detection and Monitoring

The Wazuh agent collected relevant security events from the monitored machine and forwarded them to the Wazuh Manager.

Custom Wazuh detection rules were used to identify the suspicious activities associated with the tested scenario.

The generated alerts were then examined through the Wazuh Dashboard to assess the detection results.

## 5. Results

**Detection Status: Successfully detected.**

The experiment generated relevant security events that were detected by the SOC infrastructure.

This scenario demonstrated the ability to monitor suspicious privilege-related activities and provide alerts to support further investigation by the SOC analyst.

## 6. Evidence

Screenshots illustrating the experiment and its detection results can be found in the repository's `screenshots/` directory.

- Privilege escalation activity.
- Corresponding Wazuh detection alert.
- Relevant custom detection rule.


