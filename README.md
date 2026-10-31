# Windows Failed Login Detection Using Wazuh SIEM

## Project Overview

This project demonstrates a security monitoring lab using Wazuh SIEM to detect failed Windows login attempts. A Windows 11 endpoint is connected to a Wazuh Manager running in Oracle VirtualBox. Windows Security Events are collected and analyzed to identify unsuccessful authentication attempts.

## Objectives

- Set up a Wazuh SIEM monitoring environment.
- Connect a Windows 11 endpoint using the Wazuh Agent.
- Monitor Windows failed login events.
- Identify authentication failures using Wazuh security rules.
- Develop a custom rule to detect repeated failed login attempts.

## Technologies Used

- Wazuh SIEM 4.14.6
- Windows 11
- Oracle VirtualBox
- Windows Security Event Logs
- XML (Wazuh custom rules)

## System Architecture

Windows 11 Endpoint → Wazuh Agent → Wazuh Manager → Wazuh Dashboard

## Implementation

1. Deployed the Wazuh virtual machine using Oracle VirtualBox.
2. Accessed the Wazuh Dashboard.
3. Installed and connected the Wazuh Agent on Windows 11.
4. Verified that the endpoint appeared as active.
5. Monitored Windows Security Event ID 4625.
6. Identified failed login alerts using built-in Wazuh rule ID 60122.
7. Added custom rule ID 100100 to detect repeated failed login attempts within a defined time window.

## Detection Results

The Wazuh Dashboard successfully displayed Windows authentication failure events with:

- Event ID: 4625
- Wazuh Rule ID: 60122
- Description: Logon Failure - Unknown user or bad password
- Severity Level: 5

The custom detection rule (100100) is currently under testing and has not yet been verified.

## Limitations

- The project currently focuses on Windows failed-login monitoring.
- The custom repeated-attempt detection rule requires further validation.
- The lab does not currently implement automatic account blocking or email notifications.

## Learning Outcomes

- Understanding SIEM architecture and security event monitoring.
- Working with Windows authentication logs.
- Configuring Wazuh agents and managers.
- Investigating security alerts.
- Learning custom detection rule configuration.

## Future Improvements

- Verify and refine the custom brute-force detection rule.
- Add more authentication-related detections.
- Explore alert notifications.
- Improve event investigation and reporting.

## Disclaimer

This project was developed for educational purposes in a controlled lab environment. Testing was performed on the author's own Windows system.
