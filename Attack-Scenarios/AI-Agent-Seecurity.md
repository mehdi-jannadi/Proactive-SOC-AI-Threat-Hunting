# AI Agent Monitoring and LLM Security Testing

## 1. Objective

The objective of this scenario is to extend traditional SOC monitoring to AI-powered systems by monitoring the behavior of an AI agent and evaluating its exposure to security risks.

The experiment focuses on integrating AI agent monitoring into the Wazuh infrastructure and testing selected security risks associated with Large Language Models (LLMs).

## 2. Lab Environment

The experiment was conducted using the following components:

- **Kali Linux:** Machine used to generate controlled test requests.
- **Ubuntu Server:** Hosts the AI agent and a Wazuh agent.
- **Flask:** Used to develop the AI agent and expose its application endpoint.
- **Wazuh Agent:** Collects the AI agent's application logs.
- **Wazuh Manager:** Analyzes the collected events and applies detection rules.
- **Wazuh Dashboard:** Provides alert visualization and investigation.

## 3. AI Agent Monitoring Architecture

The AI agent was developed using Flask and hosted on the Ubuntu Server.

To integrate its activity into the SOC monitoring infrastructure, application events were recorded in a dedicated log file:

`/var/log/ai-agent.log`

The Wazuh agent was configured to collect these application logs and forward them to the Wazuh Manager.

This integration allowed the SOC infrastructure to monitor security-related events generated during interactions with the AI agent, extending visibility beyond traditional operating system and network events.

## 4. LLM Security Testing

Several security tests were conducted to evaluate the AI agent's behavior against selected risks described in the OWASP Top 10 for LLM Applications.

The tested categories included:

| OWASP Category | Security Risk | Test Objective |
|---|---|---|
| LLM01 | Prompt Injection | Evaluate the agent's behavior when exposed to manipulated instructions. |
| LLM02 | Sensitive Information Disclosure | Examine whether the agent could disclose sensitive information. |
| LLM06 | Excessive Agency | Evaluate potentially unsafe actions or excessive permissions, including simulated command execution. |
| LLM07 | System Prompt Leakage | Test whether the agent could reveal information contained in its system instructions. |

These tests were performed in a controlled laboratory environment to generate security-related events and evaluate the monitoring mechanisms.

## 5. Detection and Monitoring

The AI agent's application logs were collected by the Wazuh agent and transmitted to the Wazuh Manager.

Custom detection logic was used to identify events associated with the tested LLM security risks.

The resulting alerts were made available through the Wazuh Dashboard, providing the SOC analyst with additional visibility into AI agent activity.

This approach demonstrates how application-level AI security events can be integrated into a centralized SOC monitoring workflow.

## 6. Results

**Detection Status: Successfully detected.**

The tested LLM security scenarios generated relevant events that were identified by the monitoring infrastructure.

The experiment demonstrated the feasibility of extending Wazuh monitoring to an AI agent by collecting its application logs and applying detection rules to security-related activities.

## 7. Evidence

Screenshots illustrating the AI agent monitoring and security tests can be found in the repository's `screenshots/` directory.

- AI agent application logs.
- Wazuh alerts associated with LLM01.
- Wazuh alerts associated with LLM02.
- Wazuh alerts associated with LLM06.
- Wazuh alerts associated with LLM07.


