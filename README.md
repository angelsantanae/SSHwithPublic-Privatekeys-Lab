<h1>SSH with Public and Private Keys</h1>

 

<h2>Description</h2>
In this lab I was aiming to logging in to a system with public/private keys versus a password. the point was to show how SSH key relies upon the use of two related but asymmetric keys, a public key and a private key, that together create a key pair that is used as the secure access credential.




<br />


<h2>Languages and Utilities Used</h2>

- <b>Kali Linux VM</b> 
- <b>Linux Terminal</b>

<h2>Environments Used </h2>

- <b>Kali Linux 2024.3</b> 

<h2>Project walk-through:</h2>

<p align="center">
Starting SSH daemon and try to make a connection via SSH <br/>
<img src="https://i.imgur.com/oSx9OIr.png" height="80%" width="80%" alt="SSH lab Steps"/>
<br />
<br />
Configuration of SSH public key authentication(generating unique public and private key pair) and noticing the private and public key files  
  <br/>
<img src="https://i.imgur.com/znQLDK9.png" height="80%" width="80%" alt="SSH lab Steps"/>
<br />
<br />
When creating key pairs on other hosts, I would have to copy the user public key file to the
server, specifically, the authorized_keys file in the user .ssh folder. Even though I generated the keys on the SSH server (localhost IP of 127.0.0.1), I wanted to go through how this works. I noticed the authorized_keys file that the ssh-copy-id command created and copied the public key file to, it also sets necessary permissions for user access to the file. I went ahead and looked at the copied public key on authorized_keys
  <br/>
<img src="https://i.imgur.com/u3NrdsA.png" height="80%" width="80%" alt="SSH lab Steps"/>
<br />
<br />
I went ahead in another terminal and did ssh localhost -l kali again to login as user kali but this time I was asked for SSH private key passphrase and not the user password I use at the beginning, then I logged in using SSH public key
<br />
<br />
<img src="https://i.imgur.com/v8GO2BY.png" height="80%" width="80%" alt="SSH lab Steps"/> 
<br />
<br />

<br />
<br />

</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
