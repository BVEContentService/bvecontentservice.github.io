---
layout: page
title: Prepare Files
navbar: "Upload"
---

Because a content service provides not only the file itself, but also informations and thumbnails about the route. So you need to prepare some metadata files, and match your route file with our required format.

Feel free to contact [zbx1425@outlook.com](mailto:zbx1425@outlook.com) if you have trouble following this tutorial. But we will not answer questions already explained in this document, so please **read this document carefully first.**

### Foreword

Some word off-course comes first. **Please do not overestimate the intelligence of a computer! **Computers are pretty dumb, so please follow this tutorial precisely, or something might not be working.

Although this article is pretty long, but the basic usage of BCS is not that complex as it seems. Only a part of the function described are necessery for uploading a route. Some advanced usages are also covered, which you can ignore if not required.

As I am not good at English, the descriptions might not be perfectly clear. So an example is given here for you to refer to if you cannot understand the folder structure described below.

In this case, someone with an email of 1234567890@qq.com uploaded three routes, which each has a thumbnail image and a TXT/HTML description.

```
1234567890.qq.com
│  author.ini
│
├─CSSSC-Guangzhou Metro Line 1
│      CSSSC-Guangzhou Metro Line 1_1.1.ini
│      CSSSC-Guangzhou Metro Line 1.txt
│      CSSSC-Guangzhou Metro Line 1.jpg
│      CSSSC-Guangzhou Metro Line 1_1.1_h2.zip
│
├─CSSSC-Pyongyang Metro CLM Line
│      CSSSC-Pyongyang Subway CLM Line_1.1_h2.zip
│      CSSSC-Pyongyang Subway CLM Line.html
│      CSSSC-Pyongyang Subway CLM Line.jpg
│      CSSSC-Pyongyang Subway CLM Line_1.1.ini
│
└─CSSSC-Guangzhou Metro Line 6
        CSSSC-Guangzhou Metro Line 6_2.0.ini
        CSSSC-Guangzhou Metro Line 6_2.0.txt
        CSSSC-Guangzhou Metro Line 6.jpg
        CSSSC-Guangzhou Metro Line 6_2.0_h2.zip
```

### Prerequisite

1. Create an empty folder at a location of your favor.
2. Create another folder inside this aforementioned folder with a name of your usable email. Please replace`@` to `.`, such as`zbx1425.outlook.com`.  
   All the following operations should be performed inside this folder.

### Fill in Personal Info

1. This step is only required to be done once.

