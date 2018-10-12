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

Install Proxy Zabbix on Other Site
---------------------------------
Untuk monitoring semua perangkat di kantor cabang sebenarnya cukup menggunakan satu server zabbix,
tetapi apabila terdapat banyak cabang kemudian masing-masing cabang memiliki banyak perangkat/ server yang di monitoring
terdapat sedikit permasalahan ketika yang terputus adalah jalur koneksi dari cabang ke kantor pusat atau bahkan koneksi 
di kantor pusat yang ada problem, maka zabbix akan mengirimkan email alert bahwa semua perangkat di pusat dan 
di kantor cabang bermasalah. bagaimana bila yang di monitoring dari masing-masing cabang ada 10 perangkat, kemudian
dari masing-masing perangkat / server di monitoring ada 10 item dan keseluruhan cabang ada 10 maka server zabbix akan 
mengirimkan 1000 email secara bersamaan. padahal di sini yang bermasalah hanya satu yaitu koneksi kantor pusat.
dengan zabbix proxy ini bisa di minimalisir hanya mengirimkan email sekitar 10 warning karena koneksi masing-masing 
cabang bermasalah dengan koneksi kantor pusat.  
==> cek install-zabbixproxy.txt

