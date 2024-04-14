# Forensic Investigation on Raw Memory Image

## Overview

This document outlines the forensic analysis conducted on a disk image seized from a suspected malware creator. The investigation employed various digital forensic tools and techniques to analyze the disk image, identify suspicious activities, and uncover hidden data within executable and encrypted files.

## Tools Used

- **Autopsy**: Used for initial analysis and identification of suspicious files on the disk image.
- **Wireshark**: Employed to capture and analyze network traffic associated with the executables identified in the disk image.
- **Veracrypt**: Used to decrypt encrypted files discovered during the investigation, specifically an MP3 file that was found to contain hidden data.

## Files Analyzed

1. **obiwan.exe** and **obiwan2.exe**
   - Executable files suspected of establishing remote connections and engaging in network communications with potentially malicious intent.

2. **not-the-droids-you-are-looking-for.mp3**
   - An encrypted MP3 file, decrypted using the key "r2d2" discovered during the analysis. It was found to contain sensitive data hidden within.

3. **final-form.exe**
   - An executable that was further analyzed for its network activity and behavior as it attempted to communicate with external servers.

## Analysis Process

### Initial Disk Image Examination
- The disk image was thoroughly analyzed using Autopsy to assess its content and identify areas of interest for detailed examination.

### Network Traffic Analysis
- Network interactions initiated by the executables were captured and analyzed using Wireshark to understand their nature and endpoints.

### File Decryption
- The encrypted MP3 file was decrypted using Veracrypt, revealing hidden contents that were crucial for further investigation.

### Detailed File Examination
- Each file was examined for its behavior, interaction with other system components, and network communication patterns.

## Key Findings

- Several executable files were making unauthorized server requests and establishing TCP connections to external systems.
- An encrypted MP3 file was used to covertly store and transmit sensitive information.
- Detailed examination of network traffic and decrypted contents revealed a complex scheme involving data exfiltration and potential malware activities.

## Recommendations

- Conduct further malware analysis using advanced tools to uncover any hidden functionalities.
- Investigate server interactions to trace back any potential command and control servers.
- Strengthen network security measures to prevent similar incidents in the future.

## Challenges Faced

- Dealing with robust encryption and continuous server redirection which complicated the analysis process.
- Managing and correlating a large volume of digital data across various formats.

## Conclusion

This investigation highlighted the importance of comprehensive digital forensic analysis in understanding and mitigating threats posed by sophisticated malware and encrypted files used in cyber attacks. The findings and recommendations provided in this report are intended to assist in enhancing security measures and preparing for future forensic investigations.
