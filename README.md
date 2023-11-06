# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:

### Find out the ip address of the attackers system

![image](https://github.com/Jayabharathi3/Metasploit-for-reconnaissance/assets/120367796/8e0c33ca-46e4-4c01-9d3d-3569c3b4bdff)

### Invoke msfconsole 

![image](https://github.com/Jayabharathi3/Metasploit-for-reconnaissance/assets/120367796/78354b07-be6a-49b8-8a8d-2e44ed1db890)

### Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.

![image](https://github.com/Jayabharathi3/Metasploit-for-reconnaissance/assets/120367796/04c7e825-7d02-4089-b357-6b859b50a15f)

### Port Scanning:
Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000).

**msf >  nmap -sT 192.168.1810/24 -p1-1000**

![image](https://github.com/Jayabharathi3/Metasploit-for-reconnaissance/assets/120367796/277ca7cf-57e2-46b5-b5bb-d76671ea338b)

### Use the db-nmap command to scan and save the results into Metasploit's postgresql attached database. In that way, you can use those results in the exploitation stage later.

scan the targets with the command db_nmap as follows.
**msf > db_nmap 192.168.181.0/24**

![image](https://github.com/Jayabharathi3/Metasploit-for-reconnaissance/assets/120367796/a0bbe60c-0e63-4a22-8f48-026e42d6c085)

### Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. 
**cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l**

![image](https://github.com/Jayabharathi3/Metasploit-for-reconnaissance/assets/120367796/073c5bd8-f5fd-4577-9215-65ee31324087)


### Search is a powerful command in Metasploit that you can use to find what you want to locate.
**msf >search name : Microsoft type : exploit**

![image](https://github.com/Jayabharathi3/Metasploit-for-reconnaissance/assets/120367796/088595f6-3650-4508-b097-0176944d98ae)

### info

![image](https://github.com/Jayabharathi3/Metasploit-for-reconnaissance/assets/120367796/a0801a52-773f-422d-afc4-d7c4c9dcf89f)

## MYSQL ENUMERATION

**db_nmap -sV -sC -p 3306 <metasploitable_ip_address>**

![image](https://github.com/Jayabharathi3/Metasploit-for-reconnaissance/assets/120367796/fc09f869-b6fd-4051-ac9a-87abd535fe1a)

### Use the search option to look for an auxiliary module to scan and enumerate the MySQL **database. search type:auxiliary mysql**

![image](https://github.com/Jayabharathi3/Metasploit-for-reconnaissance/assets/120367796/bfa3e745-b188-4093-b6da-c2b73a4e6fc0)

**use 11 Or: use auxiliary/scanner/mysql/mysql_version**

![image](https://github.com/Jayabharathi3/Metasploit-for-reconnaissance/assets/120367796/a80ee301-0a4c-4517-b461-cd3eca0882e5)

**Use the set rhosts command to set the parameter and run the module, as follows **

![image](https://github.com/Jayabharathi3/Metasploit-for-reconnaissance/assets/120367796/548220d6-edf5-434d-9782-5e665dc4253d)

**After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.**

![image](https://github.com/Jayabharathi3/Metasploit-for-reconnaissance/assets/120367796/a630f38a-b262-444e-8749-dff963f7e444)

**/usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt**

![image](https://github.com/Jayabharathi3/Metasploit-for-reconnaissance/assets/120367796/79f3bd03-78ae-4904-83c2-7733949c28c1)



## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
