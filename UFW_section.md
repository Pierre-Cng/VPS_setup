# UFW section:

## Steps:
### 1. Install UFW:
* sudo apt update  
* sudo apt install ufw  
### 2. Check UFW Status:
* sudo ufw status  
It should show that UFW is inactive: Status: inactive.  
### 3. Allow SSH Access:
* sudo ufw allow ssh  
or  
* sudo ufw allow [specific port number]  
### 4. Enable UFW:
* sudo ufw enable  
### 5. Check UFW Status Again:
* sudo ufw status  
The output should show the rules, with SSH access allowed and the status set to active.  
### 6. Configure Additional Rules (Optional):
* sudo ufw allow port/protocole  
You can also specify the source IP address if you want to restrict access further. For instance, to allow SSH access only from a specific IP address:
* sudo ufw allow from your_ip_address to any port 22
  
/!\ Misconfiguring the firewall can lead to unintended consequences, including being locked out of the VPS.  
## References:
<https://www.cyberciti.biz/faq/how-to-delete-a-ufw-firewall-rule-on-ubuntu-debian-linux/>  
<https://serverfault.com/questions/957740/can-not-disable-ufw-in-rescue-system-ubuntu-18>  
<https://www.it-connect.fr/configurer-un-pare-feu-local-sous-debian-11-avec-ufw/>  
<https://www.digitalocean.com/community/tutorials/how-to-set-up-a-firewall-with-ufw-on-ubuntu-20-04>  
<https://www.malekal.com/ufw-configurer-voir-creer-supprimer-reinitialiser-des-regles-de-firewall/>
<https://itslinuxfoss.com/set-up-firewall-with-ufw-debian-12/#:~:text=What%20is%20the%20Method%20to%20Install%20UFW%20on,Step%204%3A%20Check%20the%20Status%20of%20UFW%20>
