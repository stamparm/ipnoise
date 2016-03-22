# Installation

```
sudo su
apt-get install python python-pcapy git
cd /root
git clone https://github.com/stamparm/ipnoise.git
(crontab -l ; echo '*/1 * * * * if [ -n "$(ps -ef | grep -v grep | grep ipnoise/sensor.py)" ]; then : ; else python /root/ipnoise/sensor.py; fi') | crontab -
```
