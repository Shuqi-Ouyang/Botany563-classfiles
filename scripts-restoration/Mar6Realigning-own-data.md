Microsoft Windows [Version 10.0.26100.3194]
(c) Microsoft Corporation. All rights reserved.

C:\Users\欧阳葭>wsl
Welcome to Ubuntu 24.04.2 LTS (GNU/Linux 5.15.167.4-microsoft-standard-WSL2 x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Thu Mar  6 11:31:53 CST 2025

  System load:  0.0                 Processes:             49
  Usage of /:   0.3% of 1006.85GB   Users logged in:       0
  Memory usage: 3%                  IPv4 address for eth0: 172.19.133.12
  Swap usage:   0%

 * Strictly confined Kubernetes makes edge and IoT secure. Learn how MicroK8s
   just raised the bar for easy, resilient and secure K8s cluster deployment.

   https://ubuntu.com/engage/secure-kubernetes-at-the-edge

This message is shown once a day. To disable it please create the
/home/suki/.hushlogin file.
(base) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ cd /home/suki/phylo-class/
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class$ ls
D_Dataver1.fasta  hw-aligning-your-own-data  installation-exercise
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class$ mafft --auto D_Dataver1.fasta > aligned_sequences.fasta
nthread = 0
nthreadpair = 0
nthreadtb = 0
ppenalty_ex = 0
stacksize: 8192 kb
generating a scoring matrix for nucleotide (dist=200) ... done
Gap Penalty = -1.53, +0.00, +0.00



Making a distance matrix ..

There are 17 ambiguous characters.
    1 / 12
done.

Constructing a UPGMA tree (efffree=0) ...
   10 / 12
done.

Progressive alignment 1/2...
STEP     1 / 11
len1=151493, len2=151010, Switching to the memsave mode
STEP     4 / 11 mDP 00759 / 00759
Reallocating..done. *alloclen = 327955
STEP     6 / 11 mDP 00714 / 00714
Reallocating..done. *alloclen = 329836
STEP     7 / 11 mDP 00594 / 00594
Reallocating..done. *alloclen = 335642
STEP     8 / 11 mDP 00591 / 00591
Reallocating..done. *alloclen = 362014
STEP     9 / 11 mDP 00519 / 00519
Reallocating..done. *alloclen = 367507
STEP    11 / 11 mDP 00142 / 00142
done.

Making a distance matrix from msa..
    0 / 12
done.

Constructing a UPGMA tree (efffree=1) ...
   10 / 12
done.

Progressive alignment 2/2...
STEP     1 / 11
len1=151493, len2=151010, Switching to the memsave mode
STEP     4 / 11 mDP 00891 / 00891
Reallocating..done. *alloclen = 311738
STEP     6 / 11 mDP 00697 / 00697
Reallocating..done. *alloclen = 313471
STEP     7 / 11 mDP 00630 / 00630
Reallocating..done. *alloclen = 316092
STEP     9 / 11 mDP 00657 / 00657
Reallocating..done. *alloclen = 327996
STEP    10 / 11 mDP 00496 / 00496
Reallocating..done. *alloclen = 348653
STEP    11 / 11 mDP 00141 / 00141
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

(base) suki@LAPTOP-5PMP3V9O:~/phylo-class$ cd home
-bash: cd: home: No such file or directory
(base) suki@LAPTOP-5PMP3V9O:~/phylo-class$ cd ../
(base) suki@LAPTOP-5PMP3V9O:~$ conda create -n fasta_clean python=3.9 -y
conda activate fasta_clean
Retrieving notices: done
Channels:
 - defaults
Platform: linux-64
Collecting package metadata (repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: /home/suki/miniconda3/envs/fasta_clean

  added / updated specs:
    - python=3.9


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    ca-certificates-2025.2.25  |       h06a4308_0         129 KB
    openssl-3.0.16             |       h5eee18b_0         5.2 MB
    pip-25.0                   |   py39h06a4308_0         2.3 MB
    python-3.9.21              |       he870216_1        25.1 MB
    setuptools-75.8.0          |   py39h06a4308_0         1.6 MB
    wheel-0.45.1               |   py39h06a4308_0         114 KB
    xz-5.6.4                   |       h5eee18b_1         567 KB
    ------------------------------------------------------------
                                           Total:        35.0 MB

The following NEW packages will be INSTALLED:

  _libgcc_mutex      pkgs/main/linux-64::_libgcc_mutex-0.1-main
  _openmp_mutex      pkgs/main/linux-64::_openmp_mutex-5.1-1_gnu
  ca-certificates    pkgs/main/linux-64::ca-certificates-2025.2.25-h06a4308_0
  ld_impl_linux-64   pkgs/main/linux-64::ld_impl_linux-64-2.40-h12ee557_0
  libffi             pkgs/main/linux-64::libffi-3.4.4-h6a678d5_1
  libgcc-ng          pkgs/main/linux-64::libgcc-ng-11.2.0-h1234567_1
  libgomp            pkgs/main/linux-64::libgomp-11.2.0-h1234567_1
  libstdcxx-ng       pkgs/main/linux-64::libstdcxx-ng-11.2.0-h1234567_1
  ncurses            pkgs/main/linux-64::ncurses-6.4-h6a678d5_0
  openssl            pkgs/main/linux-64::openssl-3.0.16-h5eee18b_0
  pip                pkgs/main/linux-64::pip-25.0-py39h06a4308_0
  python             pkgs/main/linux-64::python-3.9.21-he870216_1
  readline           pkgs/main/linux-64::readline-8.2-h5eee18b_0
  setuptools         pkgs/main/linux-64::setuptools-75.8.0-py39h06a4308_0
  sqlite             pkgs/main/linux-64::sqlite-3.45.3-h5eee18b_0
  tk                 pkgs/main/linux-64::tk-8.6.14-h39e8969_0
  tzdata             pkgs/main/noarch::tzdata-2025a-h04d1e81_0
  wheel              pkgs/main/linux-64::wheel-0.45.1-py39h06a4308_0
  xz                 pkgs/main/linux-64::xz-5.6.4-h5eee18b_1
  zlib               pkgs/main/linux-64::zlib-1.2.13-h5eee18b_1



Downloading and Extracting Packages:

Preparing transaction: done
Verifying transaction: done
Executing transaction: done
#
# To activate this environment, use
#
#     $ conda activate fasta_clean
#
# To deactivate an active environment, use
#
#     $ conda deactivate

(fasta_clean) suki@LAPTOP-5PMP3V9O:~$ pip install biopython
Collecting biopython
  Downloading biopython-1.85-cp39-cp39-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (13 kB)
Collecting numpy (from biopython)
  Downloading numpy-2.0.2-cp39-cp39-manylinux_2_17_x86_64.manylinux2014_x86_64.whl.metadata (60 kB)
Downloading biopython-1.85-cp39-cp39-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (3.2 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 3.2/3.2 MB 11.2 MB/s eta 0:00:00
Downloading numpy-2.0.2-cp39-cp39-manylinux_2_17_x86_64.manylinux2014_x86_64.whl (19.5 MB)
   ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━ 19.5/19.5 MB 14.2 MB/s eta 0:00:00
Installing collected packages: numpy, biopython
Successfully installed biopython-1.85 numpy-2.0.2
(fasta_clean) suki@LAPTOP-5PMP3V9O:~$ from Bio import SeqIO

# 输入文件和输出文件
input_file = "C:/Users/欧阳葭/Desktop/aligned_sequences.fasta"
output_file = "C:/Users/欧阳葭/Desktop/fixed_aligned_sequences.fasta"

# 处理 FASTA 文件
with open(input_file, "r") as infile, open(output_file, "w") as outfile:
    for record in SeqIO.parse(infile, "fasta"):
        record.id = record.id.split()[0]  # 只保留 accession number
        record.description = ""  # 清空描述信息
        SeqIO.write(record, outfile, "fasta")

print(f"✅ 处理完成！已生成新文件: {output_file}")
Command 'from' not found, but can be installed with:
sudo apt install mailutils
input_file: command not found
output_file: command not found
-bash: syntax error near unexpected token `('
-bash: syntax error near unexpected token `('
-bash: syntax error near unexpected token `('
record.description: command not found
-bash: syntax error near unexpected token `record,'
-bash: syntax error near unexpected token `f"✅ 处理完成！已生成新文件: {output_file}"'
(fasta_clean) suki@LAPTOP-5PMP3V9O:~$ python -c "from Bio import SeqIO; infile, outfile = 'C:/Users/欧阳葭/Desktop/aligned_sequences.fasta', 'C:/Users/欧阳葭/Desktop/fixed_aligned_sequences.fasta'; with open(infile, 'r') as in_f, open(outfile, 'w') as out_f: [SeqIO.write(r._replace(id=r.id.split()[0], description=''), out_f, 'fasta') for r in SeqIO.parse(in_f, 'fasta')]; print('✅ 处理完成！')"
  File "<string>", line 1
    from Bio import SeqIO; infile, outfile = 'C:/Users/欧阳葭/Desktop/aligned_sequences.fasta', 'C:/Users/欧阳葭/Desktop/fixed_aligned_sequences.fasta'; with open(infile, 'r') as in_f, open(outfile, 'w') as out_f: [SeqIO.write(r._replace(id=r.id.split()[0], description=''), out_f, 'fasta') for r in SeqIO.parse(in_f, 'fasta')]; print('✅ 处理完成！')
                                                                                                                                                               ^
SyntaxError: invalid syntax
(fasta_clean) suki@LAPTOP-5PMP3V9O:~$ cd phylo-class
(fasta_clean) suki@LAPTOP-5PMP3V9O:~/phylo-class$ python -c "from Bio import SeqIO; infile, outfile = 'C:/Users/欧阳葭/Desktop/aligned_sequences.fasta', 'C:/Users/欧阳葭/Desktop/fixed_aligned_sequences.fasta'; with open(infile, 'r') as in_f, open(outfile, 'w') as out_f: [SeqIO.write(r._replace(id=r.id.split()[0], description=''), out_f, 'fasta') for r in SeqIO.parse(in_f, 'fasta')]; print('✅ 处理完成！')"
  File "<string>", line 1
    from Bio import SeqIO; infile, outfile = 'C:/Users/欧阳葭/Desktop/aligned_sequences.fasta', 'C:/Users/欧阳葭/Desktop/fixed_aligned_sequences.fasta'; with open(infile, 'r') as in_f, open(outfile, 'w') as out_f: [SeqIO.write(r._replace(id=r.id.split()[0], description=''), out_f, 'fasta') for r in SeqIO.parse(in_f, 'fasta')]; print('✅ 处理完成！')
                                                                                                                                                               ^
SyntaxError: invalid syntax
(fasta_clean) suki@LAPTOP-5PMP3V9O:~/phylo-class$ ^C
(fasta_clean) suki@LAPTOP-5PMP3V9O:~/phylo-class$ nano clean_fasta.py
(fasta_clean) suki@LAPTOP-5PMP3V9O:~/phylo-class$ conda activate fasta_clean
python clean_fasta.py
✅ 处理完成！新文件保存至: /mnt/c/Users/欧阳葭/Desktop/fixed_aligned_sequences.fasta
✅ 处理完成！新文件保存至: /mnt/c/Users/欧阳葭/Desktop/fixed_aligned_sequences.fasta
(fasta_clean) suki@LAPTOP-5PMP3V9O:~/phylo-class$