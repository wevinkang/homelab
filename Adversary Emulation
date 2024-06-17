Building an adversary emulation homelab for free with VirtualBox. 

1. Deploy Ubuntu VM.
2. Download and install Splunk enterprise onto Ubuntu VM.
3. Install docker then install Vectr (VECTR provides the ability to create assessment groups, which consist of a collection of Campaigns and supporting Test Cases to simulate adversary threats.)
4. Configure .env file for Vectr.
5. Start up the docker container to acess the Vectr web app.
6. Import atomic red team file (Atomic Red Team™ is library of tests mapped to the MITRE ATT&CK® framework.).
7. Deploy an addition Kali Linux VM.
8. Deploy sliver (Sliver is designed to be an open source alternative to Cobalt Strike.) and Caldera
(Caldera™ is a cybersecurity framework developed by MITRE that empowers cyber practitioners to save time, money, and energy through automated security assessments.) onto Kali.
10. Deploy Windows host
  Ran into a few problems here as I didn't have enough storage on my host device. Solved by getting an external hard drive to host the storage for the new Windows VM.
  Ran into a new problem because Windows 11 dev wasn't booting properly. Wasn't sure if this was an issue with my hard drive, but later determined it wasn't by deploying another linux VM
  on my external hard drive. Checked boot logs and eventually correlated the heartbeat failure error to a setting for the Windows VM display. In the display settings, changing the Graphics
  controller to VBoxVGA and disabling 3D acceleration solved the booting issue.
11. Configured sysmon on Windows host.
12. Configure Splunk universal forwarder to forward sysmon logs to the Splunk server.
  This also caused some issues, as when I ran into the previous problem. I had not touched this project for a few months and the Splunk enterprise license had expired. Splunk Free
  doesn't allow you to add forwarders and since I didn't want to upload csv files for data, I decided to choose a different SIEM - Wazuh.
13. Uninstall Splunk and install Wazuh.
14. Deploy the Wazuh agent onto the Windows host, check connectivity and logging.

