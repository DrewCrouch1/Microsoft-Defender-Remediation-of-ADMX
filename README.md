# Microsoft Defender Remediation of ADMX

## Executive Summary

This project demonstrates how **Microsoft Defender Vulnerability Management**, **Microsoft Intune**, and **administrative role activation through PIM** can be used to remediate an exposed application version through policy-based configuration management.

The lab focused on identifying a vulnerable version of **Google Chrome**, reviewing the associated exposure in Microsoft Defender, importing the appropriate ADMX templates into Intune, deploying a configuration profile to the affected device group, and validating that the exposure was remediated.

This project highlights practical skills in:

- vulnerability remediation
- Microsoft Defender security recommendations
- Intune configuration management
- ADMX template import and deployment
- least-privilege administration through PIM
- validation of remediation outcomes

---

## Environment

- Microsoft Defender Portal
- Microsoft Defender Vulnerability Management
- Microsoft Intune
- Microsoft Entra Privileged Identity Management (PIM)
- Windows Endpoint
- Google Chrome ADMX Templates

---

## Project Objectives

The objectives of this lab were to:

- identify a high-impact remediation opportunity in Microsoft Defender
- evaluate the security impact of a vulnerable application version
- request and execute remediation
- import and deploy updated ADMX-backed policy through Intune
- validate that the endpoint was no longer exposed after policy application

---

## Security Workflow Overview

This lab followed a structured remediation workflow:

1. Activate the required administrative role through PIM
2. Review Microsoft Defender remediation recommendations
3. Identify the most impactful vulnerability to remediate
4. Request remediation
5. Activate Intune administrative access
6. Download and import updated Google Chrome ADMX templates
7. Create a configuration profile from the imported template
8. Assign the profile to the affected device group
9. Sync the endpoint to apply policy
10. Verify the exposure was remediated

---

## 1. Activating the Security Administrator Role with PIM

Privileged Identity Management (PIM) was used to activate the **Security Administrator** role before making security-related changes.

This reflects a least-privilege administrative model by ensuring elevated access is used only when required.

<img width="1920" height="915" alt="Screenshot (75)" src="https://github.com/user-attachments/assets/2a140bc2-5a81-4254-b3f2-e953d7523fbe" />

<img width="1920" height="905" alt="Screenshot (76)" src="https://github.com/user-attachments/assets/65995970-c6d8-48d3-85eb-77ffbf4f741a" />

---

## 2. Reviewing Microsoft Defender Recommendations

After activating the appropriate role, the investigation moved into the Microsoft Defender portal to review recommended remediation actions.

<img width="1920" height="897" alt="Screenshot (77)" src="https://github.com/user-attachments/assets/f9ae32a7-4d37-4126-82f5-95c67b3713f4" />

The most impactful remediation opportunities were reviewed to determine which action would provide the greatest immediate security benefit.

<img width="1920" height="903" alt="Screenshot (78)" src="https://github.com/user-attachments/assets/12ba0400-4b21-427f-ad34-ba39d646da44" />

---

## 3. Identifying the Highest-Impact Remediation

The previously deployed version of **Google Chrome** was identified as the highest-priority remediation target due to multiple associated **High** and **Medium** severity CVEs.

Updating the browser version represented the most efficient way to reduce exposure and improve security posture.

<img width="1920" height="900" alt="Screenshot (79)" src="https://github.com/user-attachments/assets/cf81436b-bb13-4e57-b9ee-550c396f9857" />

---

## 4. Requesting Remediation

A remediation request was initiated through the Defender workflow.

This step demonstrates how Defender can be used not only to identify exposures, but also to operationalize remediation efforts across managed environments.

<img width="1920" height="909" alt="Screenshot (81)" src="https://github.com/user-attachments/assets/1b3d883d-fa1d-469b-bee4-05c54f34407d" />

<img width="1920" height="909" alt="Screenshot (82)" src="https://github.com/user-attachments/assets/2343dd69-4258-4170-8949-cbef5e109def" />

---

## 5. Activating the Intune Administrator Role with PIM

Because the remediation required endpoint policy changes, PIM was again used to activate the **Intune Administrator** role.

This reflects separation of duties and controlled elevation between security and device management tasks.

<img width="1920" height="897" alt="Screenshot (83)" src="https://github.com/user-attachments/assets/e2ef11e5-945c-4c80-a991-9f93801aae00" />

---

## 6. Downloading the Google Chrome ADMX Templates

To manage the application through policy, the updated **Google Chrome ADMX administrative templates** were downloaded.

These templates allow Intune to apply configuration and version-related policy settings in a structured way.

