# USRP-for-Windows
- Version : V3.10
- Updated Date : 2021.10.28
- Programmed by DS5QDR Lee, Hoenmin

# History
- 2021.10.31 V3.10 : fixed QRZ image download error and simplified
- 2021.10.09 V3.00 : [MACRO] command added to control DVSwitch Server
- 2021.09.23 V2.95 : [SERVER] section of usrp.ini has changed since V2.95 at as below
- 2021.03.24 V2.00 : support DVSwitch hUC (STFU, Intercom, ASL Mode) 
- 2021.01.04 V1.00 : USRP Client Released for Windows
- 2020.12.16 V0.95 : pyUC.py compiled to pyUC.exe

# How to setup
- download USRP-for-Windows-main.zip
- unzip
- edit usrp.ini
- run USRP.exe
- for more information, click https://ds5qdr-dv.tistory.com/224

# how to edit usrp.ini
- see : http://dvswitch.org/DVSwitch_install.pdf
- Appendix B: pyUC (python USRP Client)
![image](https://user-images.githubusercontent.com/64110724/134375327-b36d3c95-b887-4ac5-82a7-c5c620e5acfe.png)

# [SERVER] section of usrp.ini has changed since V2.95 at as below
- [SERVER] #server_name   : callsign :dmrid   : repeaterid  DDNS or IP address : USRP_rx/txport : usrp2dvs_port
- DVS_00 = DefaultDVS     : DS5QDR  : 4500495 : 450049599 : ds5qdr-dvs.iptime.org : 59595 : 61301 : 
- DVS_01 = DVS_SAMPLE     : DS5QDR  : 4500495 : 450049599 : ds5qdr-dvs.iptime.org : 59595 : 61301 : 
- DVS_NM = 4500495 : DS5QDR : Heonmin : Lee : Gimhae : KyungSang Nam-Do : Korea Republic of :
- If you use the version before V2.95, Please reconfigure the usrp.ini file.

# usrp2dvs (Option)
- install usrp2dvs by USRP program
- If you want to use full fucntion you have to install usrp2dvs program at your DVSwitch server
- to install, click 'Server' tab
- enter DVSwitch IP address, login ID and PW and then click 'install'
- After install, you must open portforwad UDP Port at your internet router.
- UDP Port is Analog_Bridge.ini [USRP] section tx/rxPort + 1 ex) tx/rxPort = 50000 UDP Port is 50001
-------------------------------------------------
- Manual installation at DVSwitch Server
- connect to your DVSwitch
- sudo git clone https://github.com/ds5qdr/USRP2DVS /opt/usrp2dvs
- sudo chmod +x /opt/usrp2dvs/usrp2dvs
- sudo chmod +x /opt/usrp2dvs/rc.local
- sudo mv /opt/usrp2dvs/rc.local /etc


Thanks,

DS5QDR Lee, Heonmin

![image](https://user-images.githubusercontent.com/64110724/134378644-46cd279f-4018-4164-9b87-ce7e21d3966a.png)

