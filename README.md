# TSQTT-CyberRange
Cyber Range for Information Security Training
=============================================================================
<TSQTT-CyberRange is based on Armitage - 12/05/2022>
=============================================================================
Instructions for TSQTT-CyberRange on Kali 2022.3 with latest updates. Java 18 breaks EVERYTHING, so avoid for now. Do everything below within a root prompt!:

msfdb init

edit /etc/postgresql/15/main/pg_hba.conf

on the line 97 (IPV4 local connections)
switch “scram-sha-256” to “trust”

systemctl enable postgresql
systemctl stop postgresql
systemctl start postgresql

java -version

if it says anything other than 11, lets go way back - because why not:

apt update; apt install -y openjdk-11-jdk

update-alternatives --config java

choose the openjdk-11 as the default. then run java -version to make sure it is good to go.

cd /opt

git clone https://github.com/TSQTT-Cyber-Lab/TSQTT-CyberRange.git

cd armitage

./package.sh

cd release/unix

./armitage

username: msf
password: cyber

Leave the rest. Do you want to start blah blah for you? Answer yes. 

Observed broken functionality / issues:
- Attacks - Find Attacks doesn't seem to work

# Disclaimer
   ----------
Use this code for your development and don't hack systems that you don't 
have permission to hack. The existence of this software does not reflect the 
opinions or beliefs of my current employers, past employers, future 
employers, or any small animals I come into contact with. Enjoy this 
software with my blessing. I hope it helps you learn and become a better 
security professional.

# Contact
   -------

