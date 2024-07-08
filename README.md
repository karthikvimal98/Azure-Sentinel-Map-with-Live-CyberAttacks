<h1>Azure Sentinel: Mapping Visualization of Live Cyber Attacks</h1>

**Project Overview:**
This project encompasses setting up Azure Sentinel, a Security Information and Event Management (SIEM) solution, end-to-end. It involves connecting Azure Sentinel to a live virtual machine functioning as a honeypot to monitor and analyze global RDP brute force attacks. Additionally, a custom PowerShell script enhances the analysis by retrieving attackers' geolocation data and presenting it visually on the Azure Sentinel Map.

<h2>Steps Involved in Project Implementation:</h2>
1. Azure Sentinel Workspace Setup
   * Created an Azure Sentinel workspace to centralize security data collection and analysis.
2. **Honeypot Deployment**
   * Deployed a virtual machine configured as a honeypot.
   * Enabled Remote Desktop Protocol (RDP) to attract potential attackers.
3. **Data Integration**
   * Configured Azure Sentinel to ingest data from the honeypot VM.
   * Integrate additional relevant data sources for a comprehensive security overview.
4. **Security Rule Configuration**
   * Define custom security rules in Azure Sentinel to detect potential RDP brute force attacks.
   * Set up alerts based on specific security events.
5. **Enhanced Analysis with Geolocation**
   * Develop a custom PowerShell script utilizing the ipgeolocation.io service.
   * Extract attacker information including country, city, and coordinates based on IP addresses.
6. **Geolocation Visualization**
   * Integrate the collected geolocation data into Azure Sentinel.
   * Configured Azure Sentinel's Map feature to visually display the locations of potential attackers.
7. **Incident Response Planning**
   * Establish clear procedures for responding to detected security incidents.
   * Define appropriate actions based on the severity of identified threats.

