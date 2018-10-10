Install-Zabbix  
==============
  
install zabbix 3.4 dan zabbix proxy dengan tambahan tool seperti smokeping, alert email, alert telegram, grafik, grafana dsb

Konfigurasi Postfix untuk email Alert
--------------------------------------
==> cek konfigurasipostfix.txt

 
Smokeping_zabbix
-----------------
template fork from https://github.com/komeiy/Smokeping_Zabbix
Hasil yang di dapat dari smokeping grafik icmp latency dan http latency

Ping Latency Graph
------------------
- besar kecil paket (max, avg, min)
- ping loss
- percentase (50th)

![Ping Latency Graph](https://github.com/butdy/install-zabbix/blob/master/screenshoot/Ping-graph.JPG)

HTTP Latency Graph
------------------
- Http latency
- percentase (50th)
![HTTP Latency Graph](https://github.com/butdy/install-zabbix/blob/master/screenshoot/http-grarh.JPG)

Integrate Grafana and Zabbix
----------------------------
Melihat Indahnya Dashboard Grafana yang terasa lebih indah daripada zabbix, tetapi rasanya masih 
terasa manis zabbix dan muncullah ide2 dari penggguna dan pemakai grafana untuk Combine keduanya.
Untuk integrasi antara zabbix dan grafana kita perlu menginstall grafana terlebih dahulu
==> cek installgrafana.txt
