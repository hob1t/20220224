#### Description
This repository will include some cvs files of scanned targets, tips and explanation of different methods of OSINT and such.

Everybody who wants to help can do it by sending the PR


#### Must learn

• NMAP

• SQLMAP

• CENSYS

• SHODAN

• COBALT STRIKE

• MALTEGO

• VULNERS Vulns and exploit DB

• GOOGLE_DORKS

• OBSERVATORY

• ХSSTRIKE xss scanner and vulntester

• VIRUSTOTAL


#### Preparing data to run slowloris

Spiderfoot should run and gather info on target before.

Go to Browse/IPv6 Address and export is as csv file.

In the terminal

 
```
cut -d "," -f6 SpiderFoot-5.csv > bcs_ru_ipv6.txt
```

Next, remove duplicates

```
sort bcs_ru_ipv6.txt | uniq -u | > bcs_ru_ipv6_no_dups.txt
```

And then run nmap with slowloris

```
cat bcs_ru_ipv6_no_dups.txt | xargs nmap -Pn --script http-slowloris-check -6 
```


Usefull links

[Nuclei](https://github.com/projectdiscovery/nuclei)


