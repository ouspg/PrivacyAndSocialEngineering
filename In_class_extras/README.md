# **In Class Extras**

Tasks in this directory are designed to be completed during the in person exercise sessions. All points awarded for these tasks are counted as bonus points, and therefore the max grade for the course can be achieved without completing these.

Tasks require equipment, security mechanisms and/or confirmations only provided during the exercise session.

You can complete these in any order you want.

Task #|Points|Description|
-----|:---:|-----------|
[Task 1](#lockpicking-1p) | 1 | Lockpicking
[Task 2](#wi-fi-deauthentication-password-attack-1p) | 1 | Wi-Fi Deauthentication password attack

## Lockpicking 1p.

#### The provided lockpicking set includes:

* Transparent practice locks with increasing difficulty:
    - A Padlock, the easiest lock of the set.
    - A Double-sided lock, one side slightly more difficult.
    - A Small cylindrical lock, tougher with a slightly obstructed view.
    - A Cruciform/Zeiss lock, toughest of the bunch. Picking this lock one pin at a time, the standard way will be time consuming.
* Lockpicks
* Turning tools
* Instruction booklet
* Keys (These will be removed beforehand)

#### The Task:

Basic one pin at a time picking let's you bypass many simple locks, for instance cabinets, drawers and simple padlocks. (Un)fortunately, it is not very likely to find door locks in Finland that are susceptible to single pin picking.

You are able to pick all of the locks using the regular one pin at a time tactic, for the cruciform this may take a very long time. We encourage you to test different picking styles and picks. Please ask for help if you get stuck.

**To complete** this task you are required to pick open 2 locks of your choice. You may pick the others as well, but 2 are required for a point.

## Wi-Fi deauthentication password attack 1p.

#### Requirements:

* Linux on HW or on a VM (preferably course VM)
* Provided monitor mode capable Wi-Fi adapter
    * Receive this after answering a couple of easy questions about the aircrack-ng suite

Wi-Fi deauthentication attack is a sort of DoS (denial-of-service) attack, where the attacker sends out deauthentication frames to devices connected to a certain AP (access point). When a device receives a deauthentication frame it will first be disconnected from the AP and then attempt to reconnect. 

This disconnection - reconnection traffic can be captured, and in our case, we will try to gain the password for the AP via a dictionary attack on the traffic. 

To receive the monitor mode capable adapter, you need to answer a couple of easy questions about the following:
* aircrack-ng, How to use a wordlist to perform the attack?
* aireplay-ng, How to use the deauthentication attack with aireplay-ng?
* airmon-ng, How to set an adapter to monitor mode?
* airodump-ng, How to specify a range of channels to monitor?
* wireshark, How to save a .pcap file?

You will get to know the basics of [aircrack-ng suite](https://www.aircrack-ng.org/documentation.html) and [wireshark](https://www.wireshark.org/docs/wsug_html_chunked/) in the context of wireless monitoring.

#### The Task

In this task you will perform a Wi-Fi deauthentication attack and carry out a dictionary attack on the recorded wireless traffic of the WLAN SSID "OUSPGTestNetwork". 

For the adapter to work remember to enable USB3 support on virtualbox and you need to install and enable the driver inside the VM:
* ```yay rtl88xxau-aircrack-dkms-git```
> [!NOTE]
> yay might not be installed,  
> ```sudo pacman -S go linux-headers base-devel make```  
> ```git clone https://aur.archlinux.org/yay.git```  
> ```cd yay```  
> ```makepkg -si```
* ```sudo vim /etc/modules-load.d/alfa-wifi.conf```
* Write "8812au" in the alfa-wifi.conf file. In vim press 'I' to to insert text, write "8812au", press esc and write ':wq'
* Can't see the adapter? Try ```sudo pacman -Syu linux linux-headers``` after this plug in the adapter again.

Remember to set it as the network adapter in virtualbox settings.

<details>
<summary><strong>Help</strong></summary>
<br>

<strong>Issues</strong>

> First debug step pull the adapter out and plug it back in

<strong>Commands that may be of use:</strong>

> lsusb

> iwconfig

<strong>Basic track for the task:</strong>

> Set the adapter to monitor mode, this requires killing interfering processes.  

> Start capturing 802.11 frames on the monitoring adapter, include atleast channels 1-170  

> Start capturing traffic with Wireshark,you can also see what's happening  

> Switch to capturing frames from the target BSSID on the targets channel with airodump-ng  

> Start sending deauths to the target BSSID   

> Wait. You should see a note 'EAPOL' marked for your target on airodump, after this you may stop airodump and deauthenticating. You may want to keep an eye on wireshark on the channel of your target aswell, you should see the different steps of EAPOL on it.  

> Stop and save Wireshark capture to a pcap file  

> Crack this file with a wordlist  
> You can install wordlists with ```sudo pacman -Syu wordlistctl``` With this tool you can ```wordlistctl fetch rockyou``` unpack the rockyou file and you can use it to crack the password  

</details>
