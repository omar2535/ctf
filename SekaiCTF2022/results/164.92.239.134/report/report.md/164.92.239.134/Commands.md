```bash
nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/_quick_tcp_nmap.txt" -oX "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/xml/_quick_tcp_nmap.xml" 164.92.239.134

nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/_full_tcp_nmap.txt" -oX "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/xml/_full_tcp_nmap.xml" 164.92.239.134

nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -oN "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/_quick_tcp_nmap.txt" -oX "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/xml/_quick_tcp_nmap.xml" 164.92.239.134

nmap -vv --reason -Pn -T4 -sV -sC --version-all -A --osscan-guess -p- -oN "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/_full_tcp_nmap.txt" -oX "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/xml/_full_tcp_nmap.xml" 164.92.239.134

nmap -vv --reason -Pn -T4 -sV -p 22 --script="banner,ssh2-enum-algos,ssh-hostkey,ssh-auth-methods" -oN "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp22/tcp_22_ssh_nmap.txt" -oX "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp22/xml/tcp_22_ssh_nmap.xml" 164.92.239.134

feroxbuster -u http://164.92.239.134:80/ -t 10 -w /home/omar2535/.config/AutoRecon/wordlists/dirbuster.txt -x "txt,html,php,asp,aspx,jsp" -v -k -n -q -e -o "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp80/tcp_80_http_feroxbuster_dirbuster.txt"

curl -sSikf http://164.92.239.134:80/.well-known/security.txt

curl -sSikf http://164.92.239.134:80/robots.txt

curl -sSik http://164.92.239.134:80/

nmap -vv --reason -Pn -T4 -sV -p 80 --script="banner,(http* or ssl*) and not (brute or broadcast or dos or external or http-slowloris* or fuzzer)" -oN "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp80/tcp_80_http_nmap.txt" -oX "/home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp80/xml/tcp_80_http_nmap.xml" 164.92.239.134

whatweb --color=never --no-errors -a 3 -v http://164.92.239.134:80 2>&1

wkhtmltoimage --format png http://164.92.239.134:80/ /home/omar2535/Desktop/programming/CTF/SekaiCTF2022/results/164.92.239.134/scans/tcp80/tcp_80_http_screenshot.png


```