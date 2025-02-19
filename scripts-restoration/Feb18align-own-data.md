Microsoft Windows [Version 10.0.26100.3194]
(c) Microsoft Corporation. All rights reserved.

C:\Users\欧阳葭>wsl
Welcome to Ubuntu 24.04.2 LTS (GNU/Linux 5.15.167.4-microsoft-standard-WSL2 x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Tue Feb 18 22:25:44 CST 2025

  System load:  0.0                 Processes:             48
  Usage of /:   0.3% of 1006.85GB   Users logged in:       0
  Memory usage: 3%                  IPv4 address for eth0: 172.19.133.12
  Swap usage:   0%

 * Strictly confined Kubernetes makes edge and IoT secure. Learn how MicroK8s
   just raised the bar for easy, resilient and secure K8s cluster deployment.

   https://ubuntu.com/engage/secure-kubernetes-at-the-edge

This message is shown once a day. To disable it please create the
/home/suki/.hushlogin file.
(base) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ sudo apt update
sudo apt install ncbi-entrez-direct
[sudo] password for suki:
Hit:1 http://archive.ubuntu.com/ubuntu noble InRelease
Get:2 http://archive.ubuntu.com/ubuntu noble-updates InRelease [126 kB]
Get:3 http://security.ubuntu.com/ubuntu noble-security InRelease [126 kB]
Get:4 http://archive.ubuntu.com/ubuntu noble-backports InRelease [126 kB]
Get:5 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 Packages [865 kB]
Get:6 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 Components [151 kB]
Get:7 http://archive.ubuntu.com/ubuntu noble-updates/universe amd64 Packages [1014 kB]
Get:8 http://archive.ubuntu.com/ubuntu noble-updates/universe amd64 Components [362 kB]
Get:9 http://archive.ubuntu.com/ubuntu noble-updates/restricted amd64 Components [212 B]
Get:10 http://archive.ubuntu.com/ubuntu noble-updates/multiverse amd64 Components [940 B]
Get:11 http://archive.ubuntu.com/ubuntu noble-backports/main amd64 Components [208 B]
Get:12 http://archive.ubuntu.com/ubuntu noble-backports/universe amd64 Components [17.7 kB]
Get:13 http://archive.ubuntu.com/ubuntu noble-backports/restricted amd64 Components [216 B]
Get:14 http://archive.ubuntu.com/ubuntu noble-backports/multiverse amd64 Components [212 B]
Get:15 http://security.ubuntu.com/ubuntu noble-security/main amd64 Packages [617 kB]
Get:16 http://security.ubuntu.com/ubuntu noble-security/main amd64 Components [8932 B]
Get:17 http://security.ubuntu.com/ubuntu noble-security/universe amd64 Packages [803 kB]
Get:18 http://security.ubuntu.com/ubuntu noble-security/universe amd64 Components [52.0 kB]
Get:19 http://security.ubuntu.com/ubuntu noble-security/restricted amd64 Components [212 B]
Get:20 http://security.ubuntu.com/ubuntu noble-security/multiverse amd64 Components [212 B]
Fetched 4272 kB in 1s (3328 kB/s)
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
6 packages can be upgraded. Run 'apt list --upgradable' to see them.
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following package was automatically installed and is no longer required:
  libllvm17t64
Use 'sudo apt autoremove' to remove it.
Suggested packages:
  libxml-simple-perl libxml2-utils unzip
The following NEW packages will be installed:
  ncbi-entrez-direct
0 upgraded, 1 newly installed, 0 to remove and 6 not upgraded.
Need to get 6315 kB of archives.
After this operation, 26.9 MB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu noble-updates/universe amd64 ncbi-entrez-direct amd64 19.2.20230331+dfsg-3ubuntu0.24.04.2 [6315 kB]
Fetched 6315 kB in 1s (4988 kB/s)
Selecting previously unselected package ncbi-entrez-direct.
(Reading database ... 40774 files and directories currently installed.)
Preparing to unpack .../ncbi-entrez-direct_19.2.20230331+dfsg-3ubuntu0.24.04.2_amd64.deb ...
Adding 'diversion of /usr/bin/efetch to /usr/bin/efetch.acedb by ncbi-entrez-direct'
Adding 'diversion of /usr/share/man/man1/efetch.1.gz to /usr/share/man/man1/efetch.acedb.1.gz by ncbi-entrez-direct'
Adding 'diversion of /usr/bin/einfo to /usr/bin/einfo.epub by ncbi-entrez-direct'
Adding 'diversion of /usr/share/man/man1/einfo.1.gz to /usr/share/man/man1/einfo.epub.1.gz by ncbi-entrez-direct'
Unpacking ncbi-entrez-direct (19.2.20230331+dfsg-3ubuntu0.24.04.2) ...
Setting up ncbi-entrez-direct (19.2.20230331+dfsg-3ubuntu0.24.04.2) ...
Processing triggers for man-db (2.12.0-4build2) ...
(base) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ efetch -db nucleotide -id MZ160998.1 -format > vatica-odorata.fna
 ERROR:  Missing -format argument
(base) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ efetch -db nucleotide -id MZ160998.1 -format fasta > vatica-odorata.fna
(base) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ head -n 10 vatica-odorata.fna
>MZ160998.1 Vatica odorata chloroplast, complete genome
GTTAGTCATATTAATTAATGGGCGAACGACGGGAATTGAACCCGCGCATGGTGGATCCACAATCCACTGC
CTTGATCCACTTGGCTACATCCGCCCTTAGAGTATAGTATATAGTATACTTTTTCACATATTTTTATTTG
CATTTTCAATTTGAAATTAAAGAAAAAACTTCAAAACTTATGTAAATAAAAGACTACTAAAATAAAGGAG
CAATACCAATACTCTTGATAGAACAAGAAATTGGATATTGCTCCTTTATTTTCAAAAACTCGTATACACT
AAGACAAGAGTCTTATCCATTTGTAGATGGAGCTTCAACAGCAGCTAGGTCTAGAGGGAAGTTATGAGCA
TTACGTTCATGCATAACTTCCATACCAAGGTTAGCACGGTTAATAATATCCGCCCAGGTATTAATTACAC
GACCTTGACTATCAACTACAGATTGGTTGAAATTGAAACCATTTAGGTTGAATGCCATAGTACTGATACC
TAAAGCAGTGAACCAGATACCCACTACAGGCCAAGCAGCTAAGAAGAAGTGTAAAGAACGAGAATTGTTG
AAACTAGCATATTGGAAGATTAATCGGCCAAAATAACCATGAGCCGCTACGATATTATAAGTTTCTCCCT
(base) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ ls -lh
total 169M
drwxrwxrwx 1 suki suki 4.0K Feb 17 05:03  AppData
lrwxrwxrwx 1 suki suki   38 Feb 17 05:02 'Application Data' -> /mnt/c/Users/欧阳葭/AppData/Roaming
drwxrwxrwx 1 suki suki 4.0K Feb 17 05:10  Contacts
lrwxrwxrwx 1 suki suki   66 Feb 17 05:02  Cookies -> /mnt/c/Users/欧阳葭/AppData/Local/Microsoft/Windows/INetCookies
drwxrwxrwx 1 suki suki 4.0K Nov 27 11:08 'Creative Cloud Files'
drwxrwxrwx 1 suki suki 4.0K Feb 18 11:04  Desktop
drwxrwxrwx 1 suki suki 4.0K Feb 17 05:10  Documents
drwxrwxrwx 1 suki suki 4.0K Feb 18 21:56  Downloads
drwxrwxrwx 1 suki suki 4.0K Feb 17 05:10  Favorites
drwxrwxrwx 1 suki suki 4.0K Feb 17 05:10  Links
lrwxrwxrwx 1 suki suki   36 Feb 17 05:02 'Local Settings' -> /mnt/c/Users/欧阳葭/AppData/Local
-rwxrwxrwx 1 suki suki 148M Feb 11 15:47  Miniconda3-latest-Linux-x86_64.sh
drwxrwxrwx 1 suki suki 4.0K Feb 17 05:10  Music
lrwxrwxrwx 1 suki suki   32 Feb 17 05:02 'My Documents' -> /mnt/c/Users/欧阳葭/Documents
-rwxrwxrwx 1 suki suki  15M Feb 18 04:31  NTUSER.DAT
-rwxrwxrwx 1 suki suki  64K Feb 17 05:02  NTUSER.DAT{77339549-ed1e-11ef-9f22-00155dc5365d}.TM.blf
-rwxrwxrwx 1 suki suki 512K Feb 17 05:02  NTUSER.DAT{77339549-ed1e-11ef-9f22-00155dc5365d}.TMContainer00000000000000000001.regtrans-ms
-rwxrwxrwx 1 suki suki 512K Feb 17 05:02  NTUSER.DAT{77339549-ed1e-11ef-9f22-00155dc5365d}.TMContainer00000000000000000002.regtrans-ms
lrwxrwxrwx 1 suki suki   74 Feb 17 05:02  NetHood -> '/mnt/c/Users/欧阳葭/AppData/Roaming/Microsoft/Windows/Network Shortcuts'
drwxrwxrwx 1 suki suki 4.0K Feb 18 10:57  OneDrive
drwxrwxrwx 1 suki suki 4.0K Feb 17 05:10  Pictures
lrwxrwxrwx 1 suki suki   74 Feb 17 05:02  PrintHood -> '/mnt/c/Users/欧阳葭/AppData/Roaming/Microsoft/Windows/Printer Shortcuts'
lrwxrwxrwx 1 suki suki   63 Feb 17 05:02  Recent -> /mnt/c/Users/欧阳葭/AppData/Roaming/Microsoft/Windows/Recent
drwxrwxrwx 1 suki suki 4.0K Feb 17 05:10 'Saved Games'
drwxrwxrwx 1 suki suki 4.0K Feb 17 05:10  Searches
lrwxrwxrwx 1 suki suki   63 Feb 17 05:02  SendTo -> /mnt/c/Users/欧阳葭/AppData/Roaming/Microsoft/Windows/SendTo
lrwxrwxrwx 1 suki suki   66 Feb 17 05:02  Templates -> /mnt/c/Users/欧阳葭/AppData/Roaming/Microsoft/Windows/Templates
drwxrwxrwx 1 suki suki 4.0K Feb 17 05:10  Videos
drwxrwxrwx 1 suki suki 4.0K Dec 25 23:37  Zotero
-rwxrwxrwx 1 suki suki 1.8M Feb 17 05:02  ntuser.dat.LOG1
-rwxrwxrwx 1 suki suki 3.8M Feb 17 05:02  ntuser.dat.LOG2
-rwxrwxrwx 1 suki suki   20 Feb 17 05:10  ntuser.ini
drwxrwxrwx 1 suki suki 4.0K Feb  4 11:58  source
-rwxrwxrwx 1 suki suki 151K Feb 18 22:47  vatica-odorata.fna
lrwxrwxrwx 1 suki suki   67 Feb 17 05:02  「开始」菜单 -> '/mnt/c/Users/欧阳葭/AppData/Roaming/Microsoft/Windows/Start Menu'
(base) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ pwd
/mnt/c/Users/欧阳葭
(base) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ ^C
(base) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ ^C
(base) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ efetch -db nucleotide -id MZ397801.1 -format fasta > vatica-rassak.fna
(base) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ efetch -db nucleotide -id MZ397800.1 -format fasta > vatica-xsbn.fna
(base) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ cd ~/phylo-class/hw-aligning-your-own-data
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ ls
MT934442.1.fna  MT934442.1.fna:Zone.Identifier  vatica-odorata.fna  vatica-rassak.fna  vatica-xsbn.fna
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ cat *.fna > all_chloroplasts.fasta
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ muscle -in all_chloroplasts.fasta -out aligned_sequences.aln


Invalid command line
Unknown option in

(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ which muscle
/home/suki/miniconda3/bin/muscle
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ muscle -align all_chloroplasts.fasta -output aligned_sequences.aln

muscle 5.1.linux64 []  16.2Gb RAM, 22 cores
Built Feb 24 2022 03:16:15
(C) Copyright 2004-2021 Robert C. Edgar.
https://drive5.com

Input: 4 seqs, avg length 151227, max 151493

00:00 8.8Mb  CPU has 22 cores, defaulting to 20 threads
00:00 74.3Gb  100.0% Calc posteriors
ps aux | grep muscle
ls -ln

Killed
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ ps aux | grep muscle
suki       17706  0.0  0.0   4088  1928 pts/0    S+   23:12   0:00 grep --color=auto muscle
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ ls -ln
total 1216
-rw-r--r-- 1 1000 1000 155390 Feb 18 11:44 MT934442.1.fna
-rw-r--r-- 1 1000 1000    187 Feb 18 11:44 MT934442.1.fna:Zone.Identifier
-rw-r--r-- 1 1000 1000      0 Feb 18 23:04 aligned_sequences.aln
-rw-r--r-- 1 1000 1000 615952 Feb 18 23:02 all_chloroplasts.fasta
-rw-r--r-- 1 1000 1000 153714 Feb 18 22:47 vatica-odorata.fna
-rw-r--r-- 1 1000 1000 153612 Feb 18 23:00 vatica-rassak.fna
-rw-r--r-- 1 1000 1000 153236 Feb 18 23:01 vatica-xsbn.fna
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ muscle -align all_chloroplasts.fasta -output aligned_sequences.aln -maxiters 2


Invalid command line
Unknown option maxiters

(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ muscle -super5 all_chloroplasts.fasta -output aligned_sequences.aln

muscle 5.1.linux64 []  16.2Gb RAM, 22 cores
Built Feb 24 2022 03:16:15
(C) Copyright 2004-2021 Robert C. Edgar.
https://drive5.com

Input: 4 seqs, length avg 151227 max 151493


WARNING: Sequence length >5k may require excessive memory

00:00 8.5Mb   100.0% Derep 3 uniques, 0 dupes
00:00 12Mb   CPU has 22 cores, defaulting to 20 threads


muscle -super5 all_chloroplasts.fasta -output aligned_sequences.aln
Elapsed time 00:00
Max memory 12Mb

---Fatal error---
allocflat.cpp(15) assert failed: uint64(Size) == Size64
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ sudo apt install mafft
[sudo] password for suki:
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following package was automatically installed and is no longer required:
  libllvm17t64
Use 'sudo apt autoremove' to remove it.
The following additional packages will be installed:
  bzip2 fonts-lato javascript-common libauthen-sasl-perl libclone-perl libdata-dump-perl libencode-locale-perl
  libfile-listing-perl libfont-afm-perl libhtml-form-perl libhtml-format-perl libhtml-parser-perl libhtml-tagset-perl
  libhtml-tree-perl libhttp-cookies-perl libhttp-daemon-perl libhttp-date-perl libhttp-message-perl
  libhttp-negotiate-perl libio-html-perl libio-socket-ssl-perl libjs-jquery liblwp-mediatypes-perl
  liblwp-protocol-https-perl libmailtools-perl libncurses6 libnet-http-perl libnet-smtp-ssl-perl libnet-ssleay-perl
  libruby libruby3.2 libtimedate-perl libtry-tiny-perl liburi-perl libwww-perl libwww-robotrules-perl lynx lynx-common
  mailcap perl-openssl-defaults rake ruby ruby-net-telnet ruby-rubygems ruby-sdbm ruby-webrick ruby-xmlrpc ruby3.2
  rubygems-integration unzip zip
Suggested packages:
  bzip2-doc apache2 | lighttpd | httpd libdigest-hmac-perl libgssapi-perl libio-compress-brotli-perl
  libcrypt-ssleay-perl libsub-name-perl libbusiness-isbn-perl libregexp-ipv6-perl libauthen-ntlm-perl debhelper ri
  ruby-dev bundler
Recommended packages:
  blast2
The following NEW packages will be installed:
  bzip2 fonts-lato javascript-common libauthen-sasl-perl libclone-perl libdata-dump-perl libencode-locale-perl
  libfile-listing-perl libfont-afm-perl libhtml-form-perl libhtml-format-perl libhtml-parser-perl libhtml-tagset-perl
  libhtml-tree-perl libhttp-cookies-perl libhttp-daemon-perl libhttp-date-perl libhttp-message-perl
  libhttp-negotiate-perl libio-html-perl libio-socket-ssl-perl libjs-jquery liblwp-mediatypes-perl
  liblwp-protocol-https-perl libmailtools-perl libncurses6 libnet-http-perl libnet-smtp-ssl-perl libnet-ssleay-perl
  libruby libruby3.2 libtimedate-perl libtry-tiny-perl liburi-perl libwww-perl libwww-robotrules-perl lynx lynx-common
  mafft mailcap perl-openssl-defaults rake ruby ruby-net-telnet ruby-rubygems ruby-sdbm ruby-webrick ruby-xmlrpc
  ruby3.2 rubygems-integration unzip zip
0 upgraded, 52 newly installed, 0 to remove and 0 not upgraded.
Need to get 13.6 MB of archives.
After this operation, 57.1 MB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://archive.ubuntu.com/ubuntu noble/main amd64 fonts-lato all 2.015-1 [2781 kB]
Get:2 http://archive.ubuntu.com/ubuntu noble/main amd64 libncurses6 amd64 6.4+20240113-1ubuntu2 [112 kB]
Get:3 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 bzip2 amd64 1.0.8-5.1build0.1 [34.5 kB]
Get:4 http://archive.ubuntu.com/ubuntu noble/main amd64 javascript-common all 11+nmu1 [5936 B]
Get:5 http://archive.ubuntu.com/ubuntu noble/main amd64 libclone-perl amd64 0.46-1build3 [10.7 kB]
Get:6 http://archive.ubuntu.com/ubuntu noble/main amd64 libdata-dump-perl all 1.25-1 [25.9 kB]
Get:7 http://archive.ubuntu.com/ubuntu noble/main amd64 libencode-locale-perl all 1.05-3 [11.6 kB]
Get:8 http://archive.ubuntu.com/ubuntu noble/main amd64 libtimedate-perl all 2.3300-2 [34.0 kB]
Get:9 http://archive.ubuntu.com/ubuntu noble/main amd64 libhttp-date-perl all 6.06-1 [10.2 kB]
Get:10 http://archive.ubuntu.com/ubuntu noble/main amd64 libfile-listing-perl all 6.16-1 [11.3 kB]
Get:11 http://archive.ubuntu.com/ubuntu noble/main amd64 libfont-afm-perl all 1.20-4 [13.0 kB]
Get:12 http://archive.ubuntu.com/ubuntu noble/main amd64 libhtml-tagset-perl all 3.20-6 [11.3 kB]
Get:13 http://archive.ubuntu.com/ubuntu noble/main amd64 liburi-perl all 5.27-1 [88.0 kB]
Get:14 http://archive.ubuntu.com/ubuntu noble/main amd64 libhtml-parser-perl amd64 3.81-1build3 [85.8 kB]
Get:15 http://archive.ubuntu.com/ubuntu noble/main amd64 libio-html-perl all 1.004-3 [15.9 kB]
Get:16 http://archive.ubuntu.com/ubuntu noble/main amd64 liblwp-mediatypes-perl all 6.04-2 [20.1 kB]
Get:17 http://archive.ubuntu.com/ubuntu noble/main amd64 libhttp-message-perl all 6.45-1ubuntu1 [78.2 kB]
Get:18 http://archive.ubuntu.com/ubuntu noble/main amd64 libhtml-form-perl all 6.11-1 [32.1 kB]
Get:19 http://archive.ubuntu.com/ubuntu noble/main amd64 libhtml-tree-perl all 5.07-3 [200 kB]
Get:20 http://archive.ubuntu.com/ubuntu noble/main amd64 libhtml-format-perl all 2.16-2 [36.9 kB]
Get:21 http://archive.ubuntu.com/ubuntu noble/main amd64 libhttp-cookies-perl all 6.11-1 [18.2 kB]
Get:22 http://archive.ubuntu.com/ubuntu noble/main amd64 libhttp-daemon-perl all 6.16-1 [22.4 kB]
Get:23 http://archive.ubuntu.com/ubuntu noble/main amd64 libhttp-negotiate-perl all 6.01-2 [12.4 kB]
Get:24 http://archive.ubuntu.com/ubuntu noble/main amd64 perl-openssl-defaults amd64 7build3 [6626 B]
Get:25 http://archive.ubuntu.com/ubuntu noble/main amd64 libnet-ssleay-perl amd64 1.94-1build4 [316 kB]
Get:26 http://archive.ubuntu.com/ubuntu noble/main amd64 libio-socket-ssl-perl all 2.085-1 [195 kB]
Get:27 http://archive.ubuntu.com/ubuntu noble/main amd64 libjs-jquery all 3.6.1+dfsg+~3.5.14-1 [328 kB]
Get:28 http://archive.ubuntu.com/ubuntu noble/main amd64 libnet-http-perl all 6.23-1 [22.3 kB]
Get:29 http://archive.ubuntu.com/ubuntu noble/main amd64 libtry-tiny-perl all 0.31-2 [20.8 kB]
Get:30 http://archive.ubuntu.com/ubuntu noble/main amd64 libwww-robotrules-perl all 6.02-1 [12.6 kB]
Get:31 http://archive.ubuntu.com/ubuntu noble/main amd64 libwww-perl all 6.76-1 [138 kB]
Get:32 http://archive.ubuntu.com/ubuntu noble/main amd64 liblwp-protocol-https-perl all 6.13-1 [9006 B]
Get:33 http://archive.ubuntu.com/ubuntu noble/main amd64 libnet-smtp-ssl-perl all 1.04-2 [6218 B]
Get:34 http://archive.ubuntu.com/ubuntu noble/main amd64 libmailtools-perl all 2.21-2 [80.4 kB]
Get:35 http://archive.ubuntu.com/ubuntu noble/main amd64 rubygems-integration all 1.18 [5336 B]
Get:36 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 ruby3.2 amd64 3.2.3-1ubuntu0.24.04.3 [50.7 kB]
Get:37 http://archive.ubuntu.com/ubuntu noble/main amd64 ruby-rubygems all 3.4.20-1 [238 kB]
Get:38 http://archive.ubuntu.com/ubuntu noble/main amd64 ruby amd64 1:3.2~ubuntu1 [3466 B]
Get:39 http://archive.ubuntu.com/ubuntu noble/main amd64 rake all 13.0.6-3 [61.6 kB]
Get:40 http://archive.ubuntu.com/ubuntu noble/main amd64 ruby-net-telnet all 0.2.0-1 [13.3 kB]
Get:41 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 ruby-webrick all 1.8.1-1ubuntu0.1 [52.6 kB]
Get:42 http://archive.ubuntu.com/ubuntu noble/main amd64 ruby-xmlrpc all 0.3.2-2 [24.8 kB]
Get:43 http://archive.ubuntu.com/ubuntu noble/main amd64 ruby-sdbm amd64 1.0.0-5build4 [16.2 kB]
Get:44 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 libruby3.2 amd64 3.2.3-1ubuntu0.24.04.3 [5341 kB]
Get:45 http://archive.ubuntu.com/ubuntu noble/main amd64 libruby amd64 1:3.2~ubuntu1 [4694 B]
Get:46 http://archive.ubuntu.com/ubuntu noble/universe amd64 lynx-common all 2.9.0rel.0-2build2 [1006 kB]
Get:47 http://archive.ubuntu.com/ubuntu noble/universe amd64 mafft amd64 7.505-1 [795 kB]
Get:48 http://archive.ubuntu.com/ubuntu noble/main amd64 mailcap all 3.70+nmu1ubuntu1 [23.8 kB]
Get:49 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 unzip amd64 6.0-28ubuntu4.1 [174 kB]
Get:50 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 zip amd64 3.0-13ubuntu0.2 [176 kB]
Get:51 http://archive.ubuntu.com/ubuntu noble/main amd64 libauthen-sasl-perl all 2.1700-1 [42.9 kB]
Get:52 http://archive.ubuntu.com/ubuntu noble/universe amd64 lynx amd64 2.9.0rel.0-2build2 [715 kB]
Fetched 13.6 MB in 3s (5073 kB/s)
Extracting templates from packages: 100%
Selecting previously unselected package fonts-lato.
(Reading database ... 41003 files and directories currently installed.)
Preparing to unpack .../00-fonts-lato_2.015-1_all.deb ...
Unpacking fonts-lato (2.015-1) ...
Selecting previously unselected package libncurses6:amd64.
Preparing to unpack .../01-libncurses6_6.4+20240113-1ubuntu2_amd64.deb ...
Unpacking libncurses6:amd64 (6.4+20240113-1ubuntu2) ...
Selecting previously unselected package bzip2.
Preparing to unpack .../02-bzip2_1.0.8-5.1build0.1_amd64.deb ...
Unpacking bzip2 (1.0.8-5.1build0.1) ...
Selecting previously unselected package javascript-common.
Preparing to unpack .../03-javascript-common_11+nmu1_all.deb ...
Unpacking javascript-common (11+nmu1) ...
Selecting previously unselected package libclone-perl:amd64.
Preparing to unpack .../04-libclone-perl_0.46-1build3_amd64.deb ...
Unpacking libclone-perl:amd64 (0.46-1build3) ...
Selecting previously unselected package libdata-dump-perl.
Preparing to unpack .../05-libdata-dump-perl_1.25-1_all.deb ...
Unpacking libdata-dump-perl (1.25-1) ...
Selecting previously unselected package libencode-locale-perl.
Preparing to unpack .../06-libencode-locale-perl_1.05-3_all.deb ...
Unpacking libencode-locale-perl (1.05-3) ...
Selecting previously unselected package libtimedate-perl.
Preparing to unpack .../07-libtimedate-perl_2.3300-2_all.deb ...
Unpacking libtimedate-perl (2.3300-2) ...
Selecting previously unselected package libhttp-date-perl.
Preparing to unpack .../08-libhttp-date-perl_6.06-1_all.deb ...
Unpacking libhttp-date-perl (6.06-1) ...
Selecting previously unselected package libfile-listing-perl.
Preparing to unpack .../09-libfile-listing-perl_6.16-1_all.deb ...
Unpacking libfile-listing-perl (6.16-1) ...
Selecting previously unselected package libfont-afm-perl.
Preparing to unpack .../10-libfont-afm-perl_1.20-4_all.deb ...
Unpacking libfont-afm-perl (1.20-4) ...
Selecting previously unselected package libhtml-tagset-perl.
Preparing to unpack .../11-libhtml-tagset-perl_3.20-6_all.deb ...
Unpacking libhtml-tagset-perl (3.20-6) ...
Selecting previously unselected package liburi-perl.
Preparing to unpack .../12-liburi-perl_5.27-1_all.deb ...
Unpacking liburi-perl (5.27-1) ...
Selecting previously unselected package libhtml-parser-perl:amd64.
Preparing to unpack .../13-libhtml-parser-perl_3.81-1build3_amd64.deb ...
Unpacking libhtml-parser-perl:amd64 (3.81-1build3) ...
Selecting previously unselected package libio-html-perl.
Preparing to unpack .../14-libio-html-perl_1.004-3_all.deb ...
Unpacking libio-html-perl (1.004-3) ...
Selecting previously unselected package liblwp-mediatypes-perl.
Preparing to unpack .../15-liblwp-mediatypes-perl_6.04-2_all.deb ...
Unpacking liblwp-mediatypes-perl (6.04-2) ...
Selecting previously unselected package libhttp-message-perl.
Preparing to unpack .../16-libhttp-message-perl_6.45-1ubuntu1_all.deb ...
Unpacking libhttp-message-perl (6.45-1ubuntu1) ...
Selecting previously unselected package libhtml-form-perl.
Preparing to unpack .../17-libhtml-form-perl_6.11-1_all.deb ...
Unpacking libhtml-form-perl (6.11-1) ...
Selecting previously unselected package libhtml-tree-perl.
Preparing to unpack .../18-libhtml-tree-perl_5.07-3_all.deb ...
Unpacking libhtml-tree-perl (5.07-3) ...
Selecting previously unselected package libhtml-format-perl.
Preparing to unpack .../19-libhtml-format-perl_2.16-2_all.deb ...
Unpacking libhtml-format-perl (2.16-2) ...
Selecting previously unselected package libhttp-cookies-perl.
Preparing to unpack .../20-libhttp-cookies-perl_6.11-1_all.deb ...
Unpacking libhttp-cookies-perl (6.11-1) ...
Selecting previously unselected package libhttp-daemon-perl.
Preparing to unpack .../21-libhttp-daemon-perl_6.16-1_all.deb ...
Unpacking libhttp-daemon-perl (6.16-1) ...
Selecting previously unselected package libhttp-negotiate-perl.
Preparing to unpack .../22-libhttp-negotiate-perl_6.01-2_all.deb ...
Unpacking libhttp-negotiate-perl (6.01-2) ...
Selecting previously unselected package perl-openssl-defaults:amd64.
Preparing to unpack .../23-perl-openssl-defaults_7build3_amd64.deb ...
Unpacking perl-openssl-defaults:amd64 (7build3) ...
Selecting previously unselected package libnet-ssleay-perl:amd64.
Preparing to unpack .../24-libnet-ssleay-perl_1.94-1build4_amd64.deb ...
Unpacking libnet-ssleay-perl:amd64 (1.94-1build4) ...
Selecting previously unselected package libio-socket-ssl-perl.
Preparing to unpack .../25-libio-socket-ssl-perl_2.085-1_all.deb ...
Unpacking libio-socket-ssl-perl (2.085-1) ...
Selecting previously unselected package libjs-jquery.
Preparing to unpack .../26-libjs-jquery_3.6.1+dfsg+~3.5.14-1_all.deb ...
Unpacking libjs-jquery (3.6.1+dfsg+~3.5.14-1) ...
Selecting previously unselected package libnet-http-perl.
Preparing to unpack .../27-libnet-http-perl_6.23-1_all.deb ...
Unpacking libnet-http-perl (6.23-1) ...
Selecting previously unselected package libtry-tiny-perl.
Preparing to unpack .../28-libtry-tiny-perl_0.31-2_all.deb ...
Unpacking libtry-tiny-perl (0.31-2) ...
Selecting previously unselected package libwww-robotrules-perl.
Preparing to unpack .../29-libwww-robotrules-perl_6.02-1_all.deb ...
Unpacking libwww-robotrules-perl (6.02-1) ...
Selecting previously unselected package libwww-perl.
Preparing to unpack .../30-libwww-perl_6.76-1_all.deb ...
Unpacking libwww-perl (6.76-1) ...
Selecting previously unselected package liblwp-protocol-https-perl.
Preparing to unpack .../31-liblwp-protocol-https-perl_6.13-1_all.deb ...
Unpacking liblwp-protocol-https-perl (6.13-1) ...
Selecting previously unselected package libnet-smtp-ssl-perl.
Preparing to unpack .../32-libnet-smtp-ssl-perl_1.04-2_all.deb ...
Unpacking libnet-smtp-ssl-perl (1.04-2) ...
Selecting previously unselected package libmailtools-perl.
Preparing to unpack .../33-libmailtools-perl_2.21-2_all.deb ...
Unpacking libmailtools-perl (2.21-2) ...
Selecting previously unselected package rubygems-integration.
Preparing to unpack .../34-rubygems-integration_1.18_all.deb ...
Unpacking rubygems-integration (1.18) ...
Selecting previously unselected package ruby3.2.
Preparing to unpack .../35-ruby3.2_3.2.3-1ubuntu0.24.04.3_amd64.deb ...
Unpacking ruby3.2 (3.2.3-1ubuntu0.24.04.3) ...
Selecting previously unselected package ruby-rubygems.
Preparing to unpack .../36-ruby-rubygems_3.4.20-1_all.deb ...
Unpacking ruby-rubygems (3.4.20-1) ...
Selecting previously unselected package ruby.
Preparing to unpack .../37-ruby_1%3a3.2~ubuntu1_amd64.deb ...
Unpacking ruby (1:3.2~ubuntu1) ...
Selecting previously unselected package rake.
Preparing to unpack .../38-rake_13.0.6-3_all.deb ...
Unpacking rake (13.0.6-3) ...
Selecting previously unselected package ruby-net-telnet.
Preparing to unpack .../39-ruby-net-telnet_0.2.0-1_all.deb ...
Unpacking ruby-net-telnet (0.2.0-1) ...
Selecting previously unselected package ruby-webrick.
Preparing to unpack .../40-ruby-webrick_1.8.1-1ubuntu0.1_all.deb ...
Unpacking ruby-webrick (1.8.1-1ubuntu0.1) ...
Selecting previously unselected package ruby-xmlrpc.
Preparing to unpack .../41-ruby-xmlrpc_0.3.2-2_all.deb ...
Unpacking ruby-xmlrpc (0.3.2-2) ...
Selecting previously unselected package ruby-sdbm:amd64.
Preparing to unpack .../42-ruby-sdbm_1.0.0-5build4_amd64.deb ...
Unpacking ruby-sdbm:amd64 (1.0.0-5build4) ...
Selecting previously unselected package libruby3.2:amd64.
Preparing to unpack .../43-libruby3.2_3.2.3-1ubuntu0.24.04.3_amd64.deb ...
Unpacking libruby3.2:amd64 (3.2.3-1ubuntu0.24.04.3) ...
Selecting previously unselected package libruby:amd64.
Preparing to unpack .../44-libruby_1%3a3.2~ubuntu1_amd64.deb ...
Unpacking libruby:amd64 (1:3.2~ubuntu1) ...
Selecting previously unselected package lynx-common.
Preparing to unpack .../45-lynx-common_2.9.0rel.0-2build2_all.deb ...
Unpacking lynx-common (2.9.0rel.0-2build2) ...
Selecting previously unselected package mafft.
Preparing to unpack .../46-mafft_7.505-1_amd64.deb ...
Unpacking mafft (7.505-1) ...
Selecting previously unselected package mailcap.
Preparing to unpack .../47-mailcap_3.70+nmu1ubuntu1_all.deb ...
Unpacking mailcap (3.70+nmu1ubuntu1) ...
Selecting previously unselected package unzip.
Preparing to unpack .../48-unzip_6.0-28ubuntu4.1_amd64.deb ...
Unpacking unzip (6.0-28ubuntu4.1) ...
Selecting previously unselected package zip.
Preparing to unpack .../49-zip_3.0-13ubuntu0.2_amd64.deb ...
Unpacking zip (3.0-13ubuntu0.2) ...
Selecting previously unselected package libauthen-sasl-perl.
Preparing to unpack .../50-libauthen-sasl-perl_2.1700-1_all.deb ...
Unpacking libauthen-sasl-perl (2.1700-1) ...
Selecting previously unselected package lynx.
Preparing to unpack .../51-lynx_2.9.0rel.0-2build2_amd64.deb ...
Unpacking lynx (2.9.0rel.0-2build2) ...
Setting up javascript-common (11+nmu1) ...
Setting up fonts-lato (2.015-1) ...
Setting up libfont-afm-perl (1.20-4) ...
Setting up mafft (7.505-1) ...
Setting up libclone-perl:amd64 (0.46-1build3) ...
Setting up libhtml-tagset-perl (3.20-6) ...
Setting up libauthen-sasl-perl (2.1700-1) ...
Setting up unzip (6.0-28ubuntu4.1) ...
Setting up liblwp-mediatypes-perl (6.04-2) ...
Setting up libtry-tiny-perl (0.31-2) ...
Setting up perl-openssl-defaults:amd64 (7build3) ...
Setting up libencode-locale-perl (1.05-3) ...
Setting up rubygems-integration (1.18) ...
Setting up bzip2 (1.0.8-5.1build0.1) ...
Setting up zip (3.0-13ubuntu0.2) ...
Setting up libdata-dump-perl (1.25-1) ...
Setting up libncurses6:amd64 (6.4+20240113-1ubuntu2) ...
Setting up ruby-net-telnet (0.2.0-1) ...
Setting up libio-html-perl (1.004-3) ...
Setting up lynx-common (2.9.0rel.0-2build2) ...
Setting up libtimedate-perl (2.3300-2) ...
Setting up ruby-webrick (1.8.1-1ubuntu0.1) ...
Setting up lynx (2.9.0rel.0-2build2) ...
update-alternatives: using /usr/bin/lynx to provide /usr/bin/www-browser (www-browser) in auto mode
Setting up libjs-jquery (3.6.1+dfsg+~3.5.14-1) ...
Setting up mailcap (3.70+nmu1ubuntu1) ...
Setting up ruby-xmlrpc (0.3.2-2) ...
Setting up liburi-perl (5.27-1) ...
Setting up libnet-ssleay-perl:amd64 (1.94-1build4) ...
Setting up libhttp-date-perl (6.06-1) ...
Setting up libfile-listing-perl (6.16-1) ...
Setting up libnet-http-perl (6.23-1) ...
Setting up libwww-robotrules-perl (6.02-1) ...
Setting up libhtml-parser-perl:amd64 (3.81-1build3) ...
Setting up libio-socket-ssl-perl (2.085-1) ...
Setting up libhttp-message-perl (6.45-1ubuntu1) ...
Setting up libhtml-form-perl (6.11-1) ...
Setting up libhttp-negotiate-perl (6.01-2) ...
Setting up libhttp-cookies-perl (6.11-1) ...
Setting up libhtml-tree-perl (5.07-3) ...
Setting up libhtml-format-perl (2.16-2) ...
Setting up libnet-smtp-ssl-perl (1.04-2) ...
Setting up libmailtools-perl (2.21-2) ...
Setting up libhttp-daemon-perl (6.16-1) ...
Setting up libwww-perl (6.76-1) ...
Setting up ruby-rubygems (3.4.20-1) ...
Setting up ruby3.2 (3.2.3-1ubuntu0.24.04.3) ...
Setting up liblwp-protocol-https-perl (6.13-1) ...
Setting up ruby (1:3.2~ubuntu1) ...
Setting up rake (13.0.6-3) ...
Setting up libruby3.2:amd64 (3.2.3-1ubuntu0.24.04.3) ...
Setting up libruby:amd64 (1:3.2~ubuntu1) ...
Setting up ruby-sdbm:amd64 (1.0.0-5build4) ...
Processing triggers for fontconfig (2.15.0-1.1ubuntu2) ...
Processing triggers for libc-bin (2.39-0ubuntu8.4) ...
Processing triggers for man-db (2.12.0-4build2) ...
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ mafft all_chloroplasts.fasta > aligned_sequences_mafft.fasta
nthread = 0
nthreadpair = 0
nthreadtb = 0
ppenalty_ex = 0
stacksize: 8192 kb
generating a scoring matrix for nucleotide (dist=200) ... done
Gap Penalty = -1.53, +0.00, +0.00



Making a distance matrix ..

There are 4 ambiguous characters.
    1 / 4
done.

Constructing a UPGMA tree (efffree=0) ...
    0 / 4
done.

Progressive alignment 1/2...
STEP     1 / 3
len1=151010, len2=151493, Switching to the memsave mode
STEP     2 / 3 mDP 00793 / 00793
Reallocating..done. *alloclen = 327955
STEP     3 / 3 mDP 00725 / 00725
done.

Making a distance matrix from msa..
    0 / 4
done.

Constructing a UPGMA tree (efffree=1) ...
    0 / 4
done.

Progressive alignment 2/2...
STEP     1 / 3
len1=151010, len2=151493, Switching to the memsave mode
mDP 00965 / 00965
Reallocating..done. *alloclen = 304037
STEP     2 / 3 mDP 00891 / 00891
Reallocating..done. *alloclen = 310215
STEP     3 / 3 mDP 00720 / 00720
done.

disttbfast (nuc) Version 7.505
alg=M, model=DNA200 (2), 1.53 (4.59), -0.00 (-0.00), noshift, amax=0.0
0 thread(s)


Strategy:
 FFT-NS-2 (Fast but rough)
 Progressive method (guide trees were built 2 times.)

If unsure which option to use, try 'mafft --auto input > output'.
For more information, see 'mafft --help', 'mafft --man' and the mafft page.

The default gap scoring scheme has been changed in version 7.110 (2013 Oct).
It tends to insert more gaps into gap-rich regions than previous versions.
To disable this change, add the --leavegappyregion option.

(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ ls -lh aligned_sequences_mafft.fasta
-rw-r--r-- 1 suki suki 724K Feb 18 23:21 aligned_sequences_mafft.fasta
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ nano vatica_xsbn.fna
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ head -n 20 vatica_species.fna
head: cannot open 'vatica_species.fna' for reading: No such file or directory
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ nano vatica_xsbn.fna
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ ls
MT934442.1.fna  aligned_sequences_mafft.fasta  vatica_xsbn.fna
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ head -n 20 vatica_species.fna
head: cannot open 'vatica_species.fna' for reading: No such file or directory
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ head -n 20 vatica_xsbn.fna
TTATAATTTTTTCACTTTCCATATATAGAAATAGAAACAGATATACTAGAAACGACATCTCTTATGTCAA
TGACACGAAAGGGGTATGAAATGAATGGAATTGGGATATGGATGGAATATAATGAAATAGAGGCGCTTTG
AGGTTCCCTATGACATGAGGCATGTAACAGAGCCACTACGAAGAAGTTACGGGGGTTACGAAGGAAACCT
CGAGTTCATATTGGTCATGGGTTGAGAACGGGAATTGAACTCGATGAGATCGAATCTCCCGTTGTTCCTC
AATAGCTCAGTGGTAGAGCGGTCGGCTGTTAACCGACTGGTCGTAGGTTCGAATCCTACTTGGGGAGATT
TGATTCATTCCGAATTAAAGAATTAAGAATGTCAGAATGAAAGGGTTCGGTTCGCTTTGACCGTTAAGAG
TCGCGTTCCCTGCGTCTTTGTTTTTATTGCAGTCTATCTCATCGTATCCCATTCTGTTCTGCGCTATTTG
AGAATCACCGTCAATACCTCGCCTCGGTGTAGGAATCCTTTGTTCCATAATCCTGTGGGGCTATTTACAA
CCAGCCAATTAAGAATTCTCAGATGTACTAGTACTAACAAATGCATCAAAGATTCAGTCATCGATTCTCC
CGAGAGGCCACAATTACCGCGAGCAAACACATTAATTTAATGACGAGGAGCGCATTTTGGCTATGCTACT
AATACTTGTACTTACTCTGCTATTCTGCCCAAGCCTGGCTGAGGAAGAGTTACGGGGCGTAAAACCAAAA
AAATATGCTTATGGGGTTATACTATATTTAAAAATAATAGAAATAATATAAATAATAATAAATCAAAGGG
CCATTCCATTTCGGCAAAAGACCCACGCCCAAGTTACATAGCTTGGGGGTCCGCTATCCCGATCATGATT
TCCCTACCCCCAGAGGAAAAGGTCCTTCCCTTTTGGGCCGGTTGTGGGCGAGGAGGGATTCGAACCCCCG
ACACCGTGGTTCGTAGCCACGTGCTCTAATCCTCTGAGCTACAGGCCCCACCTCGTCTCCACTGGATCTG
CTCCTAGGAGTCCCCTAAAAAAAGGAACTTTCCCCCTCCCCAGCCATTTCGGGTTAAGAAGATGTGAAAG
CGCCTTTCTCTCTATAAGAACGGTGCGTTCCGAGGTGTGAAGTGGGAGAGAGGGGATTTCATAATTGGGG
TTTTGAATAAGACGACCTTTTCATTTTTCATTTTTTTCTTTTTCATATTGAAAAAGGAATAAGAATGAGA
GGTTTCAAGTTTTTTATCATCCTGGCGTCGAGCTATTTTTCCGCAGGGCCTCCCCTACAGTATCGTCACC
GCAGTAGAGTTTAACCACCAAGTTCGGGATGGATTGGTGTTGTTCCTCTACGCCTAGGACACCAGAATAT
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ cat *.fna > all_chloroplasts.fasta
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ grep ">" all_chloroplasts.fasta
>MT934442.1 Vatica guangxiensis chloroplast, complete genome
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ nano vatica_xsbn.fna
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ head -n 20 vatica_xsbn.fna
>MZ397800.1 Vatica xishuangbannaensis chloroplast, complete genome
TTATAATTTTTTCACTTTCCATATATAGAAATAGAAACAGATATACTAGAAACGACATCTCTTATGTCAA
TGACACGAAAGGGGTATGAAATGAATGGAATTGGGATATGGATGGAATATAATGAAATAGAGGCGCTTTG
AGGTTCCCTATGACATGAGGCATGTAACAGAGCCACTACGAAGAAGTTACGGGGGTTACGAAGGAAACCT
CGAGTTCATATTGGTCATGGGTTGAGAACGGGAATTGAACTCGATGAGATCGAATCTCCCGTTGTTCCTC
AATAGCTCAGTGGTAGAGCGGTCGGCTGTTAACCGACTGGTCGTAGGTTCGAATCCTACTTGGGGAGATT
TGATTCATTCCGAATTAAAGAATTAAGAATGTCAGAATGAAAGGGTTCGGTTCGCTTTGACCGTTAAGAG
TCGCGTTCCCTGCGTCTTTGTTTTTATTGCAGTCTATCTCATCGTATCCCATTCTGTTCTGCGCTATTTG
AGAATCACCGTCAATACCTCGCCTCGGTGTAGGAATCCTTTGTTCCATAATCCTGTGGGGCTATTTACAA
CCAGCCAATTAAGAATTCTCAGATGTACTAGTACTAACAAATGCATCAAAGATTCAGTCATCGATTCTCC
CGAGAGGCCACAATTACCGCGAGCAAACACATTAATTTAATGACGAGGAGCGCATTTTGGCTATGCTACT
AATACTTGTACTTACTCTGCTATTCTGCCCAAGCCTGGCTGAGGAAGAGTTACGGGGCGTAAAACCAAAA
AAATATGCTTATGGGGTTATACTATATTTAAAAATAATAGAAATAATATAAATAATAATAAATCAAAGGG
CCATTCCATTTCGGCAAAAGACCCACGCCCAAGTTACATAGCTTGGGGGTCCGCTATCCCGATCATGATT
TCCCTACCCCCAGAGGAAAAGGTCCTTCCCTTTTGGGCCGGTTGTGGGCGAGGAGGGATTCGAACCCCCG
ACACCGTGGTTCGTAGCCACGTGCTCTAATCCTCTGAGCTACAGGCCCCACCTCGTCTCCACTGGATCTG
CTCCTAGGAGTCCCCTAAAAAAAGGAACTTTCCCCCTCCCCAGCCATTTCGGGTTAAGAAGATGTGAAAG
CGCCTTTCTCTCTATAAGAACGGTGCGTTCCGAGGTGTGAAGTGGGAGAGAGGGGATTTCATAATTGGGG
TTTTGAATAAGACGACCTTTTCATTTTTCATTTTTTTCTTTTTCATATTGAAAAAGGAATAAGAATGAGA
GGTTTCAAGTTTTTTATCATCCTGGCGTCGAGCTATTTTTCCGCAGGGCCTCCCCTACAGTATCGTCACC
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ ^C
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ head -n 20 vatica_xsbn.fna
>MZ397800.1 Vatica xishuangbannaensis chloroplast, complete genome
TTATAATTTTTTCACTTTCCATATATAGAAATAGAAACAGATATACTAGAAACGACATCTCTTATGTCAA
TGACACGAAAGGGGTATGAAATGAATGGAATTGGGATATGGATGGAATATAATGAAATAGAGGCGCTTTG
AGGTTCCCTATGACATGAGGCATGTAACAGAGCCACTACGAAGAAGTTACGGGGGTTACGAAGGAAACCT
CGAGTTCATATTGGTCATGGGTTGAGAACGGGAATTGAACTCGATGAGATCGAATCTCCCGTTGTTCCTC
AATAGCTCAGTGGTAGAGCGGTCGGCTGTTAACCGACTGGTCGTAGGTTCGAATCCTACTTGGGGAGATT
TGATTCATTCCGAATTAAAGAATTAAGAATGTCAGAATGAAAGGGTTCGGTTCGCTTTGACCGTTAAGAG
TCGCGTTCCCTGCGTCTTTGTTTTTATTGCAGTCTATCTCATCGTATCCCATTCTGTTCTGCGCTATTTG
AGAATCACCGTCAATACCTCGCCTCGGTGTAGGAATCCTTTGTTCCATAATCCTGTGGGGCTATTTACAA
CCAGCCAATTAAGAATTCTCAGATGTACTAGTACTAACAAATGCATCAAAGATTCAGTCATCGATTCTCC
CGAGAGGCCACAATTACCGCGAGCAAACACATTAATTTAATGACGAGGAGCGCATTTTGGCTATGCTACT
AATACTTGTACTTACTCTGCTATTCTGCCCAAGCCTGGCTGAGGAAGAGTTACGGGGCGTAAAACCAAAA
AAATATGCTTATGGGGTTATACTATATTTAAAAATAATAGAAATAATATAAATAATAATAAATCAAAGGG
CCATTCCATTTCGGCAAAAGACCCACGCCCAAGTTACATAGCTTGGGGGTCCGCTATCCCGATCATGATT
TCCCTACCCCCAGAGGAAAAGGTCCTTCCCTTTTGGGCCGGTTGTGGGCGAGGAGGGATTCGAACCCCCG
ACACCGTGGTTCGTAGCCACGTGCTCTAATCCTCTGAGCTACAGGCCCCACCTCGTCTCCACTGGATCTG
CTCCTAGGAGTCCCCTAAAAAAAGGAACTTTCCCCCTCCCCAGCCATTTCGGGTTAAGAAGATGTGAAAG
CGCCTTTCTCTCTATAAGAACGGTGCGTTCCGAGGTGTGAAGTGGGAGAGAGGGGATTTCATAATTGGGG
TTTTGAATAAGACGACCTTTTCATTTTTCATTTTTTTCTTTTTCATATTGAAAAAGGAATAAGAATGAGA
GGTTTCAAGTTTTTTATCATCCTGGCGTCGAGCTATTTTTCCGCAGGGCCTCCCCTACAGTATCGTCACC
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ cat *.fna > all_chloroplasts.fasta
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ grep ">" all_chloroplasts.fasta
>MT934442.1 Vatica guangxiensis chloroplast, complete genome
>MZ397800.1 Vatica xishuangbannaensis chloroplast, complete genome
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ mafft all_chloroplasts.fasta > aligned_sequences_mafft.fasta
nthread = 0
nthreadpair = 0
nthreadtb = 0
ppenalty_ex = 0
stacksize: 8192 kb
generating a scoring matrix for nucleotide (dist=200) ... done
Gap Penalty = -1.53, +0.00, +0.00



Making a distance matrix ..

There are 4 ambiguous characters.
    1 / 2
done.

Constructing a UPGMA tree (efffree=1) ...
    0 / 2
done.

Progressive alignment 1/1...
STEP     1 / 1
len1=151010, len2=151011, Switching to the memsave mode
mDP 00817 / 00817
done.

disttbfast (nuc) Version 7.505
alg=M, model=DNA200 (2), 1.53 (4.59), -0.00 (-0.00), noshift, amax=0.0
0 thread(s)


Strategy:
 FFT-NS-1 (Very fast but very rough)
 Progressive method (rough guide tree was used.)

If unsure which option to use, try 'mafft --auto input > output'.
For more information, see 'mafft --help', 'mafft --man' and the mafft page.

The default gap scoring scheme has been changed in version 7.110 (2013 Oct).
It tends to insert more gaps into gap-rich regions than previous versions.
To disable this change, add the --leavegappyregion option.

(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ ls -lh aligned_sequences_mafft.fasta
head -n 20 aligned_sequences_mafft.fasta
-rw-r--r-- 1 suki suki 348K Feb 18 23:39 aligned_sequences_mafft.fasta
>MT934442.1 Vatica guangxiensis chloroplast, complete genome
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
------------------------------------------------------------
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ sudo apt install aliview
[sudo] password for suki:
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
E: Unable to locate package aliview
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$ wget https://ormbunkar.se/aliview/downloads/AliView.jar -O AliView.jar
--2025-02-18 23:41:54--  https://ormbunkar.se/aliview/downloads/AliView.jar
Resolving ormbunkar.se (ormbunkar.se)... 130.238.44.8
Connecting to ormbunkar.se (ormbunkar.se)|130.238.44.8|:443... connected.
HTTP request sent, awaiting response... 404 Not Found
2025-02-18 23:41:55 ERROR 404: Not Found.

(base) suki@LAPTOP-5PMP3V9O:~/phylo-class/hw-aligning-your-own-data$