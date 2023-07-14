inflating: yogast-html/js/bootstrap.bundle.min.js  
  inflating: yogast-html/js/bootstrap.js  
  inflating: yogast-html/js/bootstrap.min.js  
  inflating: yogast-html/js/custom.js  
  inflating: yogast-html/js/jquery.mCustomScrollbar.concat.min.js  
  inflating: yogast-html/js/jquery.min.js  
  inflating: yogast-html/js/jquery-3.0.0.min.js  
  inflating: yogast-html/js/owl.carousel.js  
  inflating: yogast-html/js/owl.carousel.min.js  
  inflating: yogast-html/tranner.html  
[root@ip-172-31-32-137 temp]# ls -lrt
total 5344
-rw-r--r--. 1 root root 5471119 Aug 20  2021 yogast.zip
drwxr-xr-x. 7 root root     160 Jul  8 06:22 yogast-html
[root@ip-172-31-32-137 temp]# cd yogast-html
[root@ip-172-31-32-137 yogast-html]# ls -lrt
total 124
drwxr-xr-x. 2 root root     6 Jul 27  2019 icon
-rw-r--r--. 1 root root 11223 Feb 28  2020 tranner.html
-rw-r--r--. 1 root root 19802 Feb 28  2020 index.html
-rw-r--r--. 1 root root  8270 Feb 28  2020 games.html
-rw-r--r--. 1 root root  7216 Feb 28  2020 contact.html
-rw-r--r--. 1 root root  6413 Feb 28  2020 about.html
drwxr-xr-x. 2 root root 16384 Apr 27  2020 js
drwxr-xr-x. 2 root root 16384 Apr 27  2020 images
drwxr-xr-x. 2 root root 16384 Apr 27  2020 fonts
drwxr-xr-x. 2 root root 16384 Apr 27  2020 css
[root@ip-172-31-32-137 yogast-html]# mv * /var/www/html
[root@ip-172-31-32-137 yogast-html]# cd /var/www/html
[root@ip-172-31-32-137 html]# ls -lrt
total 124
drwxr-xr-x. 2 root root     6 Jul 27  2019 icon
-rw-r--r--. 1 root root 11223 Feb 28  2020 tranner.html
-rw-r--r--. 1 root root 19802 Feb 28  2020 index.html
-rw-r--r--. 1 root root  8270 Feb 28  2020 games.html
-rw-r--r--. 1 root root  7216 Feb 28  2020 contact.html
-rw-r--r--. 1 root root  6413 Feb 28  2020 about.html
drwxr-xr-x. 2 root root 16384 Apr 27  2020 js
drwxr-xr-x. 2 root root 16384 Apr 27  2020 images
drwxr-xr-x. 2 root root 16384 Apr 27  2020 fonts
drwxr-xr-x. 2 root root 16384 Apr 27  2020 css
[root@ip-172-31-32-137 html]# systemctl status httpd
○ httpd.service - The Apache HTTP Server
     Loaded: loaded (/usr/lib/systemd/system/httpd.service; disabled; preset: disabled)
     Active: inactive (dead)
       Docs: man:httpd.service(8)
[root@ip-172-31-32-137 html]# systemctl enable httpd
Created symlink /etc/systemd/system/multi-user.target.wants/httpd.service → /usr/lib/systemd/system/httpd.service.
[root@ip-172-31-32-137 html]# systemctl start httpd
[root@ip-172-31-32-137 html]# systemctl status httpd
● httpd.service - The Apache HTTP Server
     Loaded: loaded (/usr/lib/systemd/system/httpd.service; enabled; preset: disabled)
     Active: active (running) since Sat 2023-07-08 06:38:23 UTC; 4s ago
       Docs: man:httpd.service(8)
   Main PID: 26606 (httpd)
     Status: "Started, listening on: port 80"
      Tasks: 177 (limit: 1114)
     Memory: 12.8M
        CPU: 70ms
     CGroup: /system.slice/httpd.service
             ├─26606 /usr/sbin/httpd -DFOREGROUND
             ├─26607 /usr/sbin/httpd -DFOREGROUND
             ├─26608 /usr/sbin/httpd -DFOREGROUND
             ├─26609 /usr/sbin/httpd -DFOREGROUND
             └─26610 /usr/sbin/httpd -DFOREGROUND