2. **Please use [this tool](https://api.zbx1425.tk:8953/bcs-src/tool/authorini.html)** to prepare a file with your information. Hover your mouse over the textboxes and you can see some instructions. **Please leave "Description" empty. ** After filling in all the fields, please press "Submit" and you will get an `author.ini file, which can be put into the said folder. It must be put **directly inside the folder named after your email**, not inside its any subfolders.

   Some browser might suggest this file is malicious. I can promise this is not. And actually ini file only consists of data, not program code, so it is not possible to do harm to your computer. If you want to be cautious, feel free to perform a virus scan.

3. (Optional) You can write a piece of text to better describe yourself. Create `author.txt` besides `author.ini`, and write something inside. (Advanced) If you are familiar with HTML, you can create `author.html` to apply rich text, images and videos on your description page.

4. (Advanced) If you need to modify the ini file, you can refill the form online, or edit it manually. Please use **single-byte double quotation marks** on each side of your text, and please**make sure they match**. Because the windows notepad is not of rich functionality, Sublime Text or Notepad++ is recommended. Please use  `UTF-8` character encoding, and better `without BOM`.

### Fill in Route Info

author.ini must be placed inside the root directory, but the route information may be directly inside or inside any subfolder of the said folder named after your email.

1. **Please use [this tool](https://api.zbx1425.tk:8953/bcs-src/tool/authorini.html)** to prepare a file with your information. Hover your mouse over the textboxes and you can see some instructions.
   These are some items worth emphasizing:
   
   **ID must consist of only letters, numbers, dash `-`, BUT NOT UNDERSCORE `_` .**  
   This is the name displayed inside the menu of Hmmsim. Such as: `Tokyo Metro Tozai Line`, `CWTFSC-Beijing Metro Line 3`
   
   **Route version.** Many authors update their routes regularly, so the client features automatic updating, and will prompt the user to update their route. Only version numbers consists of number and dot are supported, **which should not contain letter or space.** For example, `3.6.1`. If the route you are uploading does not have a version number, or is not important, you can choose at your favor, but `1.0` or `0.0` is recommended.
   
   (Advanced) If you need to issue an update, after uploading the new route file, you can delete the files of the older version. Keeping them is also fine, since the newer route will take the position of the older one, which is only shown if "Show All Routes" is enabled in the settings.
   
2. Choose according to the genre of your route:

   #### If it is an original one:

   1. Fill in the informations correctly. Presenting a Homepage is recommended. It can be a page on your official website, or a page at a BBS, etc. **The Origin_LO, Origin_EN and Origin_SA should be left blank.**

   2. (Advanced) If you want the players to take a look at your homepage, you can tick "AutoOpen", so that your homepage will pop up once the download button is pressed. If you want to force your players read your homepage, you can tick "ForceView" and add a link pointing to `bcs://startDownload`, which will become the only way to start the download. *Caution: If you ticked "ForceView" without adding this link, then no one will be able to download the route.*

   3. (Advanced) You can use RouteObfuscator to shrink the size of your route, and make some trouble for the copyright violators.

   4. Choose according to the web drive you are using:

      - You are not using a web drive:  
        Uploading file is **REQUIRED** 

        Pretty appearant, isn't it?

      - The web drive does not allow downloading via browser (For example. a client is required):  
        Or for region compability (For example, you are using Google Drive, Dropbox, or Megaup):  
        Uploading file is **REQUIRED** 

        This drive is nearly useless. At least for someone in some country. Consider replacing, or upload to our server if you cannot find a nice alternative.

      - The web drive features direct link (Such as TeraCloud):  
        Uploading file is **NOT NECESSERY** 

        1. Fill in the url of the file into File_H2. 
        2. Set FileSize_H2 to the size of the file, such as "15.3MB".
        
      - The web drive has a web page, in which you click a button to start your download:  
     Uploading file is **NOT NECESSERY** 
      
        1. Fill in the url of the web page into File_H2. 
     2. Set FileSize_H2 to the size of the file, such as "15.3MB".
        3. Tick GuidedDownload.
        4. Consider adding some instruction for the users when writing description (Since the download button can be difficult to find for some web drives)

   #### If you are reposting work of others:

   1. **Fill in route information and original author information correctly**  
      **IT IS YOUR OBLIGATION TO DO THIS.**

   2. **Set Homepage to the page on which the original author releases his or her route** (i.e. Do Not just put the download page there, but the page with some words by the author. This is to give credit.)  
      Such as  `http://www.csssc.com.cn/lgz1.html`  
      **IT IS YOUR OBLIGATION TO DO THIS.** Admin team will remove your route if this is not correctly set up.

   3. **Beautify your description text**  
      A nice description can attract players.  
      And do not forget to be thankful to the original author.

   4. Choose according if you are authorized to repost this route:

   - If you are authorized by the author:  
     Automatic Installation is **POSSIBLE** 

     - If the original author has uploaded a Hmmsim route package:  
       Choose according to the web drive used by the author:
       - The web drive does not allow downloading via browser (For example. a client is required):  
         Or for region compability (For example, you are using Google Drive, Dropbox, or Megaup):   
         Uploading file is **REQUIRED** 
       - The web drive features direct link (Such as TeraCloud):  
         Uploading file is **NOT NECESSERY** 
         1. Fill in the url of the file into File_H2. 
         2. Set FileSize_H2 to the size of the file, such as "15.3MB".
       - The web drive has a web page, in which you click a button to start your download:  
         Uploading file is **NOT NECESSERY** 
         1. Fill in the url of the web page into File_H2. 
         2. Set FileSize_H2 to the size of the file, such as "15.3MB".
         3. Tick GuidedDownload.
         4. Consider adding some instruction for the users when writing description (Since the download button can be difficult to find for some web drives)
     - If only openBVE or BVE4 version is present:  
       Uploading file is **REQUIRED** 
       1. Use the Hmmsim Convertor to convert the route.
       2. (Advanced) You can use RouteObfuscator to shrink the size of your route, and make some trouble for the copyright violators.

   - If you are not authorized:  
     **If Hmmsim route package is not presented by the author, DO NOT follow these steps, since converting a route requires author's permission.**  
     Uploading file is **STRICTLY FORBIDDEN**  
     Choose according to the web drive used by the author:

     - The web drive allows downloading via browser (Direct link or web page):  
       Automatic Installation is **POSSIBLE** 

       1. Fill in the url of the web page **on which the author releases the route** (i.e. The Homepage. Do Not just put the download page there, but the page with some words by the author. This is to give credit.) into File_H2. 

       2. Set FileSize_H2 to the size of the file, such as "15.3MB".

       3. Tick GuidedDownload.

       4. Consider adding some instruction for the users when writing description (Since the download button can be difficult to find for some web drives)

     - The web drive does not allow downloading via browser (For example. a client is required):    
       Automatic Installation is **IMPOSSIBLE** 

       1. Tick NoFile
       2. Consider adding some instruction for the users when writing description.

3. **Leave the "Description" field empty.** Although it is not required, writing a piece of text will attract players and let them know about your route. Just like the `author.txt` above, both TXT and HTML are valid, and just place them right besides the ini file.

   **The filename should be identical to that of the ini file**, such as`MTR Modified Initial System_1.0.ini` -> `MTR Modified Initial System_1.0.txt`. As the description can be identical between versions, the version number can be omitted, which means  `MTR Modified Initial System_1.0.txt`  and  `MTR Modified Initial System.txt`  are both valid.  If both are present, the one with associating version number takes priority.  
   (Advanced) **Contents on external websites can also be used.** Just fill its url into the Description field.

4. (Optional) **Set a thumbnail.** Both jpg and png are accepted **(Extension should be in lowercase)**, and omitting version number is supported, such as `MTR Modified Initial System.png `. Just place it right besides the ini file. If it is not set, a default picture will be used.  
   (Advanced) **If external image storage is used**, You can set the Thumbnail field to the url of your file, such as  `https://openbve-project.net/images/logo.png` , while not putting any picture inside the directory.

   Important: The description file and thumbnail image must be in the **same directory** as the ini file, RIGHT besides it.

### Prepare to Upload the Files

If uploading a file is required as described before, please prepare all your zip route packages, and change the name of them properly so that the index program can handle them. Skip this step if uploading is not required.

Copy all your zip files and place them beside the associated ini file. The filename should be in this pattern:

```
[ID]_[Version]_[Program].zip
```

For "Program", `h2` is for Hmmsim2, `ob` is for openBVE, and `b5` is for BVE5. (ob and b5 are unfortunately currently not supported.) The letters should be lowercase. You can refer to the sample directory tree structure described at the start of this document. An example is:

```
MTR Modified Initial System_1.0_h2.zip
```

### Avoid Common Mistakes

These are some frequent mistakes. Please do a check in case you made one:

1. Unmatching file names  
   ID, Version and Program are three basic parts of BCS file names. Basically, ID and Version are included in INI, while Program is not. ID and optional, Version are included in JPG, PNG, TXT or HTML, while Program is not. All of these three are included in ZIP.

   ```
   XiJing Metro Line 3_1.0.ini
   WTFSC-XiJing Metro Line 3_1.0.jpg
   XiJing Metro Line 3 Beta ver 1.0.zip
   ```

   ↑ Naming must follow the pattern strictly, with no exception.

   ```
   XiJing Metro Line 3_1.0.ini
   XiJing Metro Lne 3.jpg
   XiJing Metro Line 3_1.0 .zip
   ```

   ↑ Is there any missing character or extra space? Spaces mislead the index program.

2. Folder structure  
   First of all, author.ini must be directly inside the folder named after your email, not outside and not inside a subfolder. Also, the BCS index program searches around the ini file, so just put your files beside it and they will get found.
   
```
   1234567890.qq.com
   ├─CSSSC-Guangzhou Metro Line 1
   │      author.ini
   │      CSSSC-Guangzhou Metro Line 1_1.1.ini
   │      CSSSC-Guangzhou Metro Line 1_1.1_h2.zip
   ```
   
↑ author.ini is not in correct position.
   
```
   1234567890.qq.com
   │ author.ini
   │ CSSSC-Guangzhou Metro Line 1_1.1.ini
   ├─CSSSC-Guangzhou Metro Line 1
   │      CSSSC-Guangzhou Metro Line 1_1.1_h2.zip
   ```
   
↑ zip is not along with ini, so it cannot be found.
   
```
   1234567890.qq.com
   │ author.ini
   │ CSSSC-Guangzhou Metro Line 1_1.1.ini
   │ CSSSC-Guangzhou Metro Line 1_1.1_h2.zip
   ```
   
↑ As long as ini and zip are together, the directory they are in does not matter. They can be directly in, or in any subfolder of the folder named after your email.

### What's next?

The Content Service System is not designed to be of only one server, since an individual server is not only limited, but also expensive. Maintaining such a server also exceeds my ability. So, we recommend you upload your routes to free, direct link storage services such as Pages, to distribute the load. These are some nice free services from the perspective of China:

| Name                             | File Size Limit | Repository Size Limit | Total Size Limit        |
| -------------------------------- | --------------- | --------------------- | ----------------------- |
| Gitee Pages                      | 100MB           | 500MB                 | 5GB per account         |
| TeraCloud                        | Unlimited       | Not divided           | 20GB per account        |
| **Tianjin Public Source Server** | 1000MB          | Not divided           | 58GB shared by everyone |

Overall speaking, Gitee Pages works fine, but the single file size limit is quite strict. Teracloud is also nice, but the download speed is poor in some regions of China, please see if it is acceptable via reverse proxy (See TeraCloud uploading document for detail). If these are not available, you can choose to use our Public Source Server. But if you want to save effort, Public Source Server is the easiest to use.

Also, we are currently short of storage spaces. if you host a server and are willing to help, please let us know! Hooking up one will not be difficult, just a 24 hour running computer, a Raspberry Pi, or even modifing your router will do the job.

Please choose a manual according to your selection:

* [Upload to TeraCloud or other direct link web drive](clouddisk.html)
* [Upload to Public Source Server](publicsrc.html)
* Upload to Pages or other git services