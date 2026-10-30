# RDP Brute-Force Attack Detection

## 1. Objective

The objective of this scenario is to evaluate the SOC's ability to detect repeated authentication failures targeting the Remote Desktop Protocol (RDP) service.

A brute-force attack consists of repeatedly attempting authentication with different credentials in an effort to gain unauthorized access.

## 2. Lab Environment

The experiment was conducted using the following components:

- **Kali Linux:** Attacking machine used to simulate the brute-force scenario.
- **Windows 10:** Target machine equipped with Sysmon and a Wazuh agent, with RDP enabled.
- **Wazuh Manager:** Centralized event analysis and detection.
- **Wazuh Dashboard:** Security alert visualization and investigation.

## 3. Scenario Description

The experiment consisted of simulating repeated RDP authentication attempts against the Windows 10 target machine.

The test covered two important phases:

- **Failed authentication attempts:** Multiple unsuccessful login attempts were generated to simulate brute-force activity.
- **Successful authentication:** An RDP session was subsequently established during the experiment to observe the resulting authentication events.

This approach allowed us to examine both failed and successful authentication activity.

## 4. Detection and Monitoring

The Windows machine generated security events related to the RDP authentication attempts.

These events were collected by the Wazuh agent and forwarded to the Wazuh Manager, where the configured detection rules analyzed the activity.

The resulting alerts were visualized through the Wazuh Dashboard, allowing the SOC analyst to investigate the authentication attempts and identify suspicious activity.

## 5. Results

**Detection Status: Successfully detected.**

The experiment generated relevant alerts associated with the RDP brute-force activity.

The detection process demonstrated the ability of the SOC infrastructure to monitor repeated authentication failures and investigate the associated login activity.

## 6. Evidence

Screenshots illustrating the experiment and its detection results can be found in the repository's `screenshots/` directory.

- RDP authentication attempts.
- Wazuh alerts related to failed authentication.
- Successful RDP session and associated events, where available.
- Relevant custom detection rules.

