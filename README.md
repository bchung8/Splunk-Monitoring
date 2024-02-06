# Splunk-Monitoring
Splunk was utilized to analyze Windows server logs and Apache logs from the fictitious company Virtual Space Industry (VSI). Utilizing the capabilities of Splunk, numerous reports, alerts, and visualization dashboards were created. Logs from a fictional attack on the servers were also analyzed via Splunk.

## Prerequisites
To be able to complete the project the following is needed:

- Splunk
- [Sample Windows log files](Log_Files/windows_server_logs.csv)
- [Sample Apache log files](Log_Files/apache_logs.txt)
- [Attack Windows log files](Log_Files/windows_server_attack_logs.csv)
- [Attack Apache log files](Log_Files/apache_attack_logs.txt)

## Set-Up

To start the project the following needs to be accomplished.
1. Navigate to the Splunk directory inside the machine.
2. Inside the directory, start the splunk.sh script.
   ```
   sudo ./splunk.sh
   ```
3. Once the container is running, utilize any web client to access Splunk.
   ```
   http://localhost:8000
   ```
4. Use the appropriate credentials to log in to Splunk.

## Overview

In this scenario, you will be a SOC analyst at a small company called Virtual Space Industries (VSI). As a SOC analyst, you will utilize Splunk to monitor potential attacks on VSI Windows server logs and VSI Apache server logs. The Windows server is a back-end server that houses VSI's intellectual property. The Apache server is a front-end server used for VSI's public-facing website. The networking team at VSI has provided you with past logs from both servers to develop baselines, reports, alerts, and dashboards for a typical day.
- [Sample Windows log files](Log_Files/windows_server_logs.csv)
- [Sample Apache log files](Log_Files/apache_logs.txt)

Following the analysis of logs from a typical day, VSI experiences several security incidents. At this time, the networking team has provided you with logs from the attack. As a SOC analyst, you will utilize the baselines, reports, alerts, and dashboards developed earlier as monitoring solutions to identify what was attacked.
- [Attack Windows log files](Log_Files/windows_server_attack_logs.csv)
- [Attack Apache log files](Log_Files/apache_attack_logs.txt)

## Analysis of Windows Logs

### Uploading Sample Windows Logs
1. Navigate to the "Add Data" option within Splunk
2. Select the "Upload" option
3. Click on "Select File"
4. Upload [windows_server_logs.csv](Log_Files/windows_server_logs.csv)
5. On the "Set Source Type" select "Next"
   - No changes to the configuration are needed
6. On the "Input Settings" page:
   - Update the "Host" field value to "windows_server_logs"
   - Select "Review"
7. On the "Review" page, verify the correct settings.
8. Select "Submit" to upload the data to Splunk
9. The file will be successfully uploaded once the message "File has been uploaded successfully" appears.
10. Select "Start Searching"
11. **IMPORTANT**:For this project the time picker range must be set for "All Time"
    > Please note this is not the best practice when utilizing Splunk and only applies to this project.

### Developing Monitoring Solution

As a SOC analyst, these logs must be interpreted to determine which data fields are most important to monitor. 
