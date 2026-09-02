# Servers

---

### Strider:
- Configuration: 96 Cores(192 Threads) AMD Threadripper, 312 GB Memory, 2 x NVIDIA GPU - RTX 5000 32 GB Ada Gen.
- Rightnow the server is configured with dynamic ip but it doesnot change much.
- hostname: strider
- ipaddress: Provided in slack.
- You can configure the ip in your hosts file.
```
	- MacOS & Ubuntu: /etc/hosts
	- Add following line.
	- <ip address> strider
```
- You can check by pinging: ```ping strider```.

#### How to connect:

- Use ssh key authentication method to connect to the server. 
- Step 1: Install ssh in your local system and see you have the file id_rsa.pub in the location:
```
	- Windows: C:\Users\<username>/.ssh/id_rsa.pub
	- MacOS: /Users/<username>/.ssh/id_rsa.pub
	- Ubuntu: /home/<username>/.ssh/id_rsa.pub
```
- Step 2: Create a file authorized_keys in the .ssh folder.
- Step 3: Copy the content of the id_rsa.pub into authorized_keys.
- Step 4: Create a folder .ssh in your home directory in the server. First connect to the server using ssh with password.
```
	$mkdir /home/<user_name>/.ssh	
```
- Step 5: Upload the authorized_keys from your local system to the server at ```/home/<username>/.ssh```. It will ask for password.
```
	$scp authorized_keys <username>@<servername>:/home/<username>/.ssh
```

- Step 6: Now connect using command below. You should connect without requiring to give the password.
```
 $ssh <username>@<servername>
```

### Filezila
- Use Filezila application to upload or download files/folder to/from the server.

### Screen
- Use miniconda python environment.
- Use screen app to run your python programs.
- Always check for <b>memory leaks</b> in your code before running it in the server.

### HTOP
- Use htop app to monitor the resource utilization of your program.

<br><br>
<center><b><font color="red">THIS WEBSITE IS INTENDED EXCLUSIVELY FOR INTERNAL USE BY OUR TEAM.</font></b></center>
