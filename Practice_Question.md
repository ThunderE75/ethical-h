## Set 1

1. INSTALL HTTPD WEB SERVER AND AN FTP SERVER ON A CENTOS MACHINE. OPEN PORTS IN THE FIREWALL. SCAN WITH NMAP AND FIND OPEN PORTS AND SERVICE VERSIONS AND OPERATING SYSTEM ALSO SCAN USING METASPLOIT AND DISPLAY OPEN PORTS.
2. PERFORM A DOS ATTACK ON THE WEBSERVER USING LOIC. DISPLAY CHANGE IN RESOURCE UTILIZATION BEFORE THE ATTACK AND AFTER THE ATTACK.
3. PERFORM A DOS ATTACK ON THE WEBSERVER USING HPING3 (ICMP AND TCP SYN).DISPLAY CHANGE IN RESOURCE UTILIZATION BEFORE THE ATTACK AND AFTER THE ATTACK.
4. Create a user by name Smith on the centos machine. Give password as pass12345. Use rockyou.txt and use hydra and perform attack on FTP server. Use Medussa and perform attack on SSH for the same user.
5. Close the Web server port in the firewall. Only FTP Server and SSH ports should be visible. Display the same using nmap. Now from Kali Linux create a SSH tunnel and access the internal website on CentOS on port 7200 on the Kali Linux IP address.
6. Create a file with a payload to provide reverse shell using msfvenom for Linux. Send this file to CentOS  machine. Execute and display the reverse shell created on the Kali Linux.
7. Capture the flag integrated inside the image using 2 images given. Use crypttool. Image names are clue1.jpg and cluse2.jpg. 
8. Create a user by name manager. Create PGP keys for the user. Share the key with the admin1 user. Create a file and encrypt it using manager public key. Display the file opens with manager user.
9. Create a exe file using msfvenom and use meterpreter payload. Send the file on the Windows VM. Execute the file. Display meterpreter session created on the Kali Linux VM. Take a screenshot of the windows VM. Try to display usernames and passwords of Windows VM. 


## Set 2

1. Install ftp server on a CentOS machine. Create 2 users by name soham and sneha. Provide 12345 as a password for soham user. Provide pass12345 as the password for sneha user. Install vsftpd package on the machine. Start the service. Open ports 20,21 and 30000-31000 in the firewall. From Kali Linux perform a password dictionary attack on FTP service using rockyou.txt file and display the passwords cracked for both the users. 
2. Keep all machines in NAT mode. From Kali Linux machine perform a Man-In-The-Middle attack. From CentOS VM access the http://info.cern.ch. Browse 1 or 2 pages. Display the traffic in the Wireshark on the Kali Linux machine.
3. On the CentOS machine allow only SSH connection in the firewall. On a terminal create a website using http.server python module. This website will run on port 7500. From Kali Linux machine create a SSH tunnel and access this website on Local Port 8500.
4. Convert the following Cipher text to plain text. `Emtkwum bw bpm ewztl wn Kzgxbwozixpg`
5. Create an exe file using msfvenom. Use the meterpreter payload. Send the file to a Windows machine. Execute and display the meterpreter session created on Kali Linux. Also take the screenshot of the Windows machine from within the meterpreter session.
6. Create a database by name csf. Create a table by name users inside this database. The fields inside this table will be Name,Age,City,Password. Add 3 entries in this table. Now modify the age of one of the user. Delete one of the user entry. Perform all the tasks using command line.
7. Scan your network and find out the live IP's. Find out 2 computers with maximum ports open. Find out the Operating system and Service versions on these computers.
8. Create a web server on a Windows. Open the task manager. From Kali Linux perform a DOS attack on the web server using Hping3 and LOIC and display the change in resource utilization.
