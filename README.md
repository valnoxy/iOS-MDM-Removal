# How to remove MDM profile on iOS & iPadOS

This guide shows how to remove the MDM profile on iOS and iPadOS. 
> Important: If the device has been registered in Apple Business Manager, the MDM profile will be restored after a factory reset. 

## Tested devices
- iPhone 7 (iOS 15.5)
- iPhone 11 Pro (iOS 16.1)

---

## Requirements
- iMazing (or any other tool to modify iOS Backups)
- iOS / iPadOS backup

## Guide
### Creating a backup
1. Install iMazing
2. Connect your device and create a backup with iMazing
![iMazing creating a backup](assets/Step1.png)

### Edit the backup
3. Click on the top-right on ```iPhone Backups```, select your backup and click on ```Edit```.
![iMazing iPhone Backup list](assets/Step2.png)
4. Select your backup on the left panel and select ```File System```.
![iMazing iPhone List](assets/Step3.png)
5. Navigate to ```System Shared Containers -> SysSharedContainerDomain-systemgroup.com.apple.configurationprofiles -> Library -> ConfigurationProfiles```.
6. If exists, delete ```MDM.plist```, ```MDMEvents.plist``` & ```CloudConfigurationDetails.plist```.

### Restore backup
7. Right-click on the backup and select ```Restore this Backup to Device```.
![iMazing Restore backup](assets/Step5.png)
8. Set the restore options to default and start the restoration.


After the restore, the MDM profile should be removed from the device.

<hr>
<h6 align="center">© 2018 - 2023 valnoxy. All Rights Reserved. 
<br>
By Jonas Günner &lt;jonas@exploitox.de&gt;</h6>
<p align="center">
	<a href="https://github.com/valnoxy/Dive/blob/main/LICENSE"><img src="https://img.shields.io/static/v1.svg?style=for-the-badge&label=License&message=GNU%20GENERAL%20PUBLIC%20%20LICENSE&logoColor=d9e0ee&colorA=363a4f&colorB=b7bdf8"/></a>
</p