<img width="1920" height="965" alt="Screenshot (85)" src="https://github.com/user-attachments/assets/9dee10e0-fbce-4b7a-9162-b99d6c15cfe9" />

---

## 7. Navigating to Device Configuration in Intune

The remediation workflow then moved into **Device Configuration** within Intune, where imported administrative templates can be used to create and assign policy profiles.

<img width="1920" height="898" alt="Screenshot (86)" src="https://github.com/user-attachments/assets/ea1bc86d-ff41-493a-b4d7-0771b6d21790" />

<img width="1920" height="906" alt="Screenshot (87)" src="https://github.com/user-attachments/assets/47ae93d7-f23c-4446-9e24-d87436e9f898" />

---

## 8. Importing the ADMX Templates

The downloaded Google Chrome administrative templates were imported into Intune.

This enabled policy creation based on vendor-provided template settings rather than relying on manual configuration.

<img width="1920" height="902" alt="Screenshot (93)" src="https://github.com/user-attachments/assets/a1765a00-5e73-4ce1-a43f-cfad496355a2" />

<img width="1920" height="1080" alt="Screenshot (94)" src="https://github.com/user-attachments/assets/1eb9effe-c1a9-47eb-ae41-01a72396b816" />

---

## 9. Creating the Imported Template Profile

A configuration profile was created from the imported Chrome ADMX template to apply the required remediation settings.

This demonstrates how Intune can be used to standardize remediation actions across device groups.

<img width="1920" height="895" alt="Screenshot (95)" src="https://github.com/user-attachments/assets/5ec769a5-be9e-45d7-9e37-bfab0135370f" />

<img width="1920" height="905" alt="Screenshot (96)" src="https://github.com/user-attachments/assets/12b8634e-364b-46aa-b6d8-38a27ea6fefe" />

<img width="1920" height="905" alt="Screenshot (97)" src="https://github.com/user-attachments/assets/cf6a617b-b708-4ea7-b703-535ff2f61636" />

---

## 10. Assigning the Policy to the Affected Device Group

The profile was assigned to the affected device group so the remediation could be applied to the exposed endpoint population.

<img width="1920" height="915" alt="Screenshot (98)" src="https://github.com/user-attachments/assets/42b56b4a-2545-4c4d-90d6-68e988bdcd35" />

<img width="1920" height="908" alt="Screenshot (99)" src="https://github.com/user-attachments/assets/80c0ab8e-9a58-4c90-a480-6430128bbcea" />

---

## 11. Syncing the Endpoint

The endpoint **DC-Windows11-V** was manually synced to accelerate policy retrieval and application.

This step helps validate remediation more quickly in lab environments.

<img width="1920" height="909" alt="Screenshot (100)" src="https://github.com/user-attachments/assets/f3f8dc09-2fc9-40a8-bf36-28a407873923" />

---

## 12. Verifying the Exposure Was Remediated

After the policy was applied, verification was performed to confirm that the device was no longer reported as exposed in Microsoft Defender.

<img width="1920" height="904" alt="Screenshot (101)" src="https://github.com/user-attachments/assets/1cc42be8-7423-46f4-9012-8a848666a542" />

<img width="1920" height="910" alt="Screenshot (102)" src="https://github.com/user-attachments/assets/a1a294fd-7ebd-43a2-bddc-1251e4532232" />

An additional manual validation was performed through RDP to verify that the installed Google Chrome version had been updated. The screenshot for that validation was saved locally to the lab VM and was lost during environment cleanup.

---

## Outcome

This lab successfully demonstrated how Microsoft Defender and Intune can be used together to remediate an application exposure through policy-driven configuration management.

The vulnerable Chrome version was identified, prioritized, remediated, and validated as no longer exposed.

---

## Skills Demonstrated

- Microsoft Defender Vulnerability Management
- Security recommendation analysis
- Microsoft Intune configuration management
- ADMX template import and deployment
- Policy assignment and endpoint sync
- Security remediation validation
- Privileged Identity Management (PIM)
- Least-privilege administration

---

## Security Value

This project demonstrates practical cloud and endpoint security engineering skills relevant to Azure security roles, including:

- prioritizing remediation based on vulnerability impact
- translating Defender findings into operational fixes
- using Intune to apply standardized hardening actions
- validating remediation outcomes after deployment

---

## Future Improvements

Potential enhancements for this project:

- include CVE identifiers and severity details in a short remediation summary
- document the exact policy settings changed within the ADMX template
- add rollback considerations for production environments
- include a small “before vs. after” security posture summary

---

## Disclaimer

This project was performed in a lab environment for defensive security education and remediation practice.
