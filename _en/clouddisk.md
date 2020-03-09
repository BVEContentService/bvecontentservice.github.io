---
layout: page
title: Upload to Cloud Storage
---

TeraCloud is used as an example here. It is a high-capacity and region-compatible direct link cloud storage platform. Please let me know if you have a better alternative.

### Register an Account

Register an account at the [official website](https://teracloud.jp/en/).

It is worth noting that TeraCloud is not a shared storage service. Therefore password must be presented to BCS for players to download your files. So we recommend **not using a frequently-used password. Use a new, random one instead, and do not store personal file into the drive.**

### Prerequisite

1. (Optional) Although TeraCloud features an online file manager, using a WebDAV management software such as  [WinSCP](https://winscp.net/eng/download.php) might be more convenient. Installing as Commander is recommended.

2. The Public Source Server will generate metadata by itself, which is not a feature of a web drive. So you must download our metadata generator. Because of my laziness, it is written in PHP. Please download the newest `x64 Thread Safe`  or `x86 Thread Safe` version from [official website](https://windows.php.net/download) according to your computer. Extract it to `C:\php`. Please make sure `php.exe` is located at `C:\php\php.exe` .

3. Download the generator itself from [Github](https://github.com/BVEContentService/MetadataGenerator) , click that little green button and select `Download Zip`. Extract `metadata.php` and `metadata.bat` to the **parent folder** of that folder named after your email. For example:

   ```
   │  metadata.php
   │  metadata.bat
   │ 
   └─zbx1425.outlook.com
       │  author.ini
       │
       └─MTR Modified Initial System
               MTR Modified Initial System.html
               MTR Modified Initial System.png
               MTR Modified Initial System_1.0.ini
               MTR Modified Initial System_1.0_h2.zip
   ```

   This metadata generator might update. So please check for update regularly, in order to make use of newest features. The current latest version is:
   
   ![Latest Generator](https://img.shields.io/github/v/release/BVEContentService/MetadataGenerator?label=LatestGenerator&logo=github&style=for-the-badge)

### Generate Metadata

1. Run `metadata.bat`. You should see all your routes being listed, while a folder named index appears. This indicates that metadata has been generated.
2. **After any modification of the content, do not forget to run `metadata.bat` again to refresh the metadata. Then, use the files inside `index` to replace the associated file online.**
3. Note: You may find files like  `***.thumb.jpg`  in your folder. They are automatically generated, and automatically maintanced. Please leave them as-is. If you need to remove a route, just delete them alongside with other files that belongs to the associated route.

### Upload File

1. If you are using WinSCP, New Site. Use these configurations:
   * File Protocol: WebDAV
   * Encryption: TLS/SSL Implicit encryption
   * Host name: kita.teracloud.jp
   * Port number: 443 (Default)
   * Username and Password: You know better than me!
   * **Advanced->Directories->Remote Directory**: /dav
   
   If the speed is considerably slow or connection is not possible, try this reverse proxy:
   
   * Host name: teracloud.zbx1425.tk
   * Port number: 8953
   
2. Upload `index` and that folder named after your email to remote server. It should be kind of like this:

   ```
   Remote root directory
   │
   ├─index
   │      authors.json
   │      packs.json
   │
   └─zbx1425.outlook.com
       │  author.ini
       │
       └─MTR Modified Initial System
               MTR Modified Initial System.html
               MTR Modified Initial System.png
               MTR Modified Initial System_1.0.ini
               MTR Modified Initial System_1.0_h2.zip
   ```

   

   ![WinSCP Example](/assets/images/winscp_example.png)

### Submit Server

Your cloud drive must be submitted to our index before it can appear in the app.

1. Refer to [submit page](https://bvecontentservice.gitee.io/bcs-index/submission/) and fill in the information. The fields already filled in is the configurations for TeraCloud, and do not need to be changed if you are using this service.
2. We will check if your web drive is set up correctly. Please wait for our reply.

### See also

The commenting feature of this website is worth noticing. Please [check this out.](rssnotif.html)