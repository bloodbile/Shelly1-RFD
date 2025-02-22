# 🎀 Shelly1 RFD 🎀
## Overview
Recently, a reflected file download vulnerability was discovered in the web management panel of the Shelly1 Wi-Fi switch. The vulnerability was discovered in the 'Button switched ON URL' field under the 'I/O URL actions' tab. By entering a payload into this field, you are able to induce the device to send a request to the payload when the button is switched on. This behavior allows for the download of arbitrary files from external sources, potentially leading to further exploitation.
## Details
The vulnerability arises due to insufficient validation and sanitization of user-supplied input in the URL field. When a URL is entered, the device blindly follows the link and retrieves whatever content is being hosted at the specified location. This lack of input validation creates a significant security risk, as users are able to craft a payload to download and execute malicious files on the device/system. Successful exploitation could result in remote code execution, device compromise, or the distribution of malware within the network.

[![vid](https://github.com/user-attachments/assets/a84ec592-0c90-42a8-9bfd-85ba8306d9e6)](https://raw.githubusercontent.com/bloodbile/Shelly1-RFD/main/video.mp4)
