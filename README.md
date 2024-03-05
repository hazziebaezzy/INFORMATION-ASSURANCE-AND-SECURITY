# INFORMATION ASSURANCE AND SECURITY - FINAL PROJECT

 **Group 9 - BSCS 3A**
* Hazel A. Llorente
* Derick Emmanuel Marpuri
* Mariana Jane Ramos
* Ellyza Mae Periabras

## STEP-BY-STEP DOCUMENTATION

## 1. Prepare and Install Headless Raspbian OS in Raspberry Pi
* Download and Install Raspberry Pi Imager to a computer. Here is the link of [Raspberry Pi Imager](https://www.raspberrypi.com/software/).
![1 1](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/93c81343-e975-4a9a-802e-cbdd5cb7a9ee)
 ![1 1 1](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/c5e03a1e-f5c7-44c3-8dd9-4dfb536ec32b)

* After you install the Raspberry Pi Imager. Put the SD card you'll use with your Raspberry Pi into the reader and run Raspberry Pi Imager.
![1 2](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/2201f9d9-1432-4e5d-985b-f978c9346938)

* In this project, we choose ***Raspberry Pi 3*** for Raspberry Pi Device, ***Raspberry Pi OS (Legacy)*** for Operating System, and for storage choose your SD Card. And click **NEXT**.
![1 3](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/a015b2fb-0961-4ade-9031-6d571aff7ead)
![1 4](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/53d5f4ee-3f27-4e01-9292-8ab22754c123)
![1 5](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/6bbcab7e-0b2d-4fa5-97e4-7fed01b1484f)

* And after clicking **NEXT**, the OS Customisation will ask if you would like to apply OS customisation settings just click ***Edit Settings*** to customize the OS Settings.
![1 6](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/c5e72ce7-88fa-4949-9cc3-0594d3721d33)

* In the OS Customization, in _GENERAL_ we need to set hostname, username (_group9_) and password (_admin_). Also, set Configure wireless LAN the **CSPC BayanihanET** and set the wireless LAN country ro **PH** and set the locale settings then **SAVE**.
> [!NOTE]
> Do not change the password of the wireless LAN in your OS customisation.

![Screenshot 2023-12-10 161439](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/c3f16873-883f-49fb-885f-b35713ff26ad)

* Click _SERVICES_ to enable SSH and use password authentication, then **SAVE**.
![Screenshot 2023-12-10 161622](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/4c0baf89-ee79-4880-a7fa-d1b8a18f17a8)

* Click **YES** to apply our customisation setting.
![Screenshot 2023-12-10 161647](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/4a143d0c-845a-4290-9db3-107d5087b9b7)

> [!WARNING]
> If your SD Card has important existing files, make sure to backup all data to avoid deletion while formatting.
* A waring will appear that all existing data on your SD Card will be arased and asking if you want to continue for installation. Click **YES** to proceed since our SD Card have no existing files.
![Screenshot 2023-12-10 161709](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/1c2403d0-94db-4ea3-a611-9e9bf42ecbe3)

* Then the OS writing on your SD card will start and wait until the verification done to be write succesfylly. 
![Screenshot 2023-12-10 161736](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/8d6a747a-3754-4f47-a00b-2190c2395cac)


## 2. Connect to Raspberry Pi via SSH using the terminal then update the OS.
* Open command prompt and type the following command to update and upgrade:
  * ***ssh <username>@<hostname>***
    * Example: ssh group9@172.18.90.149
  ![1](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/4e76ce6c-7fa0-4fa6-b74a-eab50834c82f)

  * ***sudo  apt update***
  ![2 1](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/9e5fbaa0-0b92-461e-8acd-e2753e7c2f9b)

  * ***sudo apt upgrade***
  ![2 2](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/338d36ea-c535-41aa-afca-269eb02ad23d)

## 3. Deploying LAMP (Linux Apache MySQL PHP) Stack in raspberry Pi
* deploying a LAMP stack on a Raspberry Pi involves installing and configuring several software components:
  * ***sudo apt install apache2***
    ![3 1](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/18dcf34a-63a2-45db-9510-567a321136e2)
  * ***sudo apt install mariadb-server***
    ![10 1](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/6a45f0be-d826-4f50-b0d6-3d9ab454358c)
  * ***sudo mysql_secure_installation***
    ![14 1](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/397498d4-5656-4968-85f7-340e3d151e6d)
  * ***sudo apt install php libapache2-mod-php php-mysql***
    ![19](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/e1d0b56b-dfa0-4c28-863e-b07d3101997e)
  * ***sudo apt-get install php***
    ![25](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/6f9ba469-88af-4de6-9b4c-13c76d3ce1a8)
  * ***sudo apt install phpmyadmin***
    ![26](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/5c814df6-df77-4b1e-b892-73eb8abc017d)
  * ![30](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/05345bc8-71e2-489e-b947-66b81828e2ce)

## 4. Enabling and controlling Raspberry Pi using VNC.

  * Access the Raspberry Pi Configuration to enable VNC on the OS type ***sudo raspi-config*** command.
    ![39 1](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/e36a9268-20fa-4652-96d1-0968f61c2930)
  * Download and Install RealVNC on your windows. Here is the link [RealVNC](https://www.realvnc.com/en/connect/download/viewer/).
    ![33 1](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/957a18f9-a5b7-4e9d-966f-09ea47a9309b)

  * After the installation, proceed to the next step of configuring **VNC** follow the picture bellow:
    ![34](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/d1c627f4-6f1b-47ac-84d5-75a9423e1bd8)
    ![35](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/09e68589-1edb-4b67-91ce-74a72db161aa)
    ![36](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/6ceafad7-eec2-444d-a1ac-525d1d548f07)
    ![37](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/0bf208f9-d2b0-4b12-aa72-805677bfd102)
    ![38](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/49fb376b-f0dc-4ae8-9827-6446e6dbd6a7)

   * After that RealVNC Reviewer will open then type the ***IP Addreess***, And DONE!
     ![40 1](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/de8c6b75-79e2-45f1-a3c3-a7f02bb6ed50)
     ![41 1](https://github.com/ha-zee/INFORMATION-ASSURANCE-AND-SECURITY/assets/146160055/0e3ff8b1-a2e0-4047-9a32-51972a17b403)
