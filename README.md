<h1>Azure Sentinel: Mapping Visualization of Live Cyber Attacks</h1>

# Project Overview:

This project encompasses setting up Azure Sentinel, a Security Information and Event Management (SIEM) solution, end-to-end. It involves connecting Azure Sentinel to a live virtual machine functioning as a honeypot to monitor and analyze global RDP brute force attacks. Additionally, a custom PowerShell script enhances the analysis by retrieving attackers' geolocation data and presenting it visually on the Azure Sentinel Map.

# Steps Involved in this Project

## 1. Azure Sentinel Workspace Setup
   * Created an Azure Sentinel workspace to centralize security data collection and analysis.
     
## 2. Honeypot Deployment
   * Deployed a virtual machine configured as a honeypot.
   * Enabled Remote Desktop Protocol (RDP) to attract potential attackers.
     
## 3. Data Integration
   * Configured Azure Sentinel to ingest data from the honeypot VM.
   * Integrate additional relevant data sources for a comprehensive security overview.
     
## 4. Security Rule Configuration
   * Define custom security rules in Azure Sentinel to detect potential RDP brute force attacks.
   * Set up alerts based on specific security events.
     
## 5. Enhanced Analysis with Geolocation
   * Develop a custom PowerShell script utilizing the ipgeolocation.io service.
   * Extract attacker information including country, city, and coordinates based on IP addresses.
     
## 6. Geolocation Visualization
   * Integrate the collected geolocation data into Azure Sentinel.
   * Configured Azure Sentinel's Map feature to visually display the locations of potential attackers.
     
## 7. Incident Response Planning
   * Establish clear procedures for responding to detected security incidents.
   * Define appropriate actions based on the severity of identified threats.

# Project Implementation in Detail

## 1. Creating the VM setup in Azure

  The project commenced with a critical initial step: the deployment of a purpose-built Windows Virtual Machine. This VM was meticulously configured to function as a honeypot, serving as a controlled bait system. By intentionally          enabling Remote Desktop Protocol (RDP), the VM was designed to appear vulnerable, thereby enticing potential cyber threats. This strategic setup creates an ideal environment for observing, analyzing, and documenting malicious            activities, forming the foundation of our proactive security monitoring efforts.

![image](https://github.com/karthikvimal98/Azure-Sentinel-Map-with-Live-CyberAttacks/assets/78943245/c4b1af15-b786-49bf-8780-81915e9081e6)

## 2. Creating a Log Analytics Workspace and Adding the Virtual Machine

  A key part of getting Azure Sentinel ready was making a Log Analytics workspace. This workspace acts like a big storage and analysis center. It collects and keeps all the important information created by different parts of the system,   including the virtual computer set up to attract and track potential attackers. Now that I have completed setting up the Log Analytics workspace and linked it to our trap computer, we're ready to move forward. The next steps involve     improving how we spot threats, creating smart ways to search through our data, and using all the log information we've gathered to get a full picture of our security setup in Azure Sentinel. This will help us better understand and       protect against potential cyber attacks.

![image](https://github.com/karthikvimal98/Azure-Sentinel-Map-with-Live-CyberAttacks/assets/78943245/6edff506-49e0-4ef3-ad82-7bf752ec63bf)

## 3. Integration of Geolocation Enrichment Using PowerShell Script

  This PowerShell script is designed to improve the analysis of failed RDP events by gathering and enhancing data with geolocation information. It continuously monitors the Windows Event Viewer, extracts details from failed RDP events,    performs IP geolocation lookups, and updates a custom log file. The script's output, which includes geolocation data, provides valuable insights into the origins of potential security threats. When integrated into Azure Sentinel         through Log Analytics workspace tables, this enriched data aids in more effective threat detection and response.

  ![azure_script_sentinel](https://github.com/karthikvimal98/Azure-Sentinel-Map-with-Live-CyberAttacks/assets/78943245/53226e4a-f634-4aa3-a258-56231b049b73)

## 4. Azure Monitor Agent to send logs

  To create custom logs in the Azure portal using the Log Analytics workspace, start by generating custom logs from the Failed RDP logs files on the VM. Proceed with Azure Monitor to create data collection endpoints, followed by setting   up Data Collection Rules based on the VM platform type, specifically Windows OS. Integrate these with the resource scope of the Log Analytics workspace and ensure all necessary information matches the VM details. After creating the      rules, add a datasource for the newly created data collection rule, then add the custom log table in the datasource. Finally, review and create the data collection rule, and check the data collection endpoint box when it is created      using the custom logs.
  
  <img align="left" width="100" height="100" src="![image](https://github.com/user-attachments/assets/ff60f03f-6c0a-478b-a705-92420b86a326)">
     

## 5. 
  
