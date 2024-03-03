![image](https://github.com/Chillsoda/observing-icmp-traffic/assets/161760771/b21a6713-8741-42a2-844a-8ac4f381d943)

<h1> Observing ICMP traffic between two VMs</h1> 

We will now observe the traffic sent between the two virtual machines we created using a free packet analyzer called Wireshark. 

<h2> Requirements and Prerequisites </h2> 

1.) Two virtual machines that we created in Azure 

2.) Remote desktop command or Microsoft Remote Desktop for macOS users. 

3.) Wireshark 

<h2> Operating Systems used </h2> 

1.) Windows 10 

2.) Linux (Ubuntu) 

<h1> Instructions </h1>

1.) At the Azure portal, go to your Windows 10 VM and copy its IP address. 

2.) Open up a remote desktop connection or Microsoft Remote Desktop and paste the IP address where it asks. Next, you can just type in the username and password you created and login to the VM. 

3.) Once logged in, go to Edge and search for Wireshark. Go to it and download the Windows x64 version. Go to the installer and hit next until you download it. 

![Screen Shot 2024-03-02 at 7 18 35 PM](https://github.com/Chillsoda/observing-icmp-traffic/assets/161760771/7007979b-55a3-4071-bfa0-1480e65de106) 

4.) Open Wireshark and on the screen click where it says ethernet and then click the blue shark fin in the corner. Your screen should look like this. 

![Screen Shot 2024-03-02 at 7 31 42 PM](https://github.com/Chillsoda/observing-icmp-traffic/assets/161760771/ccf097c7-e064-4537-b8b0-c7c4b9482473)


