```bash
[*] ssh on tcp/22

	[-] Bruteforce logins:

		hydra -L "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e nsr -s 22 -o "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp22/tcp_22_ssh_hydra.txt" ssh://164.92.239.134

		medusa -U "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e ns -n 22 -O "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp22/tcp_22_ssh_medusa.txt" -M ssh -h 164.92.239.134

[*] http on tcp/80

	[-] (feroxbuster) Multi-threaded recursive directory/file enumeration for web servers using various wordlists:

		feroxbuster -u http://164.92.239.134:80 -t 10 -w /usr/share/wordlists/dirbuster/directory-list-2.3-medium.txt -x "txt,html,php,asp,aspx,jsp" -v -k -n -e -o /home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp80/tcp_80_http_feroxbuster_dirbuster.txt

	[-] Credential bruteforcing commands (don't run these without modifying them):

		hydra -L "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e nsr -s 80 -o "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp80/tcp_80_http_auth_hydra.txt" http-get://164.92.239.134/path/to/auth/area

		medusa -U "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e ns -n 80 -O "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp80/tcp_80_http_auth_medusa.txt" -M http -h 164.92.239.134 -m DIR:/path/to/auth/area

		hydra -L "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e nsr -s 80 -o "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp80/tcp_80_http_form_hydra.txt" http-post-form://164.92.239.134/path/to/login.php:"username=^USER^&password=^PASS^":"invalid-login-message"

		medusa -U "/usr/share/seclists/Usernames/top-usernames-shortlist.txt" -P "/usr/share/seclists/Passwords/darkweb2017-top100.txt" -e ns -n 80 -O "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp80/tcp_80_http_form_medusa.txt" -M web-form -h 164.92.239.134 -m FORM:/path/to/login.php -m FORM-DATA:"post?username=&password=" -m DENY-SIGNAL:"invalid login message"

	[-] (nikto) old but generally reliable web server enumeration tool:

		nikto -ask=no -h http://164.92.239.134:80 2>&1 | tee "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp80/tcp_80_http_nikto.txt"

	[-] (wpscan) WordPress Security Scanner (useful if WordPress is found):

		wpscan --url http://164.92.239.134:80/ --no-update -e vp,vt,tt,cb,dbe,u,m --plugins-detection aggressive --plugins-version-detection aggressive -f cli-no-color 2>&1 | tee "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp80/tcp_80_http_wpscan.txt"


```