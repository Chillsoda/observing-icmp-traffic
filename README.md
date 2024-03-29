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

1.) At the Azure portal, go to your Windows 10 VM and copy its public IP address. 

2.) Open up a remote desktop connection or Microsoft Remote Desktop and paste the IP address where it asks. Next, you can just type in the username and password you created and login to the VM. 

3.) Once logged in, go to Edge and search for Wireshark. Go to it and download the Windows x64 version. Go to the installer and hit next until you download it. 

![Screen Shot 2024-03-02 at 7 18 35 PM](https://github.com/Chillsoda/observing-icmp-traffic/assets/161760771/7007979b-55a3-4071-bfa0-1480e65de106) 

4.) Open Wireshark and on the screen click where it says ethernet and then click the blue shark fin in the corner. Your screen should look like this. 

![Screen Shot 2024-03-02 at 7 31 42 PM](https://github.com/Chillsoda/observing-icmp-traffic/assets/161760771/ccf097c7-e064-4537-b8b0-c7c4b9482473) 

5.) On the line next to the blue bookmark, type ICMP to filter traffic by Internet Control Message Protocol. Notice there is no longer any traffic that is displayed. 

6.) On Azure, go to your Ubuntu VM, locate its private address, and copy it. On your Windows VM, open up the Powershell app and type: ping [IP address]. 

7.) Observe our Windows VM successfully pinged our Ubuntu VM and it's reflected both on Powershell and Wireshark. 

8.) Ping any public website by its domain name and watch for traffic. In my case, I pinged www.Google.com. 

![Screen Shot 2024-03-02 at 7 47 03 PM](https://github.com/Chillsoda/observing-icmp-traffic/assets/161760771/48f8e880-a3b4-4e66-bfbe-e1d8b71c2e82) 

9.) On Powershell create a perpetual ping by typing ping [IP Address] followed by -t. ICMP traffic should now flow perpetually. 

10.) On Azure go to your Ubuntu VM's Network Security Group, and click on inbound security rules. Click Add New Rule. Then, click on ICMP and set it to deny. Port ranges do not matter and set priority to 200. 

![Screen Shot 2024-03-02 at 7 53 45 PM](https://github.com/Chillsoda/observing-icmp-traffic/assets/161760771/96ac16a7-44ab-483a-b157-2d597eb17e63) 

11.) Notice how traffic stops on Wireshark and Powershell. To resume traffic, go back to Azure and delete the rule we just created. 

12.) Traffic is now restored and our two VMSs are now communicating again. Hit control-c to stop the pinging. 

FINISH





