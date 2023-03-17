# NPWD App for QB mail. Requires NPWD 1.5.0 or higher.

### Make sure you have OxMyql

## Install
1. Download the `npwd_qb_mail.zip` from releases. DO NOT CHANGE THE RESOURCE NAME. If you want to change it, you'll have to download the source code, alter `fetchNui.ts`, and build the project.
2. Run this sql:
```CREATE TABLE IF NOT EXISTS `player_mails` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `citizenid` varchar(50) DEFAULT NULL,
  `sender` varchar(50) DEFAULT NULL,
  `subject` varchar(50) DEFAULT NULL,
  `message` text DEFAULT NULL,
  `read` tinyint(4) DEFAULT 0,
  `mailid` int(11) DEFAULT NULL,
  `date` timestamp NULL DEFAULT current_timestamp(),
  `button` text DEFAULT NULL,
  PRIMARY KEY (`id`),
  KEY `citizenid` (`citizenid`)
) ENGINE=InnoDB AUTO_INCREMENT=1 DEFAULT CHARSET=utf8mb4;```
3. Unzip and add the resource to your server resources folder
4. Ensure `npwd_qb_mail` BEFORE `npwd`
5. Add app to NPWD config.json in the `apps` section `"apps": ["npwd_qb_mail"]`

## Preview
![cfc3409d1fb6ae8bda8ee48d895fe6ef](https://user-images.githubusercontent.com/97451137/184981884-8ea27d27-ba60-4cd1-8d10-5cf317d0ece1.png)
![e0df660cc00791170955c40c50fd5362](https://user-images.githubusercontent.com/97451137/184981899-2c3005e2-7857-44b8-b889-c3845b2f1cd0.png)
