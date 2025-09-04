# Snort IDS/IPS Configuration - Windows

This repository contains a **Windows-compatible Snort configuration file (`snort.conf`)**.  
It is tuned for monitoring and detecting intrusions on a Windows-based environment with simplified paths and enabled preprocessors.


##  Features

- Preconfigured for **Windows installation paths** `C:\Snort\...`  
- Custom **HOME_NET** variable set for local environment  
- Includes **all default Snort rule categories**  
- Enabled **preprocessors** for HTTP, DNS, SMTP, SSL, FTP, SIP, and more  
- Supports both **IDS (alert-only)** and **IPS (inline)** operation modes  
- Compatible with **Snort 2.x** on Windows  


##  Installation

1. **Download Snort for Windows**  
   ⦁ Get the latest version from: [***Snort***](https://www.snort.org/downloads)  
   ⦁ Install it in `C:\Snort\`

2. **Update rules**  
   ⦁ Place your updated rules under:  


     ```
     C:\Snort\rules\
     C:\Snort\so_rules\
     C:\Snort\preproc_rules\
     ```

4. **Replace the default configuration**  
   ⦁ Copy this repository’s `snort.conf` into:  

   ```
     C:\Snort\etc\snort.conf
   ```



##  Usage

Run Snort with the fixed configuration file:

```powershell
cd C:\Snort\bin
snort.exe -c "C:\Snort\etc\snort.conf" -i 1 -A console
