# VPS_setup

Quick reminder of how to setup a virtual personal server (VPS).

## Steps to setup a VPS:

* Choose a hosting provider
* Choose an OS (c.f [Debian section](#debian-section))
* Configure the VPS through the hosting provider platform ([here](https://help.ovhcloud.com/csm/fr-vps-getting-started?id=kb_article_view&sysparm_article=KB0047736))
* Create and configure ssh connection (c.f [SSH section](#ssh-section))
* Update the system
* Secure the VPS (e.g configure a firewall, c.f [Security section](#security-section))
* Install necessary software (e.g Jenkins, see [Jenkins section](#jenkins-section)))
* Setup backup strategy (c.f [Backup strategy section](#backup-strategy-section))

## Debian section:

[Bash reminder](Bash_reminder.md)  
[Debian info](Debian_info.md)  

## SSH section:

[SSH section](SSH_section.md)

## Security section:

[Security section](Security_section.md)  
[UFW section](UFW_section.md)

## Jenkins section:

[Jenkins section](Jenkins_section.md)

## Backup strategy section:

[Backup strategy section](Backup_strategy_section.md)

## Rescue mode:

To get back your VPS in case of problem you can reboot it in rescue mode, which allows you to access the VPS disk with another external OS (linux).
Here is a [link to a quick tutorial](https://help.ovhcloud.com/csm/fr-vps-rescue?id=kb_article_view&sysparm_article=KB0047658).   
