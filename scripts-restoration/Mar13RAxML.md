Microsoft Windows [Version 10.0.26100.3476]
(c) Microsoft Corporation. All rights reserved.

C:\Users\欧阳葭>wsl
Welcome to Ubuntu 24.04.2 LTS (GNU/Linux 5.15.167.4-microsoft-standard-WSL2 x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Thu Mar 13 13:06:49 CDT 2025

  System load:  0.08                Processes:             78
  Usage of /:   0.3% of 1006.85GB   Users logged in:       0
  Memory usage: 3%                  IPv4 address for eth0: 172.19.133.12
  Swap usage:   0%

 * Strictly confined Kubernetes makes edge and IoT secure. Learn how MicroK8s
   just raised the bar for easy, resilient and secure K8s cluster deployment.

   https://ubuntu.com/engage/secure-kubernetes-at-the-edge

This message is shown once a day. To disable it please create the
/home/suki/.hushlogin file.
(base) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ pwd
/mnt/c/Users/欧阳葭
(base) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ conda create -n iqtree-env -y
Retrieving notices: done
Channels:
 - defaults
Platform: linux-64
Collecting package metadata (repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: /home/suki/miniconda3/envs/iqtree-env




Downloading and Extracting Packages:

Preparing transaction: done
Verifying transaction: done
Executing transaction: done
#
# To activate this environment, use
#
#     $ conda activate iqtree-env
#
# To deactivate an active environment, use
#
#     $ conda deactivate

(base) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ conda activate iqtree-env
(iqtree-env) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ conda install -c bioconda iqtree
Channels:
 - bioconda
 - defaults
Platform: linux-64
Collecting package metadata (repodata.json): done
Solving environment: done

## Package Plan ##

  environment location: /home/suki/miniconda3/envs/iqtree-env

  added / updated specs:
    - iqtree


The following packages will be downloaded:

    package                    |            build
    ---------------------------|-----------------
    iqtree-2.1.4_beta          |       hdcc8f71_0         6.4 MB  bioconda
    ------------------------------------------------------------
                                           Total:         6.4 MB

The following NEW packages will be INSTALLED:

  _libgcc_mutex      pkgs/main/linux-64::_libgcc_mutex-0.1-main
  _openmp_mutex      pkgs/main/linux-64::_openmp_mutex-5.1-1_gnu
  iqtree             bioconda/linux-64::iqtree-2.1.4_beta-hdcc8f71_0
  libgcc-ng          pkgs/main/linux-64::libgcc-ng-11.2.0-h1234567_1
  libgomp            pkgs/main/linux-64::libgomp-11.2.0-h1234567_1
  libstdcxx-ng       pkgs/main/linux-64::libstdcxx-ng-11.2.0-h1234567_1
  zlib               pkgs/main/linux-64::zlib-1.2.13-h5eee18b_1


Proceed ([y]/n)? y


Downloading and Extracting Packages:

Preparing transaction: done
Verifying transaction: done
Executing transaction: done
(iqtree-env) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ iqtree --version
IQ-TREE multicore version 2.1.4-beta COVID-edition for Linux 64-bit built Jun 24 2021
Developed by Bui Quang Minh, James Barbetti, Nguyen Lam Tung,
Olga Chernomor, Heiko Schmidt, Dominik Schrempf, Michael Woodhams.

(iqtree-env) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ conda activate raxml-n
g-env
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ raxml-ng --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta \
         --model GTR+G \
         --prefix test_run \
         --seed 12345

RAxML-NG v. 0.9.0 released on 20.05.2019 by The Exelixis Lab.
Developed by: Alexey M. Kozlov and Alexandros Stamatakis.
Contributors: Diego Darriba, Tomas Flouri, Benoit Morel, Sarah Lutteropp, Ben Bettisworth.
Latest version: https://github.com/amkozlov/raxml-ng
Questions/problems/suggestions? Please visit: https://groups.google.com/forum/#!forum/raxml

RAxML-NG was called at 13-Mar-2025 13:16:34 as follows:

raxml-ng --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta --model GTR+G --prefix test_run --seed 12345

Analysis options:
  run mode: ML tree search
  start tree(s): random (10) + parsimony (10)
  random seed: 12345
  tip-inner: OFF
  pattern compression: ON
  per-rate scalers: OFF
  site repeats: ON
  fast spr radius: AUTO
  spr subtree cutoff: 1.000000
  branch lengths: proportional (ML estimate, algorithm: NR-FAST)
  SIMD kernels: AVX2
  parallelization: PTHREADS (11 threads), thread pinning: OFF

[00:00:00] Reading alignment from file: /home/suki/phylo-class/fixed_aligned_sequences.fasta
[00:00:00] Loaded alignment with 12 taxa and 267535 sites

Alignment comprises 1 partitions and 5658 patterns

Partition 0: noname
Model: GTR+FO+G4m
Alignment sites / patterns: 267535 / 5658
Gaps: 43.33 %
Invariant sites: 90.87 %


NOTE: Binary MSA file created: test_run.raxml.rba


WARNING: You might be using too many threads (11) for your alignment with 5658 unique patterns.
NOTE:    For the optimal throughput, please consider using fewer threads
NOTE:    and parallelize across starting trees/bootstrap replicates.
NOTE:    As a general rule-of-thumb, please assign at least 200-1000 alignment patterns per thread.

[00:00:00] Generating 10 random starting tree(s) with 12 taxa
[00:00:00] Generating 10 parsimony starting tree(s) with 12 taxa
[00:00:00] Data distribution: max. partitions/sites/weight per thread: 1 / 515 / 8240

Starting ML tree search with 20 distinct starting trees

[00:00:00 -740053.624458] Initial branch length optimization
[00:00:00 -613037.248015] Model parameter optimization (eps = 10.000000)
[00:00:00 -580147.335205] AUTODETECT spr round 1 (radius: 5)
[00:00:00 -530184.813379] AUTODETECT spr round 2 (radius: 10)
[00:00:00 -530184.812992] SPR radius for FAST iterations: 5 (autodetect)
[00:00:00 -530184.812992] Model parameter optimization (eps = 3.000000)
[00:00:00 -529567.696377] FAST spr round 1 (radius: 5)
[00:00:01 -528905.985493] FAST spr round 2 (radius: 5)
[00:00:01 -528905.985441] Model parameter optimization (eps = 1.000000)
[00:00:01 -528899.801768] SLOW spr round 1 (radius: 5)
[00:00:01 -528899.801704] SLOW spr round 2 (radius: 10)
[00:00:01 -528899.801704] Model parameter optimization (eps = 0.100000)

[00:00:01] ML tree search #1, logLikelihood: -528899.801508

[00:00:01 -738516.832559] Initial branch length optimization
[00:00:01 -608914.228423] Model parameter optimization (eps = 10.000000)
[00:00:02 -576465.364320] AUTODETECT spr round 1 (radius: 5)
[00:00:02 -529626.307664] AUTODETECT spr round 2 (radius: 10)
[00:00:02 -529626.303215] SPR radius for FAST iterations: 5 (autodetect)
[00:00:02 -529626.303215] Model parameter optimization (eps = 3.000000)
[00:00:02 -528909.920270] FAST spr round 1 (radius: 5)
[00:00:02 -528899.808955] FAST spr round 2 (radius: 5)
[00:00:02 -528899.808955] Model parameter optimization (eps = 1.000000)
[00:00:02 -528899.801917] SLOW spr round 1 (radius: 5)
[00:00:02 -528899.801916] SLOW spr round 2 (radius: 10)
[00:00:03 -528899.801916] Model parameter optimization (eps = 0.100000)

[00:00:03] ML tree search #2, logLikelihood: -528899.801684

[00:00:03 -732032.956754] Initial branch length optimization
[00:00:03 -616264.369598] Model parameter optimization (eps = 10.000000)
[00:00:03 -586349.860293] AUTODETECT spr round 1 (radius: 5)
[00:00:03 -530037.114476] AUTODETECT spr round 2 (radius: 10)
[00:00:03 -530037.114217] SPR radius for FAST iterations: 5 (autodetect)
[00:00:03 -530037.114217] Model parameter optimization (eps = 3.000000)
[00:00:03 -529415.832289] FAST spr round 1 (radius: 5)
[00:00:03 -528901.897007] FAST spr round 2 (radius: 5)
[00:00:03 -528901.897007] Model parameter optimization (eps = 1.000000)
[00:00:03 -528899.802107] SLOW spr round 1 (radius: 5)
[00:00:04 -528899.802104] SLOW spr round 2 (radius: 10)
[00:00:04 -528899.802104] Model parameter optimization (eps = 0.100000)

[00:00:04] ML tree search #3, logLikelihood: -528899.801601

[00:00:04 -713328.288952] Initial branch length optimization
[00:00:04 -581764.443562] Model parameter optimization (eps = 10.000000)
[00:00:04 -557137.249974] AUTODETECT spr round 1 (radius: 5)
[00:00:04 -531016.285026] AUTODETECT spr round 2 (radius: 10)
[00:00:04 -531016.284533] SPR radius for FAST iterations: 5 (autodetect)
[00:00:04 -531016.284533] Model parameter optimization (eps = 3.000000)
[00:00:04 -530513.238753] FAST spr round 1 (radius: 5)
[00:00:04 -528944.389191] FAST spr round 2 (radius: 5)
[00:00:04 -528944.389095] Model parameter optimization (eps = 1.000000)
[00:00:04 -528899.806234] SLOW spr round 1 (radius: 5)
[00:00:05 -528899.806037] SLOW spr round 2 (radius: 10)
[00:00:05 -528899.806037] Model parameter optimization (eps = 0.100000)

[00:00:05] ML tree search #4, logLikelihood: -528899.803538

[00:00:05 -745094.085999] Initial branch length optimization
[00:00:05 -623369.896262] Model parameter optimization (eps = 10.000000)
[00:00:05 -586518.529408] AUTODETECT spr round 1 (radius: 5)
[00:00:05 -529700.509680] AUTODETECT spr round 2 (radius: 10)
[00:00:05 -529700.509667] SPR radius for FAST iterations: 5 (autodetect)
[00:00:05 -529700.509667] Model parameter optimization (eps = 3.000000)
[00:00:05 -528899.802029] FAST spr round 1 (radius: 5)
[00:00:05 -528899.801972] Model parameter optimization (eps = 1.000000)
[00:00:05 -528899.801595] SLOW spr round 1 (radius: 5)
[00:00:06 -528899.801595] SLOW spr round 2 (radius: 10)
[00:00:06 -528899.801595] Model parameter optimization (eps = 0.100000)

[00:00:06] ML tree search #5, logLikelihood: -528899.801588

[00:00:06 -742442.892087] Initial branch length optimization
[00:00:06 -617371.863100] Model parameter optimization (eps = 10.000000)
[00:00:06 -585029.518552] AUTODETECT spr round 1 (radius: 5)
[00:00:06 -530393.693586] AUTODETECT spr round 2 (radius: 10)
[00:00:06 -530393.693485] SPR radius for FAST iterations: 5 (autodetect)
[00:00:06 -530393.693485] Model parameter optimization (eps = 3.000000)
[00:00:06 -529911.565191] FAST spr round 1 (radius: 5)
[00:00:06 -528926.607937] FAST spr round 2 (radius: 5)
[00:00:06 -528926.607937] Model parameter optimization (eps = 1.000000)
[00:00:06 -528899.802932] SLOW spr round 1 (radius: 5)
[00:00:07 -528899.802917] SLOW spr round 2 (radius: 10)
[00:00:07 -528899.802917] Model parameter optimization (eps = 0.100000)

[00:00:07] ML tree search #6, logLikelihood: -528899.801674

[00:00:07 -740597.478289] Initial branch length optimization
[00:00:07 -609310.334124] Model parameter optimization (eps = 10.000000)
[00:00:07 -577188.194302] AUTODETECT spr round 1 (radius: 5)
[00:00:07 -529599.307594] AUTODETECT spr round 2 (radius: 10)
[00:00:07 -529599.307585] SPR radius for FAST iterations: 5 (autodetect)
[00:00:07 -529599.307585] Model parameter optimization (eps = 3.000000)
[00:00:07 -528899.801721] FAST spr round 1 (radius: 5)
[00:00:07 -528899.801719] Model parameter optimization (eps = 1.000000)
[00:00:07 -528899.801497] SLOW spr round 1 (radius: 5)
[00:00:08 -528899.801497] SLOW spr round 2 (radius: 10)
[00:00:08 -528899.801497] Model parameter optimization (eps = 0.100000)

[00:00:08] ML tree search #7, logLikelihood: -528899.801484

[00:00:08 -743115.846362] Initial branch length optimization
[00:00:08 -618037.767655] Model parameter optimization (eps = 10.000000)
[00:00:08 -584036.361135] AUTODETECT spr round 1 (radius: 5)
[00:00:08 -529644.104554] AUTODETECT spr round 2 (radius: 10)
[00:00:08 -529644.104532] SPR radius for FAST iterations: 5 (autodetect)
[00:00:08 -529644.104532] Model parameter optimization (eps = 3.000000)
[00:00:08 -528899.802037] FAST spr round 1 (radius: 5)
[00:00:08 -528899.802029] Model parameter optimization (eps = 1.000000)
[00:00:08 -528899.801681] SLOW spr round 1 (radius: 5)
[00:00:09 -528899.801681] SLOW spr round 2 (radius: 10)
[00:00:09 -528899.801681] Model parameter optimization (eps = 0.100000)

[00:00:09] ML tree search #8, logLikelihood: -528899.801674

[00:00:09 -742709.122104] Initial branch length optimization
[00:00:09 -613314.715333] Model parameter optimization (eps = 10.000000)
[00:00:09 -578805.483557] AUTODETECT spr round 1 (radius: 5)
[00:00:09 -531009.209423] AUTODETECT spr round 2 (radius: 10)
[00:00:09 -531009.207189] SPR radius for FAST iterations: 5 (autodetect)
[00:00:09 -531009.207189] Model parameter optimization (eps = 3.000000)
[00:00:09 -530513.252357] FAST spr round 1 (radius: 5)
[00:00:09 -528944.385464] FAST spr round 2 (radius: 5)
[00:00:09 -528944.385375] Model parameter optimization (eps = 1.000000)
[00:00:09 -528899.805515] SLOW spr round 1 (radius: 5)
[00:00:10 -528899.805483] SLOW spr round 2 (radius: 10)
[00:00:10 -528899.805483] Model parameter optimization (eps = 0.100000)

[00:00:10] ML tree search #9, logLikelihood: -528899.802504

[00:00:10 -742438.485465] Initial branch length optimization
[00:00:10 -615923.859394] Model parameter optimization (eps = 10.000000)
[00:00:10 -580349.423099] AUTODETECT spr round 1 (radius: 5)
[00:00:10 -530859.050598] AUTODETECT spr round 2 (radius: 10)
[00:00:10 -530859.048253] SPR radius for FAST iterations: 5 (autodetect)
[00:00:10 -530859.048253] Model parameter optimization (eps = 3.000000)
[00:00:10 -530296.471336] FAST spr round 1 (radius: 5)
[00:00:10 -528941.672567] FAST spr round 2 (radius: 5)
[00:00:11 -528941.672567] Model parameter optimization (eps = 1.000000)
[00:00:11 -528899.804220] SLOW spr round 1 (radius: 5)
[00:00:11 -528899.804105] SLOW spr round 2 (radius: 10)
[00:00:11 -528899.804105] Model parameter optimization (eps = 0.100000)

[00:00:11] ML tree search #10, logLikelihood: -528899.802218

[00:00:11 -672232.973901] Initial branch length optimization
[00:00:11 -541092.239552] Model parameter optimization (eps = 10.000000)
[00:00:11 -528909.920347] AUTODETECT spr round 1 (radius: 5)
[00:00:11 -528909.920237] SPR radius for FAST iterations: 5 (autodetect)
[00:00:11 -528909.920237] Model parameter optimization (eps = 3.000000)
[00:00:11 -528909.919843] FAST spr round 1 (radius: 5)
[00:00:11 -528899.810110] FAST spr round 2 (radius: 5)
[00:00:12 -528899.810110] Model parameter optimization (eps = 1.000000)
[00:00:12 -528899.802262] SLOW spr round 1 (radius: 5)
[00:00:12 -528899.802260] SLOW spr round 2 (radius: 10)
[00:00:12 -528899.802260] Model parameter optimization (eps = 0.100000)

[00:00:12] ML tree search #11, logLikelihood: -528899.802014

[00:00:12 -672232.973901] Initial branch length optimization
[00:00:12 -541092.312586] Model parameter optimization (eps = 10.000000)
[00:00:12 -528909.920428] AUTODETECT spr round 1 (radius: 5)
[00:00:12 -528909.920277] SPR radius for FAST iterations: 5 (autodetect)
[00:00:12 -528909.920277] Model parameter optimization (eps = 3.000000)
[00:00:12 -528909.919849] FAST spr round 1 (radius: 5)
[00:00:13 -528899.810054] FAST spr round 2 (radius: 5)
[00:00:13 -528899.810054] Model parameter optimization (eps = 1.000000)
[00:00:13 -528899.802328] SLOW spr round 1 (radius: 5)
[00:00:13 -528899.802327] SLOW spr round 2 (radius: 10)
[00:00:13 -528899.802327] Model parameter optimization (eps = 0.100000)

[00:00:13] ML tree search #12, logLikelihood: -528899.802071

[00:00:13 -672232.973901] Initial branch length optimization
[00:00:14 -541092.291647] Model parameter optimization (eps = 10.000000)
[00:00:14 -528909.920423] AUTODETECT spr round 1 (radius: 5)
[00:00:14 -528909.920242] SPR radius for FAST iterations: 5 (autodetect)
[00:00:14 -528909.920242] Model parameter optimization (eps = 3.000000)
[00:00:14 -528909.919862] FAST spr round 1 (radius: 5)
[00:00:14 -528899.810772] FAST spr round 2 (radius: 5)
[00:00:14 -528899.810772] Model parameter optimization (eps = 1.000000)
[00:00:14 -528899.802270] SLOW spr round 1 (radius: 5)
[00:00:14 -528899.802269] SLOW spr round 2 (radius: 10)
[00:00:14 -528899.802269] Model parameter optimization (eps = 0.100000)

[00:00:14] ML tree search #13, logLikelihood: -528899.802017

[00:00:14 -672232.973901] Initial branch length optimization
[00:00:14 -541092.248809] Model parameter optimization (eps = 10.000000)
[00:00:15 -528909.920343] AUTODETECT spr round 1 (radius: 5)
[00:00:15 -528909.920238] SPR radius for FAST iterations: 5 (autodetect)
[00:00:15 -528909.920238] Model parameter optimization (eps = 3.000000)
[00:00:15 -528909.919838] FAST spr round 1 (radius: 5)
[00:00:15 -528899.810091] FAST spr round 2 (radius: 5)
[00:00:15 -528899.810091] Model parameter optimization (eps = 1.000000)
[00:00:15 -528899.802261] SLOW spr round 1 (radius: 5)
[00:00:15 -528899.802259] SLOW spr round 2 (radius: 10)
[00:00:16 -528899.802259] Model parameter optimization (eps = 0.100000)

[00:00:16] ML tree search #14, logLikelihood: -528899.802014

[00:00:16 -672232.973901] Initial branch length optimization
[00:00:16 -541092.254378] Model parameter optimization (eps = 10.000000)
[00:00:16 -528909.920378] AUTODETECT spr round 1 (radius: 5)
[00:00:16 -528909.920281] SPR radius for FAST iterations: 5 (autodetect)
[00:00:16 -528909.920281] Model parameter optimization (eps = 3.000000)
[00:00:16 -528909.919848] FAST spr round 1 (radius: 5)
[00:00:16 -528899.810043] FAST spr round 2 (radius: 5)
[00:00:16 -528899.810043] Model parameter optimization (eps = 1.000000)
[00:00:16 -528899.802330] SLOW spr round 1 (radius: 5)
[00:00:16 -528899.802328] SLOW spr round 2 (radius: 10)
[00:00:17 -528899.802328] Model parameter optimization (eps = 0.100000)

[00:00:17] ML tree search #15, logLikelihood: -528899.802072

[00:00:17 -672232.973901] Initial branch length optimization
[00:00:17 -541092.239335] Model parameter optimization (eps = 10.000000)
[00:00:17 -528909.920458] AUTODETECT spr round 1 (radius: 5)
[00:00:17 -528909.920250] SPR radius for FAST iterations: 5 (autodetect)
[00:00:17 -528909.920250] Model parameter optimization (eps = 3.000000)
[00:00:17 -528909.919854] FAST spr round 1 (radius: 5)
[00:00:17 -528899.810096] FAST spr round 2 (radius: 5)
[00:00:17 -528899.810096] Model parameter optimization (eps = 1.000000)
[00:00:17 -528899.802297] SLOW spr round 1 (radius: 5)
[00:00:17 -528899.802295] SLOW spr round 2 (radius: 10)
[00:00:18 -528899.802295] Model parameter optimization (eps = 0.100000)

[00:00:18] ML tree search #16, logLikelihood: -528899.802037

[00:00:18 -672232.973901] Initial branch length optimization
[00:00:18 -541092.259346] Model parameter optimization (eps = 10.000000)
[00:00:18 -528909.920337] AUTODETECT spr round 1 (radius: 5)
[00:00:18 -528909.920242] SPR radius for FAST iterations: 5 (autodetect)
[00:00:18 -528909.920242] Model parameter optimization (eps = 3.000000)
[00:00:18 -528909.919844] FAST spr round 1 (radius: 5)
[00:00:18 -528899.810040] FAST spr round 2 (radius: 5)
[00:00:18 -528899.810040] Model parameter optimization (eps = 1.000000)
[00:00:18 -528899.802262] SLOW spr round 1 (radius: 5)
[00:00:18 -528899.802262] SLOW spr round 2 (radius: 10)
[00:00:18 -528899.802262] Model parameter optimization (eps = 0.100000)

[00:00:18] ML tree search #17, logLikelihood: -528899.802016

[00:00:19 -672232.973901] Initial branch length optimization
[00:00:19 -541092.267793] Model parameter optimization (eps = 10.000000)
[00:00:19 -528909.920373] AUTODETECT spr round 1 (radius: 5)
[00:00:19 -528909.920267] SPR radius for FAST iterations: 5 (autodetect)
[00:00:19 -528909.920267] Model parameter optimization (eps = 3.000000)
[00:00:19 -528909.919880] FAST spr round 1 (radius: 5)
[00:00:19 -528899.809884] FAST spr round 2 (radius: 5)
[00:00:19 -528899.809884] Model parameter optimization (eps = 1.000000)
[00:00:19 -528899.802283] SLOW spr round 1 (radius: 5)
[00:00:19 -528899.802281] SLOW spr round 2 (radius: 10)
[00:00:19 -528899.802281] Model parameter optimization (eps = 0.100000)

[00:00:19] ML tree search #18, logLikelihood: -528899.802022

[00:00:19 -672232.973901] Initial branch length optimization
[00:00:19 -541092.274183] Model parameter optimization (eps = 10.000000)
[00:00:20 -528909.920377] AUTODETECT spr round 1 (radius: 5)
[00:00:20 -528909.920288] SPR radius for FAST iterations: 5 (autodetect)
[00:00:20 -528909.920288] Model parameter optimization (eps = 3.000000)
[00:00:20 -528909.919854] FAST spr round 1 (radius: 5)
[00:00:20 -528899.810011] FAST spr round 2 (radius: 5)
[00:00:20 -528899.810011] Model parameter optimization (eps = 1.000000)
[00:00:20 -528899.802330] SLOW spr round 1 (radius: 5)
[00:00:20 -528899.802329] SLOW spr round 2 (radius: 10)
[00:00:20 -528899.802329] Model parameter optimization (eps = 0.100000)

[00:00:20] ML tree search #19, logLikelihood: -528899.802073

[00:00:20 -672232.973901] Initial branch length optimization
[00:00:20 -541092.285524] Model parameter optimization (eps = 10.000000)
[00:00:20 -528909.920341] AUTODETECT spr round 1 (radius: 5)
[00:00:21 -528909.920274] SPR radius for FAST iterations: 5 (autodetect)
[00:00:21 -528909.920274] Model parameter optimization (eps = 3.000000)
[00:00:21 -528909.919843] FAST spr round 1 (radius: 5)
[00:00:21 -528899.810088] FAST spr round 2 (radius: 5)
[00:00:21 -528899.810088] Model parameter optimization (eps = 1.000000)
[00:00:21 -528899.802323] SLOW spr round 1 (radius: 5)
[00:00:21 -528899.802323] SLOW spr round 2 (radius: 10)
[00:00:21 -528899.802323] Model parameter optimization (eps = 0.100000)

[00:00:21] ML tree search #20, logLikelihood: -528899.802068


Optimized model parameters:

   Partition 0: noname
   Rate heterogeneity: GAMMA (4 cats, mean),  alpha: 0.307234 (ML),  weights&rates: (0.250000,0.005900) (0.250000,0.110133) (0.250000,0.607754) (0.250000,3.276213)
   Base frequencies (ML): 0.315592 0.185658 0.182815 0.315935
   Substitution rates (ML): 0.999800 1.745175 0.713275 0.668865 1.760600 1.000000


Final LogLikelihood: -528899.801484

AIC score: 1057859.602968 / AICc score: 1057859.609921 / BIC score: 1058174.513138
Free parameters (model + branch lengths): 30

Best ML tree saved to: /mnt/c/Users/欧阳葭/test_run.raxml.bestTree
All ML trees saved to: /mnt/c/Users/欧阳葭/test_run.raxml.mlTrees
Optimized model saved to: /mnt/c/Users/欧阳葭/test_run.raxml.bestModel

Execution log saved to: /mnt/c/Users/欧阳葭/test_run.raxml.log

Analysis started: 13-Mar-2025 13:16:34 / finished: 13-Mar-2025 13:16:56

Elapsed time: 21.829 seconds

(raxml-ng-env) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ cd /home/suki/phylo-class
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ ls
D_Dataver1.fasta         fixed_aligned_sequences.fasta
aligned_sequences.fasta  hw-aligning-your-own-data
clean_fasta.py           installation-exercise
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ cat /home/suki/phylo-class
/test_run.raxml.bestTree
(MZ379792.1:0.001131,MZ160991.1:0.001327,(MZ160992.1:0.045484,(((MZ160993.1:0.001916,MZ160994.1:0.003971):0.003316,(MZ160995.1:0.034423,(MZ160997.1:0.013106,MZ160996.1:0.005338):0.030318):0.035859):0.007575,(MZ397801.1:0.002712,((MT934442.1:0.000319,MZ397800.1:0.002830):0.000079,MZ160998.1:0.000639):0.001929):0.013448):0.009202):0.003035):0.0;
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ sudo apt install figtree
[sudo] password for suki:
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following package was automatically installed and is no longer required:
  libllvm17t64
Use 'sudo apt autoremove' to remove it.
The following additional packages will be installed:
  alsa-topology-conf alsa-ucm-conf ca-certificates-java default-jdk
  default-jdk-headless default-jre default-jre-headless fonts-dejavu-extra
  java-common java-wrappers libactivation-java libapache-pom-java
  libasound2-data libasound2t64 libatk-wrapper-java libatk-wrapper-java-jni
  libbatik-java libcommons-io-java libcommons-logging-java
  libcommons-parent-java libgif7 libice-dev libice6 libitext5-java
  libjam-java libjaxp1.3-java libjebl2-java libnspr4 libnss3 libpcsclite1
  libpthread-stubs0-dev libsm-dev libsm6 libx11-dev libxau-dev libxaw7
  libxcb-shape0 libxcb1-dev libxdmcp-dev libxft2 libxkbfile1
  libxml-commons-external-java libxmlgraphics-commons-java libxmu6 libxpm4
  libxt-dev libxt6t64 libxv1 libxxf86dga1 openjdk-21-jdk
  openjdk-21-jdk-headless openjdk-21-jre openjdk-21-jre-headless x11-utils
  x11proto-dev xorg-sgml-doctools xtrans-dev
Suggested packages:
  alsa-utils libasound2-plugins librhino-java libcommons-io-java-doc
  libavalon-framework-java libexcalibur-logkit-java liblog4j1.2-java
  libice-doc libbcpkix-java libbcprov-java libxml-security-java pcscd
  libsm-doc libx11-doc libxcb-doc libxmlgraphics-commons-java-doc libxt-doc
  openjdk-21-demo openjdk-21-source visualvm libnss-mdns
  fonts-ipafont-gothic fonts-ipafont-mincho fonts-wqy-microhei
  | fonts-wqy-zenhei fonts-indic mesa-utils
Recommended packages:
  luit
The following NEW packages will be installed:
  alsa-topology-conf alsa-ucm-conf ca-certificates-java default-jdk
  default-jdk-headless default-jre default-jre-headless figtree
  fonts-dejavu-extra java-common java-wrappers libactivation-java
  libapache-pom-java libasound2-data libasound2t64 libatk-wrapper-java
  libatk-wrapper-java-jni libbatik-java libcommons-io-java
  libcommons-logging-java libcommons-parent-java libgif7 libice-dev libice6
  libitext5-java libjam-java libjaxp1.3-java libjebl2-java libnspr4 libnss3
  libpcsclite1 libpthread-stubs0-dev libsm-dev libsm6 libx11-dev libxau-dev
  libxaw7 libxcb-shape0 libxcb1-dev libxdmcp-dev libxft2 libxkbfile1
  libxml-commons-external-java libxmlgraphics-commons-java libxmu6 libxpm4
  libxt-dev libxt6t64 libxv1 libxxf86dga1 openjdk-21-jdk
  openjdk-21-jdk-headless openjdk-21-jre openjdk-21-jre-headless x11-utils
  x11proto-dev xorg-sgml-doctools xtrans-dev
0 upgraded, 58 newly installed, 0 to remove and 13 not upgraded.
Need to get 148 MB of archives.
After this operation, 343 MB of additional disk space will be used.
Do you want to continue? [Y/n] y
Get:1 http://archive.ubuntu.com/ubuntu noble/main amd64 alsa-topology-conf all 1.2.5.1-2 [15.5 kB]
Get:2 http://archive.ubuntu.com/ubuntu noble/main amd64 libasound2-data all 1.2.11-1build2 [21.0 kB]
Get:3 http://archive.ubuntu.com/ubuntu noble/main amd64 libasound2t64 amd64 1.2.11-1build2 [399 kB]
Get:4 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 alsa-ucm-conf all 1.2.10-1ubuntu5.4 [64.8 kB]
Get:5 http://archive.ubuntu.com/ubuntu noble/main amd64 ca-certificates-java all 20240118 [11.6 kB]
Get:6 http://archive.ubuntu.com/ubuntu noble/main amd64 java-common all 0.75+exp1 [6798 B]
Get:7 http://archive.ubuntu.com/ubuntu noble/main amd64 libnspr4 amd64 2:4.35-1.1build1 [117 kB]
Get:8 http://archive.ubuntu.com/ubuntu noble/main amd64 libnss3 amd64 2:3.98-1build1 [1445 kB]
Get:9 http://archive.ubuntu.com/ubuntu noble/main amd64 libpcsclite1 amd64 2.0.3-1build1 [21.4 kB]
Get:10 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 openjdk-21-jre-headless amd64 21.0.6+7-1~24.04.1 [46.4 MB]
Get:11 http://archive.ubuntu.com/ubuntu noble/main amd64 default-jre-headless amd64 2:1.21-75+exp1 [3094 B]
Get:12 http://archive.ubuntu.com/ubuntu noble/main amd64 libgif7 amd64 5.2.2-1ubuntu1 [35.2 kB]
Get:13 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 openjdk-21-jre amd64 21.0.6+7-1~24.04.1 [227 kB]
Get:14 http://archive.ubuntu.com/ubuntu noble/main amd64 default-jre amd64 2:1.21-75+exp1 [922 B]
Get:15 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 openjdk-21-jdk-headless amd64 21.0.6+7-1~24.04.1 [82.6 MB]
Get:16 http://archive.ubuntu.com/ubuntu noble/main amd64 default-jdk-headless amd64 2:1.21-75+exp1 [960 B]
Get:17 http://archive.ubuntu.com/ubuntu noble-updates/main amd64 openjdk-21-jdk amd64 21.0.6+7-1~24.04.1 [1648 kB]
Get:18 http://archive.ubuntu.com/ubuntu noble/main amd64 default-jdk amd64 2:1.21-75+exp1 [926 B]
Get:19 http://archive.ubuntu.com/ubuntu noble/universe amd64 libactivation-java all 1.2.0-2 [84.7 kB]
Get:20 http://archive.ubuntu.com/ubuntu noble/universe amd64 java-wrappers all 0.4 [8662 B]
Get:21 http://archive.ubuntu.com/ubuntu noble/universe amd64 libjaxp1.3-java all 1.3.05-6 [227 kB]
Get:22 http://archive.ubuntu.com/ubuntu noble/universe amd64 libxml-commons-external-java all 1.4.01-6 [240 kB]
Get:23 http://archive.ubuntu.com/ubuntu noble/universe amd64 libapache-pom-java all 29-2 [5284 B]
Get:24 http://archive.ubuntu.com/ubuntu noble/universe amd64 libcommons-parent-java all 56-1 [10.7 kB]
Get:25 http://archive.ubuntu.com/ubuntu noble/universe amd64 libcommons-io-java all 2.11.0-2 [297 kB]
Get:26 http://archive.ubuntu.com/ubuntu noble/universe amd64 libcommons-logging-java all 1.3.0-1ubuntu1 [63.8 kB]
Get:27 http://archive.ubuntu.com/ubuntu noble/universe amd64 libxmlgraphics-commons-java all 2.8-2 [619 kB]
Get:28 http://archive.ubuntu.com/ubuntu noble/universe amd64 libbatik-java all 1.17+dfsg-1 [3877 kB]
Get:29 http://archive.ubuntu.com/ubuntu noble/universe amd64 libitext5-java all 5.5.13.3-4 [2691 kB]
Get:30 http://archive.ubuntu.com/ubuntu noble/universe amd64 libjam-java all 0.1.git20180106.740247a+dfsg-1 [164 kB]
Get:31 http://archive.ubuntu.com/ubuntu noble/universe amd64 libjebl2-java all 0.1+git20230701.b3c0f25-1 [527 kB]
Get:32 http://archive.ubuntu.com/ubuntu noble/universe amd64 figtree all 1.4.4-6 [897 kB]
Get:33 http://archive.ubuntu.com/ubuntu noble/main amd64 fonts-dejavu-extra all 2.37-8 [1947 kB]
Get:34 http://archive.ubuntu.com/ubuntu noble/main amd64 libice6 amd64 2:1.0.10-1build3 [41.4 kB]
Get:35 http://archive.ubuntu.com/ubuntu noble/main amd64 libsm6 amd64 2:1.2.3-1build3 [15.7 kB]
Get:36 http://archive.ubuntu.com/ubuntu noble/main amd64 libxt6t64 amd64 1:1.2.1-1.2build1 [171 kB]
Get:37 http://archive.ubuntu.com/ubuntu noble/main amd64 libxmu6 amd64 2:1.1.3-3build2 [47.6 kB]
Get:38 http://archive.ubuntu.com/ubuntu noble/main amd64 libxpm4 amd64 1:3.5.17-1build2 [36.5 kB]
Get:39 http://archive.ubuntu.com/ubuntu noble/main amd64 libxaw7 amd64 2:1.0.14-1build2 [187 kB]
Get:40 http://archive.ubuntu.com/ubuntu noble/main amd64 libxcb-shape0 amd64 1.15-1ubuntu2 [6100 B]
Get:41 http://archive.ubuntu.com/ubuntu noble/main amd64 libxft2 amd64 2.3.6-1build1 [45.3 kB]
Get:42 http://archive.ubuntu.com/ubuntu noble/main amd64 libxkbfile1 amd64 1:1.1.0-1build4 [70.0 kB]
Get:43 http://archive.ubuntu.com/ubuntu noble/main amd64 libxv1 amd64 2:1.0.11-1.1build1 [10.7 kB]
Get:44 http://archive.ubuntu.com/ubuntu noble/main amd64 libxxf86dga1 amd64 2:1.1.5-1build1 [11.6 kB]
Get:45 http://archive.ubuntu.com/ubuntu noble/main amd64 x11-utils amd64 7.7+6build2 [189 kB]
Get:46 http://archive.ubuntu.com/ubuntu noble/main amd64 libatk-wrapper-java all 0.40.0-3build2 [54.3 kB]
Get:47 http://archive.ubuntu.com/ubuntu noble/main amd64 libatk-wrapper-java-jni amd64 0.40.0-3build2 [46.4 kB]
Get:48 http://archive.ubuntu.com/ubuntu noble/main amd64 xorg-sgml-doctools all 1:1.11-1.1 [10.9 kB]
Get:49 http://archive.ubuntu.com/ubuntu noble/main amd64 x11proto-dev all 2023.2-1 [602 kB]
Get:50 http://archive.ubuntu.com/ubuntu noble/main amd64 libice-dev amd64 2:1.0.10-1build3 [51.0 kB]
Get:51 http://archive.ubuntu.com/ubuntu noble/main amd64 libpthread-stubs0-dev amd64 0.4-1build3 [4746 B]
Get:52 http://archive.ubuntu.com/ubuntu noble/main amd64 libsm-dev amd64 2:1.2.3-1build3 [17.8 kB]
Get:53 http://archive.ubuntu.com/ubuntu noble/main amd64 libxau-dev amd64 1:1.0.9-1build6 [9570 B]
Get:54 http://archive.ubuntu.com/ubuntu noble/main amd64 libxdmcp-dev amd64 1:1.1.3-0ubuntu6 [26.5 kB]
Get:55 http://archive.ubuntu.com/ubuntu noble/main amd64 xtrans-dev all 1.4.0-1 [68.9 kB]
Get:56 http://archive.ubuntu.com/ubuntu noble/main amd64 libxcb1-dev amd64 1.15-1ubuntu2 [85.8 kB]
Get:57 http://archive.ubuntu.com/ubuntu noble/main amd64 libx11-dev amd64 2:1.8.7-1build1 [732 kB]
Get:58 http://archive.ubuntu.com/ubuntu noble/main amd64 libxt-dev amd64 1:1.2.1-1.2build1 [394 kB]
Fetched 148 MB in 22s (6588 kB/s)
Extracting templates from packages: 100%
Selecting previously unselected package alsa-topology-conf.
(Reading database ... 45068 files and directories currently installed.)
Preparing to unpack .../00-alsa-topology-conf_1.2.5.1-2_all.deb ...
Unpacking alsa-topology-conf (1.2.5.1-2) ...
Selecting previously unselected package libasound2-data.
Preparing to unpack .../01-libasound2-data_1.2.11-1build2_all.deb ...
Unpacking libasound2-data (1.2.11-1build2) ...
Selecting previously unselected package libasound2t64:amd64.
Preparing to unpack .../02-libasound2t64_1.2.11-1build2_amd64.deb ...
Unpacking libasound2t64:amd64 (1.2.11-1build2) ...
Selecting previously unselected package alsa-ucm-conf.
Preparing to unpack .../03-alsa-ucm-conf_1.2.10-1ubuntu5.4_all.deb ...
Unpacking alsa-ucm-conf (1.2.10-1ubuntu5.4) ...
Selecting previously unselected package ca-certificates-java.
Preparing to unpack .../04-ca-certificates-java_20240118_all.deb ...
Unpacking ca-certificates-java (20240118) ...
Selecting previously unselected package java-common.
Preparing to unpack .../05-java-common_0.75+exp1_all.deb ...
Unpacking java-common (0.75+exp1) ...
Selecting previously unselected package libnspr4:amd64.
Preparing to unpack .../06-libnspr4_2%3a4.35-1.1build1_amd64.deb ...
Unpacking libnspr4:amd64 (2:4.35-1.1build1) ...
Selecting previously unselected package libnss3:amd64.
Preparing to unpack .../07-libnss3_2%3a3.98-1build1_amd64.deb ...
Unpacking libnss3:amd64 (2:3.98-1build1) ...
Selecting previously unselected package libpcsclite1:amd64.
Preparing to unpack .../08-libpcsclite1_2.0.3-1build1_amd64.deb ...
Unpacking libpcsclite1:amd64 (2.0.3-1build1) ...
Selecting previously unselected package openjdk-21-jre-headless:amd64.
Preparing to unpack .../09-openjdk-21-jre-headless_21.0.6+7-1~24.04.1_amd64.deb ...
Unpacking openjdk-21-jre-headless:amd64 (21.0.6+7-1~24.04.1) ...
Selecting previously unselected package default-jre-headless.
Preparing to unpack .../10-default-jre-headless_2%3a1.21-75+exp1_amd64.deb ...
Unpacking default-jre-headless (2:1.21-75+exp1) ...
Selecting previously unselected package libgif7:amd64.
Preparing to unpack .../11-libgif7_5.2.2-1ubuntu1_amd64.deb ...
Unpacking libgif7:amd64 (5.2.2-1ubuntu1) ...
Selecting previously unselected package openjdk-21-jre:amd64.
Preparing to unpack .../12-openjdk-21-jre_21.0.6+7-1~24.04.1_amd64.deb ...
Unpacking openjdk-21-jre:amd64 (21.0.6+7-1~24.04.1) ...
Selecting previously unselected package default-jre.
Preparing to unpack .../13-default-jre_2%3a1.21-75+exp1_amd64.deb ...
Unpacking default-jre (2:1.21-75+exp1) ...
Selecting previously unselected package openjdk-21-jdk-headless:amd64.
Preparing to unpack .../14-openjdk-21-jdk-headless_21.0.6+7-1~24.04.1_amd64.deb ...
Unpacking openjdk-21-jdk-headless:amd64 (21.0.6+7-1~24.04.1) ...
Selecting previously unselected package default-jdk-headless.
Preparing to unpack .../15-default-jdk-headless_2%3a1.21-75+exp1_amd64.deb ...
Unpacking default-jdk-headless (2:1.21-75+exp1) ...
Selecting previously unselected package openjdk-21-jdk:amd64.
Preparing to unpack .../16-openjdk-21-jdk_21.0.6+7-1~24.04.1_amd64.deb ...
Unpacking openjdk-21-jdk:amd64 (21.0.6+7-1~24.04.1) ...
Selecting previously unselected package default-jdk.
Preparing to unpack .../17-default-jdk_2%3a1.21-75+exp1_amd64.deb ...
Unpacking default-jdk (2:1.21-75+exp1) ...
Selecting previously unselected package libactivation-java.
Preparing to unpack .../18-libactivation-java_1.2.0-2_all.deb ...
Unpacking libactivation-java (1.2.0-2) ...
Selecting previously unselected package java-wrappers.
Preparing to unpack .../19-java-wrappers_0.4_all.deb ...
Unpacking java-wrappers (0.4) ...
Selecting previously unselected package libjaxp1.3-java.
Preparing to unpack .../20-libjaxp1.3-java_1.3.05-6_all.deb ...
Unpacking libjaxp1.3-java (1.3.05-6) ...
Selecting previously unselected package libxml-commons-external-java.
Preparing to unpack .../21-libxml-commons-external-java_1.4.01-6_all.deb ...
Unpacking libxml-commons-external-java (1.4.01-6) ...
Selecting previously unselected package libapache-pom-java.
Preparing to unpack .../22-libapache-pom-java_29-2_all.deb ...
Unpacking libapache-pom-java (29-2) ...
Selecting previously unselected package libcommons-parent-java.
Preparing to unpack .../23-libcommons-parent-java_56-1_all.deb ...
Unpacking libcommons-parent-java (56-1) ...
Selecting previously unselected package libcommons-io-java.
Preparing to unpack .../24-libcommons-io-java_2.11.0-2_all.deb ...
Unpacking libcommons-io-java (2.11.0-2) ...
Selecting previously unselected package libcommons-logging-java.
Preparing to unpack .../25-libcommons-logging-java_1.3.0-1ubuntu1_all.deb ...
Unpacking libcommons-logging-java (1.3.0-1ubuntu1) ...
Selecting previously unselected package libxmlgraphics-commons-java.
Preparing to unpack .../26-libxmlgraphics-commons-java_2.8-2_all.deb ...
Unpacking libxmlgraphics-commons-java (2.8-2) ...
Selecting previously unselected package libbatik-java.
Preparing to unpack .../27-libbatik-java_1.17+dfsg-1_all.deb ...
Unpacking libbatik-java (1.17+dfsg-1) ...
Selecting previously unselected package libitext5-java.
Preparing to unpack .../28-libitext5-java_5.5.13.3-4_all.deb ...
Unpacking libitext5-java (5.5.13.3-4) ...
Selecting previously unselected package libjam-java.
Preparing to unpack .../29-libjam-java_0.1.git20180106.740247a+dfsg-1_all.deb ...
Unpacking libjam-java (0.1.git20180106.740247a+dfsg-1) ...
Selecting previously unselected package libjebl2-java.
Preparing to unpack .../30-libjebl2-java_0.1+git20230701.b3c0f25-1_all.deb ...
Unpacking libjebl2-java (0.1+git20230701.b3c0f25-1) ...
Selecting previously unselected package figtree.
Preparing to unpack .../31-figtree_1.4.4-6_all.deb ...
Unpacking figtree (1.4.4-6) ...
Selecting previously unselected package fonts-dejavu-extra.
Preparing to unpack .../32-fonts-dejavu-extra_2.37-8_all.deb ...
Unpacking fonts-dejavu-extra (2.37-8) ...
Selecting previously unselected package libice6:amd64.
Preparing to unpack .../33-libice6_2%3a1.0.10-1build3_amd64.deb ...
Unpacking libice6:amd64 (2:1.0.10-1build3) ...
Selecting previously unselected package libsm6:amd64.
Preparing to unpack .../34-libsm6_2%3a1.2.3-1build3_amd64.deb ...
Unpacking libsm6:amd64 (2:1.2.3-1build3) ...
Selecting previously unselected package libxt6t64:amd64.
Preparing to unpack .../35-libxt6t64_1%3a1.2.1-1.2build1_amd64.deb ...
Unpacking libxt6t64:amd64 (1:1.2.1-1.2build1) ...
Selecting previously unselected package libxmu6:amd64.
Preparing to unpack .../36-libxmu6_2%3a1.1.3-3build2_amd64.deb ...
Unpacking libxmu6:amd64 (2:1.1.3-3build2) ...
Selecting previously unselected package libxpm4:amd64.
Preparing to unpack .../37-libxpm4_1%3a3.5.17-1build2_amd64.deb ...
Unpacking libxpm4:amd64 (1:3.5.17-1build2) ...
Selecting previously unselected package libxaw7:amd64.
Preparing to unpack .../38-libxaw7_2%3a1.0.14-1build2_amd64.deb ...
Unpacking libxaw7:amd64 (2:1.0.14-1build2) ...
Selecting previously unselected package libxcb-shape0:amd64.
Preparing to unpack .../39-libxcb-shape0_1.15-1ubuntu2_amd64.deb ...
Unpacking libxcb-shape0:amd64 (1.15-1ubuntu2) ...
Selecting previously unselected package libxft2:amd64.
Preparing to unpack .../40-libxft2_2.3.6-1build1_amd64.deb ...
Unpacking libxft2:amd64 (2.3.6-1build1) ...
Selecting previously unselected package libxkbfile1:amd64.
Preparing to unpack .../41-libxkbfile1_1%3a1.1.0-1build4_amd64.deb ...
Unpacking libxkbfile1:amd64 (1:1.1.0-1build4) ...
Selecting previously unselected package libxv1:amd64.
Preparing to unpack .../42-libxv1_2%3a1.0.11-1.1build1_amd64.deb ...
Unpacking libxv1:amd64 (2:1.0.11-1.1build1) ...
Selecting previously unselected package libxxf86dga1:amd64.
Preparing to unpack .../43-libxxf86dga1_2%3a1.1.5-1build1_amd64.deb ...
Unpacking libxxf86dga1:amd64 (2:1.1.5-1build1) ...
Selecting previously unselected package x11-utils.
Preparing to unpack .../44-x11-utils_7.7+6build2_amd64.deb ...
Unpacking x11-utils (7.7+6build2) ...
Selecting previously unselected package libatk-wrapper-java.
Preparing to unpack .../45-libatk-wrapper-java_0.40.0-3build2_all.deb ...
Unpacking libatk-wrapper-java (0.40.0-3build2) ...
Selecting previously unselected package libatk-wrapper-java-jni:amd64.
Preparing to unpack .../46-libatk-wrapper-java-jni_0.40.0-3build2_amd64.deb ...
Unpacking libatk-wrapper-java-jni:amd64 (0.40.0-3build2) ...
Selecting previously unselected package xorg-sgml-doctools.
Preparing to unpack .../47-xorg-sgml-doctools_1%3a1.11-1.1_all.deb ...
Unpacking xorg-sgml-doctools (1:1.11-1.1) ...
Selecting previously unselected package x11proto-dev.
Preparing to unpack .../48-x11proto-dev_2023.2-1_all.deb ...
Unpacking x11proto-dev (2023.2-1) ...
Selecting previously unselected package libice-dev:amd64.
Preparing to unpack .../49-libice-dev_2%3a1.0.10-1build3_amd64.deb ...
Unpacking libice-dev:amd64 (2:1.0.10-1build3) ...
Selecting previously unselected package libpthread-stubs0-dev:amd64.
Preparing to unpack .../50-libpthread-stubs0-dev_0.4-1build3_amd64.deb ...
Unpacking libpthread-stubs0-dev:amd64 (0.4-1build3) ...
Selecting previously unselected package libsm-dev:amd64.
Preparing to unpack .../51-libsm-dev_2%3a1.2.3-1build3_amd64.deb ...
Unpacking libsm-dev:amd64 (2:1.2.3-1build3) ...
Selecting previously unselected package libxau-dev:amd64.
Preparing to unpack .../52-libxau-dev_1%3a1.0.9-1build6_amd64.deb ...
Unpacking libxau-dev:amd64 (1:1.0.9-1build6) ...
Selecting previously unselected package libxdmcp-dev:amd64.
Preparing to unpack .../53-libxdmcp-dev_1%3a1.1.3-0ubuntu6_amd64.deb ...
Unpacking libxdmcp-dev:amd64 (1:1.1.3-0ubuntu6) ...
Selecting previously unselected package xtrans-dev.
Preparing to unpack .../54-xtrans-dev_1.4.0-1_all.deb ...
Unpacking xtrans-dev (1.4.0-1) ...
Selecting previously unselected package libxcb1-dev:amd64.
Preparing to unpack .../55-libxcb1-dev_1.15-1ubuntu2_amd64.deb ...
Unpacking libxcb1-dev:amd64 (1.15-1ubuntu2) ...
Selecting previously unselected package libx11-dev:amd64.
Preparing to unpack .../56-libx11-dev_2%3a1.8.7-1build1_amd64.deb ...
Unpacking libx11-dev:amd64 (2:1.8.7-1build1) ...
Selecting previously unselected package libxt-dev:amd64.
Preparing to unpack .../57-libxt-dev_1%3a1.2.1-1.2build1_amd64.deb ...
Unpacking libxt-dev:amd64 (1:1.2.1-1.2build1) ...
Setting up libjebl2-java (0.1+git20230701.b3c0f25-1) ...
Setting up libice6:amd64 (2:1.0.10-1build3) ...
Setting up libxft2:amd64 (2.3.6-1build1) ...
Setting up java-wrappers (0.4) ...
Setting up libxpm4:amd64 (1:3.5.17-1build2) ...
Setting up java-common (0.75+exp1) ...
Setting up libxcb-shape0:amd64 (1.15-1ubuntu2) ...
Setting up libxxf86dga1:amd64 (2:1.1.5-1build1) ...
Setting up libpthread-stubs0-dev:amd64 (0.4-1build3) ...
Setting up libasound2-data (1.2.11-1build2) ...
Setting up xtrans-dev (1.4.0-1) ...
Setting up libasound2t64:amd64 (1.2.11-1build2) ...
Setting up libnspr4:amd64 (2:4.35-1.1build1) ...
Setting up libapache-pom-java (29-2) ...
Setting up libxv1:amd64 (2:1.0.11-1.1build1) ...
Setting up libitext5-java (5.5.13.3-4) ...
Setting up libpcsclite1:amd64 (2.0.3-1build1) ...
Setting up libactivation-java (1.2.0-2) ...
Setting up libgif7:amd64 (5.2.2-1ubuntu1) ...
Setting up fonts-dejavu-extra (2.37-8) ...
Setting up alsa-topology-conf (1.2.5.1-2) ...
Setting up libxml-commons-external-java (1.4.01-6) ...
Setting up xorg-sgml-doctools (1:1.11-1.1) ...
Setting up libxkbfile1:amd64 (1:1.1.0-1build4) ...
Setting up libjam-java (0.1.git20180106.740247a+dfsg-1) ...
Setting up ca-certificates-java (20240118) ...
No JRE found. Skipping Java certificates setup.
Setting up libjaxp1.3-java (1.3.05-6) ...
Setting up libsm6:amd64 (2:1.2.3-1build3) ...
Setting up alsa-ucm-conf (1.2.10-1ubuntu5.4) ...
Setting up libcommons-parent-java (56-1) ...
Setting up libcommons-logging-java (1.3.0-1ubuntu1) ...
Setting up libnss3:amd64 (2:3.98-1build1) ...
Setting up libxt6t64:amd64 (1:1.2.1-1.2build1) ...
Setting up libxmu6:amd64 (2:1.1.3-3build2) ...
Setting up openjdk-21-jre-headless:amd64 (21.0.6+7-1~24.04.1) ...
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/java to provide /usr/bin/java (java) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jpackage to provide /usr/bin/jpackage (jpackage) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/keytool to
provide /usr/bin/keytool (keytool) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/rmiregistry
 to provide /usr/bin/rmiregistry (rmiregistry) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/lib/jexec to provide /usr/bin/jexec (jexec) in auto mode
Setting up libcommons-io-java (2.11.0-2) ...
Setting up libxmlgraphics-commons-java (2.8-2) ...
Setting up libxaw7:amd64 (2:1.0.14-1build2) ...
Setting up x11-utils (7.7+6build2) ...
Setting up libatk-wrapper-java (0.40.0-3build2) ...
Setting up libbatik-java (1.17+dfsg-1) ...
Setting up libatk-wrapper-java-jni:amd64 (0.40.0-3build2) ...
Processing triggers for sgml-base (1.31) ...
Processing triggers for mailcap (3.70+nmu1ubuntu1) ...
Setting up x11proto-dev (2023.2-1) ...
Processing triggers for fontconfig (2.15.0-1.1ubuntu2) ...
Setting up libxau-dev:amd64 (1:1.0.9-1build6) ...
Processing triggers for hicolor-icon-theme (0.17-2) ...
Setting up libice-dev:amd64 (2:1.0.10-1build3) ...
Setting up libsm-dev:amd64 (2:1.2.3-1build3) ...
Processing triggers for libc-bin (2.39-0ubuntu8.4) ...
Processing triggers for man-db (2.12.0-4build2) ...
Setting up libxdmcp-dev:amd64 (1:1.1.3-0ubuntu6) ...
Setting up libxcb1-dev:amd64 (1.15-1ubuntu2) ...
Setting up libx11-dev:amd64 (2:1.8.7-1build1) ...
Setting up libxt-dev:amd64 (1:1.2.1-1.2build1) ...
Processing triggers for ca-certificates-java (20240118) ...
Adding debian:ACCVRAIZ1.pem
Adding debian:AC_RAIZ_FNMT-RCM.pem
Adding debian:AC_RAIZ_FNMT-RCM_SERVIDORES_SEGUROS.pem
Adding debian:ANF_Secure_Server_Root_CA.pem
Adding debian:Actalis_Authentication_Root_CA.pem
Adding debian:AffirmTrust_Commercial.pem
Adding debian:AffirmTrust_Networking.pem
Adding debian:AffirmTrust_Premium.pem
Adding debian:AffirmTrust_Premium_ECC.pem
Adding debian:Amazon_Root_CA_1.pem
Adding debian:Amazon_Root_CA_2.pem
Adding debian:Amazon_Root_CA_3.pem
Adding debian:Amazon_Root_CA_4.pem
Adding debian:Atos_TrustedRoot_2011.pem
Adding debian:Atos_TrustedRoot_Root_CA_ECC_TLS_2021.pem
Adding debian:Atos_TrustedRoot_Root_CA_RSA_TLS_2021.pem
Adding debian:Autoridad_de_Certificacion_Firmaprofesional_CIF_A62634068.pem
Adding debian:BJCA_Global_Root_CA1.pem
Adding debian:BJCA_Global_Root_CA2.pem
Adding debian:Baltimore_CyberTrust_Root.pem
Adding debian:Buypass_Class_2_Root_CA.pem
Adding debian:Buypass_Class_3_Root_CA.pem
Adding debian:CA_Disig_Root_R2.pem
Adding debian:CFCA_EV_ROOT.pem
Adding debian:COMODO_Certification_Authority.pem
Adding debian:COMODO_ECC_Certification_Authority.pem
Adding debian:COMODO_RSA_Certification_Authority.pem
Adding debian:Certainly_Root_E1.pem
Adding debian:Certainly_Root_R1.pem
Adding debian:Certigna.pem
Adding debian:Certigna_Root_CA.pem
Adding debian:Certum_EC-384_CA.pem
Adding debian:Certum_Trusted_Network_CA.pem
Adding debian:Certum_Trusted_Network_CA_2.pem
Adding debian:Certum_Trusted_Root_CA.pem
Adding debian:CommScope_Public_Trust_ECC_Root-01.pem
Adding debian:CommScope_Public_Trust_ECC_Root-02.pem
Adding debian:CommScope_Public_Trust_RSA_Root-01.pem
Adding debian:CommScope_Public_Trust_RSA_Root-02.pem
Adding debian:Comodo_AAA_Services_root.pem
Adding debian:D-TRUST_BR_Root_CA_1_2020.pem
Adding debian:D-TRUST_EV_Root_CA_1_2020.pem
Adding debian:D-TRUST_Root_Class_3_CA_2_2009.pem
Adding debian:D-TRUST_Root_Class_3_CA_2_EV_2009.pem
Adding debian:DigiCert_Assured_ID_Root_CA.pem
Adding debian:DigiCert_Assured_ID_Root_G2.pem
Adding debian:DigiCert_Assured_ID_Root_G3.pem
Adding debian:DigiCert_Global_Root_CA.pem
Adding debian:DigiCert_Global_Root_G2.pem
Adding debian:DigiCert_Global_Root_G3.pem
Adding debian:DigiCert_High_Assurance_EV_Root_CA.pem
Adding debian:DigiCert_TLS_ECC_P384_Root_G5.pem
Adding debian:DigiCert_TLS_RSA4096_Root_G5.pem
Adding debian:DigiCert_Trusted_Root_G4.pem
Adding debian:Entrust.net_Premium_2048_Secure_Server_CA.pem
Adding debian:Entrust_Root_Certification_Authority.pem
Adding debian:Entrust_Root_Certification_Authority_-_EC1.pem
Adding debian:Entrust_Root_Certification_Authority_-_G2.pem
Adding debian:Entrust_Root_Certification_Authority_-_G4.pem
Adding debian:GDCA_TrustAUTH_R5_ROOT.pem
Adding debian:GLOBALTRUST_2020.pem
Adding debian:GTS_Root_R1.pem
Adding debian:GTS_Root_R2.pem
Adding debian:GTS_Root_R3.pem
Adding debian:GTS_Root_R4.pem
Adding debian:GlobalSign_ECC_Root_CA_-_R4.pem
Adding debian:GlobalSign_ECC_Root_CA_-_R5.pem
Adding debian:GlobalSign_Root_CA.pem
Adding debian:GlobalSign_Root_CA_-_R3.pem
Adding debian:GlobalSign_Root_CA_-_R6.pem
Adding debian:GlobalSign_Root_E46.pem
Adding debian:GlobalSign_Root_R46.pem
Adding debian:Go_Daddy_Class_2_CA.pem
Adding debian:Go_Daddy_Root_Certificate_Authority_-_G2.pem
Adding debian:HARICA_TLS_ECC_Root_CA_2021.pem
Adding debian:HARICA_TLS_RSA_Root_CA_2021.pem
Adding debian:Hellenic_Academic_and_Research_Institutions_ECC_RootCA_2015.pem
Adding debian:Hellenic_Academic_and_Research_Institutions_RootCA_2015.pem
Adding debian:HiPKI_Root_CA_-_G1.pem
Adding debian:Hongkong_Post_Root_CA_3.pem
Adding debian:ISRG_Root_X1.pem
Adding debian:ISRG_Root_X2.pem
Adding debian:IdenTrust_Commercial_Root_CA_1.pem
Adding debian:IdenTrust_Public_Sector_Root_CA_1.pem
Adding debian:Izenpe.com.pem
Adding debian:Microsec_e-Szigno_Root_CA_2009.pem
Adding debian:Microsoft_ECC_Root_Certificate_Authority_2017.pem
Adding debian:Microsoft_RSA_Root_Certificate_Authority_2017.pem
Adding debian:NAVER_Global_Root_Certification_Authority.pem
Adding debian:NetLock_Arany_=Class_Gold=_Főtanúsítvány.pem
Adding debian:OISTE_WISeKey_Global_Root_GB_CA.pem
Adding debian:OISTE_WISeKey_Global_Root_GC_CA.pem
Adding debian:QuoVadis_Root_CA_1_G3.pem
Adding debian:QuoVadis_Root_CA_2.pem
Adding debian:QuoVadis_Root_CA_2_G3.pem
Adding debian:QuoVadis_Root_CA_3.pem
Adding debian:QuoVadis_Root_CA_3_G3.pem
Adding debian:SSL.com_EV_Root_Certification_Authority_ECC.pem
Adding debian:SSL.com_EV_Root_Certification_Authority_RSA_R2.pem
Adding debian:SSL.com_Root_Certification_Authority_ECC.pem
Adding debian:SSL.com_Root_Certification_Authority_RSA.pem
Adding debian:SSL.com_TLS_ECC_Root_CA_2022.pem
Adding debian:SSL.com_TLS_RSA_Root_CA_2022.pem
Adding debian:SZAFIR_ROOT_CA2.pem
Adding debian:Sectigo_Public_Server_Authentication_Root_E46.pem
Adding debian:Sectigo_Public_Server_Authentication_Root_R46.pem
Adding debian:SecureSign_RootCA11.pem
Adding debian:SecureTrust_CA.pem
Adding debian:Secure_Global_CA.pem
Adding debian:Security_Communication_ECC_RootCA1.pem
Adding debian:Security_Communication_RootCA2.pem
Adding debian:Security_Communication_RootCA3.pem
Adding debian:Security_Communication_Root_CA.pem
Adding debian:Starfield_Class_2_CA.pem
Adding debian:Starfield_Root_Certificate_Authority_-_G2.pem
Adding debian:Starfield_Services_Root_Certificate_Authority_-_G2.pem
Adding debian:SwissSign_Gold_CA_-_G2.pem
Adding debian:SwissSign_Silver_CA_-_G2.pem
Adding debian:T-TeleSec_GlobalRoot_Class_2.pem
Adding debian:T-TeleSec_GlobalRoot_Class_3.pem
Adding debian:TUBITAK_Kamu_SM_SSL_Kok_Sertifikasi_-_Surum_1.pem
Adding debian:TWCA_Global_Root_CA.pem
Adding debian:TWCA_Root_Certification_Authority.pem
Adding debian:TeliaSonera_Root_CA_v1.pem
Adding debian:Telia_Root_CA_v2.pem
Adding debian:TrustAsia_Global_Root_CA_G3.pem
Adding debian:TrustAsia_Global_Root_CA_G4.pem
Adding debian:Trustwave_Global_Certification_Authority.pem
Adding debian:Trustwave_Global_ECC_P256_Certification_Authority.pem
Adding debian:Trustwave_Global_ECC_P384_Certification_Authority.pem
Adding debian:TunTrust_Root_CA.pem
Adding debian:UCA_Extended_Validation_Root.pem
Adding debian:UCA_Global_G2_Root.pem
Adding debian:USERTrust_ECC_Certification_Authority.pem
Adding debian:USERTrust_RSA_Certification_Authority.pem
Adding debian:XRamp_Global_CA_Root.pem
Adding debian:certSIGN_ROOT_CA.pem
Adding debian:certSIGN_Root_CA_G2.pem
Adding debian:e-Szigno_Root_CA_2017.pem
Adding debian:ePKI_Root_Certification_Authority.pem
Adding debian:emSign_ECC_Root_CA_-_C3.pem
Adding debian:emSign_ECC_Root_CA_-_G3.pem
Adding debian:emSign_Root_CA_-_C1.pem
Adding debian:emSign_Root_CA_-_G1.pem
Adding debian:vTrus_ECC_Root_CA.pem
Adding debian:vTrus_Root_CA.pem
done.
Setting up default-jre-headless (2:1.21-75+exp1) ...
Setting up openjdk-21-jre:amd64 (21.0.6+7-1~24.04.1) ...
Setting up openjdk-21-jdk-headless:amd64 (21.0.6+7-1~24.04.1) ...
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jar to provide /usr/bin/jar (jar) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jarsigner t
o provide /usr/bin/jarsigner (jarsigner) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/javac to provide /usr/bin/javac (javac) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/javadoc to
provide /usr/bin/javadoc (javadoc) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/javap to pr
ovide /usr/bin/javap (javap) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jcmd to provide /usr/bin/jcmd (jcmd) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jdb to prov
ide /usr/bin/jdb (jdb) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jdeprscan t
o provide /usr/bin/jdeprscan (jdeprscan) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jdeps to provide /usr/bin/jdeps (jdeps) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jfr to prov
ide /usr/bin/jfr (jfr) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jimage to p
rovide /usr/bin/jimage (jimage) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jinfo to pr
ovide /usr/bin/jinfo (jinfo) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jlink to provide /usr/bin/jlink (jlink) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jmap to pro
vide /usr/bin/jmap (jmap) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jmod to pro
vide /usr/bin/jmod (jmod) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jps to prov
ide /usr/bin/jps (jps) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jrunscript to provide /usr/bin/jrunscript (jrunscript) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jshell to p
rovide /usr/bin/jshell (jshell) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jstack to p
rovide /usr/bin/jstack (jstack) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jstat to pr
ovide /usr/bin/jstat (jstat) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jstatd to provide /usr/bin/jstatd (jstatd) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jwebserver
to provide /usr/bin/jwebserver (jwebserver) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/serialver t
o provide /usr/bin/serialver (serialver) in auto mode
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jhsdb to pr
ovide /usr/bin/jhsdb (jhsdb) in auto mode
Setting up default-jre (2:1.21-75+exp1) ...
Setting up openjdk-21-jdk:amd64 (21.0.6+7-1~24.04.1) ...
update-alternatives: using /usr/lib/jvm/java-21-openjdk-amd64/bin/jconsole to provide /usr/bin/jconsole (jconsole) in auto mode
Setting up default-jdk-headless (2:1.21-75+exp1) ...
Setting up default-jdk (2:1.21-75+exp1) ...
Setting up figtree (1.4.4-6) ...
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ figtree /home/suki/phylo-class/final_tree.raxml.support
javax.swing.UIManager$LookAndFeelInfo[Metal javax.swing.plaf.metal.MetalLookAndFeel]
javax.swing.UIManager$LookAndFeelInfo[Nimbus javax.swing.plaf.nimbus.NimbusLookAndFeel]
javax.swing.UIManager$LookAndFeelInfo[CDE/Motif com.sun.java.swing.plaf.motif.MotifLookAndFeel]
javax.swing.UIManager$LookAndFeelInfo[GTK+ com.sun.java.swing.plaf.gtk.GTKLookAndFeel]
Mar 13, 2025 1:23:20 PM java.util.prefs.FileSystemPreferences$1 run
INFO: Created user preferences directory.


conda remove figtree






ll
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ conda remove figtree

PackagesNotFoundError: The following packages are missing from the target environment:
  - figtree


(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ ll
total 8368
drwxr-xr-x  4 suki suki    4096 Mar 13 13:21 ./
drwxr-x--- 10 suki suki    4096 Mar 13 13:23 ../
-rw-r--r--  1 suki suki 1872045 Mar  6 11:28 D_Dataver1.fasta
-rw-r--r--  1 suki suki 3264661 Mar  6 11:45 aligned_sequences.fasta
-rw-r--r--  1 suki suki    1210 Mar  6 12:01 clean_fasta.py
-rw-r--r--  1 suki suki 3264072 Mar  6 12:01 fixed_aligned_sequences.fasta
drwxr-xr-x  2 suki suki    4096 Feb 18 23:41 hw-aligning-your-own-data/
drwxr-xr-x  2 suki suki    4096 Feb 18 22:54 installation-exercise/
-rw-r--r--  1 suki suki     132 Mar 13 13:16 test_run.raxml.bestModel
-rw-r--r--  1 suki suki     346 Mar 13 13:16 test_run.raxml.bestTree
-rw-r--r--  1 suki suki   18641 Mar 13 13:16 test_run.raxml.log
-rw-r--r--  1 suki suki    6920 Mar 13 13:16 test_run.raxml.mlTrees
-rw-r--r--  1 suki suki   91124 Mar 13 13:16 test_run.raxml.rba
-rw-r--r--  1 suki suki    6920 Mar 13 13:16 test_run.raxml.startTree
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ conda info --envs

# conda environments:
#
base                   /home/suki/miniconda3
fasta_clean            /home/suki/miniconda3/envs/fasta_clean
iqtree-env             /home/suki/miniconda3/envs/iqtree-env
raxml-ng-env         * /home/suki/miniconda3/envs/raxml-ng-env

(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ conda list | grep figtree
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ raxml-ng --parse --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta --model GTR+G --prefix parsed_data

RAxML-NG v. 0.9.0 released on 20.05.2019 by The Exelixis Lab.
Developed by: Alexey M. Kozlov and Alexandros Stamatakis.
Contributors: Diego Darriba, Tomas Flouri, Benoit Morel, Sarah Lutteropp, Ben Bettisworth.
Latest version: https://github.com/amkozlov/raxml-ng
Questions/problems/suggestions? Please visit: https://groups.google.com/forum/#!forum/raxml

RAxML-NG was called at 13-Mar-2025 13:48:15 as follows:

raxml-ng --parse --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta --model GTR+G --prefix parsed_data

Analysis options:
  run mode: Alignment parsing and compression
  start tree(s):
  random seed: 1741891695
  tip-inner: OFF
  pattern compression: ON
  per-rate scalers: OFF
  site repeats: ON
  branch lengths: proportional (ML estimate, algorithm: NR-FAST)
  SIMD kernels: AVX2
  parallelization: PTHREADS (11 threads), thread pinning: OFF

[00:00:00] Reading alignment from file: /home/suki/phylo-class/fixed_aligned_sequences.fasta
[00:00:00] Loaded alignment with 12 taxa and 267535 sites

Alignment comprises 1 partitions and 5658 patterns

Partition 0: noname
Model: GTR+FO+G4m
Alignment sites / patterns: 267535 / 5658
Gaps: 43.33 %
Invariant sites: 90.87 %


NOTE: Binary MSA file created: parsed_data.raxml.rba

* Estimated memory requirements                : 16 MB

* Recommended number of threads / MPI processes: 8

Please note that numbers given above are rough estimates only.
Actual memory consumption and parallel performance on your system may differ!

Alignment can be successfully read by RAxML-NG.


Execution log saved to: /home/suki/phylo-class/parsed_data.raxml.log

Analysis started: 13-Mar-2025 13:48:15 / finished: 13-Mar-2025 13:48:15

Elapsed time: 0.155 seconds

(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ less parsed_data.raxml.reduced.phy
parsed_data.raxml.reduced.phy: No such file or directory
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ raxml-ng --parse --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta --model GTR+G --prefix parsed_data

RAxML-NG v. 0.9.0 released on 20.05.2019 by The Exelixis Lab.
Developed by: Alexey M. Kozlov and Alexandros Stamatakis.
Contributors: Diego Darriba, Tomas Flouri, Benoit Morel, Sarah Lutteropp, Ben Bettisworth.
Latest version: https://github.com/amkozlov/raxml-ng
Questions/problems/suggestions? Please visit: https://groups.google.com/forum/#!forum/raxml

RAxML-NG was called at 13-Mar-2025 13:51:29 as follows:

raxml-ng --parse --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta --model GTR+G --prefix parsed_data

Analysis options:
  run mode: Alignment parsing and compression
  start tree(s):
  random seed: 1741891889
  tip-inner: OFF
  pattern compression: ON
  per-rate scalers: OFF
  site repeats: ON
  branch lengths: proportional (ML estimate, algorithm: NR-FAST)
  SIMD kernels: AVX2
  parallelization: PTHREADS (11 threads), thread pinning: OFF

[00:00:00] Reading alignment from file: /home/suki/phylo-class/fixed_aligned_sequences.fasta
[00:00:00] Loaded alignment with 12 taxa and 267535 sites

Alignment comprises 1 partitions and 5658 patterns

Partition 0: noname
Model: GTR+FO+G4m
Alignment sites / patterns: 267535 / 5658
Gaps: 43.33 %
Invariant sites: 90.87 %


NOTE: Binary MSA file created: parsed_data.raxml.rba

* Estimated memory requirements                : 16 MB

* Recommended number of threads / MPI processes: 8

Please note that numbers given above are rough estimates only.
Actual memory consumption and parallel performance on your system may differ!

Alignment can be successfully read by RAxML-NG.


Execution log saved to: /home/suki/phylo-class/parsed_data.raxml.log

Analysis started: 13-Mar-2025 13:51:29 / finished: 13-Mar-2025 13:51:29

Elapsed time: 0.136 seconds

(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ conda update -c bioconda raxml-ng
Channels:
 - bioconda
 - defaults
Platform: linux-64
Collecting package metadata (repodata.json): done
Solving environment: done

# All requested packages already installed.

(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ raxml-ng --parse --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta \
         --model GTR+G \
         --prefix parsed_data

RAxML-NG v. 0.9.0 released on 20.05.2019 by The Exelixis Lab.
Developed by: Alexey M. Kozlov and Alexandros Stamatakis.
Contributors: Diego Darriba, Tomas Flouri, Benoit Morel, Sarah Lutteropp, Ben Bettisworth.
Latest version: https://github.com/amkozlov/raxml-ng
Questions/problems/suggestions? Please visit: https://groups.google.com/forum/#!forum/raxml

RAxML-NG was called at 13-Mar-2025 13:54:33 as follows:

raxml-ng --parse --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta --model GTR+G --prefix parsed_data

Analysis options:
  run mode: Alignment parsing and compression
  start tree(s):
  random seed: 1741892073
  tip-inner: OFF
  pattern compression: ON
  per-rate scalers: OFF
  site repeats: ON
  branch lengths: proportional (ML estimate, algorithm: NR-FAST)
  SIMD kernels: AVX2
  parallelization: PTHREADS (11 threads), thread pinning: OFF

[00:00:00] Reading alignment from file: /home/suki/phylo-class/fixed_aligned_sequences.fasta
[00:00:00] Loaded alignment with 12 taxa and 267535 sites

Alignment comprises 1 partitions and 5658 patterns

Partition 0: noname
Model: GTR+FO+G4m
Alignment sites / patterns: 267535 / 5658
Gaps: 43.33 %
Invariant sites: 90.87 %


NOTE: Binary MSA file created: parsed_data.raxml.rba

* Estimated memory requirements                : 16 MB

* Recommended number of threads / MPI processes: 8

Please note that numbers given above are rough estimates only.
Actual memory consumption and parallel performance on your system may differ!

Alignment can be successfully read by RAxML-NG.


Execution log saved to: /home/suki/phylo-class/parsed_data.raxml.log

Analysis started: 13-Mar-2025 13:54:33 / finished: 13-Mar-2025 13:54:33

Elapsed time: 0.132 seconds

(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ raxml-ng --parse --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta \
         --model GTR+G \
         --prefix parsed_data \
         --msa-format PHYLIP

RAxML-NG v. 0.9.0 released on 20.05.2019 by The Exelixis Lab.
Developed by: Alexey M. Kozlov and Alexandros Stamatakis.
Contributors: Diego Darriba, Tomas Flouri, Benoit Morel, Sarah Lutteropp, Ben Bettisworth.
Latest version: https://github.com/amkozlov/raxml-ng
Questions/problems/suggestions? Please visit: https://groups.google.com/forum/#!forum/raxml

RAxML-NG was called at 13-Mar-2025 13:55:02 as follows:

raxml-ng --parse --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta --model GTR+G --prefix parsed_data --msa-format PHYLIP

Analysis options:
  run mode: Alignment parsing and compression
  start tree(s):
  random seed: 1741892102
  tip-inner: OFF
  pattern compression: ON
  per-rate scalers: OFF
  site repeats: ON
  branch lengths: proportional (ML estimate, algorithm: NR-FAST)
  SIMD kernels: AVX2
  parallelization: PTHREADS (11 threads), thread pinning: OFF

[00:00:00] Reading alignment from file: /home/suki/phylo-class/fixed_aligned_sequences.fasta

ERROR: Error loading MSA: Unable to parse PHYLIP file: /home/suki/phylo-class/fixed_aligned_sequences.fasta
 (LIBPLL-106): Invalid number of sequences in header

(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ ./raxml-ng --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta --model GTR+G --prefix T3 --threa
ds 2 --seed 2
-bash: ./raxml-ng: No such file or directory
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ ./raxml-ng --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta \ --model GTR+G --prefix T3 --thr
eads 2 --seed 2
-bash: ./raxml-ng: No such file or directory
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ raxml-ng --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta \
         --model GTR+G \
         --prefix my_tree \
         --threads 2 \
         --seed 42

RAxML-NG v. 0.9.0 released on 20.05.2019 by The Exelixis Lab.
Developed by: Alexey M. Kozlov and Alexandros Stamatakis.
Contributors: Diego Darriba, Tomas Flouri, Benoit Morel, Sarah Lutteropp, Ben Bettisworth.
Latest version: https://github.com/amkozlov/raxml-ng
Questions/problems/suggestions? Please visit: https://groups.google.com/forum/#!forum/raxml

RAxML-NG was called at 13-Mar-2025 13:59:17 as follows:

raxml-ng --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta --model GTR+G --prefix my_tree --threads 2 --seed 42

Analysis options:
  run mode: ML tree search
  start tree(s): random (10) + parsimony (10)
  random seed: 42
  tip-inner: OFF
  pattern compression: ON
  per-rate scalers: OFF
  site repeats: ON
  fast spr radius: AUTO
  spr subtree cutoff: 1.000000
  branch lengths: proportional (ML estimate, algorithm: NR-FAST)
  SIMD kernels: AVX2
  parallelization: PTHREADS (2 threads), thread pinning: OFF

[00:00:00] Reading alignment from file: /home/suki/phylo-class/fixed_aligned_sequences.fasta
[00:00:00] Loaded alignment with 12 taxa and 267535 sites

Alignment comprises 1 partitions and 5658 patterns

Partition 0: noname
Model: GTR+FO+G4m
Alignment sites / patterns: 267535 / 5658
Gaps: 43.33 %
Invariant sites: 90.87 %


NOTE: Binary MSA file created: my_tree.raxml.rba

[00:00:00] Generating 10 random starting tree(s) with 12 taxa
[00:00:00] Generating 10 parsimony starting tree(s) with 12 taxa
[00:00:00] Data distribution: max. partitions/sites/weight per thread: 1 / 2829 / 45264

Starting ML tree search with 20 distinct starting trees

[00:00:00 -727241.369933] Initial branch length optimization
[00:00:00 -605375.298996] Model parameter optimization (eps = 10.000000)
[00:00:00 -577350.804502] AUTODETECT spr round 1 (radius: 5)
[00:00:00 -529552.490036] AUTODETECT spr round 2 (radius: 10)
[00:00:00 -529552.486685] SPR radius for FAST iterations: 5 (autodetect)
[00:00:00 -529552.486685] Model parameter optimization (eps = 3.000000)
[00:00:00 -528899.801634] FAST spr round 1 (radius: 5)
[00:00:01 -528899.801625] Model parameter optimization (eps = 1.000000)
[00:00:01 -528899.801498] SLOW spr round 1 (radius: 5)
[00:00:01 -528899.801498] SLOW spr round 2 (radius: 10)
[00:00:02 -528899.801498] Model parameter optimization (eps = 0.100000)

[00:00:02] ML tree search #1, logLikelihood: -528899.801493

[00:00:02 -741471.230896] Initial branch length optimization
[00:00:02 -618833.985317] Model parameter optimization (eps = 10.000000)
[00:00:02 -585782.064952] AUTODETECT spr round 1 (radius: 5)
[00:00:02 -530754.791745] AUTODETECT spr round 2 (radius: 10)
[00:00:02 -530754.781736] SPR radius for FAST iterations: 5 (autodetect)
[00:00:02 -530754.781736] Model parameter optimization (eps = 3.000000)
[00:00:02 -530289.485000] FAST spr round 1 (radius: 5)
[00:00:03 -528950.653968] FAST spr round 2 (radius: 5)
[00:00:03 -528940.022865] FAST spr round 3 (radius: 5)
[00:00:03 -528940.022865] Model parameter optimization (eps = 1.000000)
[00:00:03 -528899.804102] SLOW spr round 1 (radius: 5)
[00:00:04 -528899.803994] SLOW spr round 2 (radius: 10)
[00:00:04 -528899.803994] Model parameter optimization (eps = 0.100000)

[00:00:04] ML tree search #2, logLikelihood: -528899.802127

[00:00:04 -748175.649501] Initial branch length optimization
[00:00:04 -624585.795695] Model parameter optimization (eps = 10.000000)
[00:00:05 -588593.448238] AUTODETECT spr round 1 (radius: 5)
[00:00:05 -529694.960304] AUTODETECT spr round 2 (radius: 10)
[00:00:05 -529694.960134] SPR radius for FAST iterations: 5 (autodetect)
[00:00:05 -529694.960134] Model parameter optimization (eps = 3.000000)
[00:00:05 -528909.920357] FAST spr round 1 (radius: 5)
[00:00:05 -528899.808632] FAST spr round 2 (radius: 5)
[00:00:06 -528899.808632] Model parameter optimization (eps = 1.000000)
[00:00:06 -528899.801810] SLOW spr round 1 (radius: 5)
[00:00:06 -528899.801810] SLOW spr round 2 (radius: 10)
[00:00:07 -528899.801810] Model parameter optimization (eps = 0.100000)

[00:00:07] ML tree search #3, logLikelihood: -528899.801681

[00:00:07 -746406.090808] Initial branch length optimization
[00:00:07 -620150.457332] Model parameter optimization (eps = 10.000000)
[00:00:07 -584945.233580] AUTODETECT spr round 1 (radius: 5)
[00:00:07 -529667.404531] AUTODETECT spr round 2 (radius: 10)
[00:00:07 -529667.401839] SPR radius for FAST iterations: 5 (autodetect)
[00:00:07 -529667.401839] Model parameter optimization (eps = 3.000000)
[00:00:07 -528909.920229] FAST spr round 1 (radius: 5)
[00:00:08 -528899.809059] FAST spr round 2 (radius: 5)
[00:00:08 -528899.809059] Model parameter optimization (eps = 1.000000)
[00:00:08 -528899.801947] SLOW spr round 1 (radius: 5)
[00:00:09 -528899.801946] SLOW spr round 2 (radius: 10)
[00:00:09 -528899.801946] Model parameter optimization (eps = 0.100000)

[00:00:09] ML tree search #4, logLikelihood: -528899.801771

[00:00:09 -708959.632572] Initial branch length optimization
[00:00:09 -585846.816498] Model parameter optimization (eps = 10.000000)
[00:00:09 -564687.639235] AUTODETECT spr round 1 (radius: 5)
[00:00:09 -529559.737739] AUTODETECT spr round 2 (radius: 10)
[00:00:09 -529559.736881] SPR radius for FAST iterations: 5 (autodetect)
[00:00:09 -529559.736881] Model parameter optimization (eps = 3.000000)
[00:00:09 -528909.920284] FAST spr round 1 (radius: 5)
[00:00:10 -528899.808427] FAST spr round 2 (radius: 5)
[00:00:10 -528899.808427] Model parameter optimization (eps = 1.000000)
[00:00:10 -528899.802133] SLOW spr round 1 (radius: 5)
[00:00:11 -528899.802132] SLOW spr round 2 (radius: 10)
[00:00:11 -528899.802132] Model parameter optimization (eps = 0.100000)

[00:00:11] ML tree search #5, logLikelihood: -528899.801916

[00:00:11 -734751.123701] Initial branch length optimization
[00:00:11 -608443.342060] Model parameter optimization (eps = 10.000000)
[00:00:11 -577595.576882] AUTODETECT spr round 1 (radius: 5)
[00:00:12 -530512.451867] AUTODETECT spr round 2 (radius: 10)
[00:00:12 -530512.451799] SPR radius for FAST iterations: 5 (autodetect)
[00:00:12 -530512.451799] Model parameter optimization (eps = 3.000000)
[00:00:12 -530041.933962] FAST spr round 1 (radius: 5)
[00:00:12 -528946.535059] FAST spr round 2 (radius: 5)
[00:00:12 -528935.986073] FAST spr round 3 (radius: 5)
[00:00:13 -528935.986073] Model parameter optimization (eps = 1.000000)
[00:00:13 -528899.803942] SLOW spr round 1 (radius: 5)
[00:00:14 -528899.803786] SLOW spr round 2 (radius: 10)
[00:00:14 -528899.803786] Model parameter optimization (eps = 0.100000)

[00:00:14] ML tree search #6, logLikelihood: -528899.801992

[00:00:14 -745884.792243] Initial branch length optimization
[00:00:14 -623433.998933] Model parameter optimization (eps = 10.000000)
[00:00:14 -586010.257348] AUTODETECT spr round 1 (radius: 5)
[00:00:14 -530216.996133] AUTODETECT spr round 2 (radius: 10)
[00:00:14 -530216.995809] SPR radius for FAST iterations: 5 (autodetect)
[00:00:14 -530216.995809] Model parameter optimization (eps = 3.000000)
[00:00:14 -529558.281556] FAST spr round 1 (radius: 5)
[00:00:15 -528922.844505] FAST spr round 2 (radius: 5)
[00:00:15 -528922.844505] Model parameter optimization (eps = 1.000000)
[00:00:15 -528899.802542] SLOW spr round 1 (radius: 5)
[00:00:16 -528899.802498] SLOW spr round 2 (radius: 10)
[00:00:16 -528899.802498] Model parameter optimization (eps = 0.100000)

[00:00:16] ML tree search #7, logLikelihood: -528899.802074

[00:00:16 -746207.756356] Initial branch length optimization
[00:00:16 -623977.630431] Model parameter optimization (eps = 10.000000)
[00:00:16 -588612.070470] AUTODETECT spr round 1 (radius: 5)
[00:00:16 -530118.345929] AUTODETECT spr round 2 (radius: 10)
[00:00:16 -530118.345200] SPR radius for FAST iterations: 5 (autodetect)
[00:00:16 -530118.345200] Model parameter optimization (eps = 3.000000)
[00:00:17 -529418.046539] FAST spr round 1 (radius: 5)
[00:00:17 -528915.603488] FAST spr round 2 (radius: 5)
[00:00:17 -528915.603488] Model parameter optimization (eps = 1.000000)
[00:00:17 -528899.802300] SLOW spr round 1 (radius: 5)
[00:00:18 -528899.802120] SLOW spr round 2 (radius: 10)
[00:00:18 -528899.802119] Model parameter optimization (eps = 0.100000)

[00:00:18] ML tree search #8, logLikelihood: -528899.801722

[00:00:18 -724286.886094] Initial branch length optimization
[00:00:18 -600904.501696] Model parameter optimization (eps = 10.000000)
[00:00:18 -574223.300464] AUTODETECT spr round 1 (radius: 5)
[00:00:18 -530459.093087] AUTODETECT spr round 2 (radius: 10)
[00:00:19 -530459.092945] SPR radius for FAST iterations: 5 (autodetect)
[00:00:19 -530459.092945] Model parameter optimization (eps = 3.000000)
[00:00:19 -530048.068274] FAST spr round 1 (radius: 5)
[00:00:19 -528947.928692] FAST spr round 2 (radius: 5)
[00:00:19 -528937.368905] FAST spr round 3 (radius: 5)
[00:00:20 -528937.368905] Model parameter optimization (eps = 1.000000)
[00:00:20 -528899.803952] SLOW spr round 1 (radius: 5)
[00:00:21 -528899.803795] SLOW spr round 2 (radius: 10)
[00:00:21 -528899.803795] Model parameter optimization (eps = 0.100000)

[00:00:21] ML tree search #9, logLikelihood: -528899.802078

[00:00:21 -740127.894444] Initial branch length optimization
[00:00:21 -616529.345424] Model parameter optimization (eps = 10.000000)
[00:00:21 -584133.155438] AUTODETECT spr round 1 (radius: 5)
[00:00:21 -529957.774922] AUTODETECT spr round 2 (radius: 10)
[00:00:21 -529957.774878] SPR radius for FAST iterations: 5 (autodetect)
[00:00:21 -529957.774878] Model parameter optimization (eps = 3.000000)
[00:00:21 -529434.598338] FAST spr round 1 (radius: 5)
[00:00:22 -528925.990414] FAST spr round 2 (radius: 5)
[00:00:22 -528915.553371] FAST spr round 3 (radius: 5)
[00:00:22 -528915.553371] Model parameter optimization (eps = 1.000000)
[00:00:23 -528899.802259] SLOW spr round 1 (radius: 5)
[00:00:23 -528899.802089] SLOW spr round 2 (radius: 10)
[00:00:23 -528899.802088] Model parameter optimization (eps = 0.100000)

[00:00:23] ML tree search #10, logLikelihood: -528899.801544

[00:00:23 -672232.973901] Initial branch length optimization
[00:00:23 -541092.301931] Model parameter optimization (eps = 10.000000)
[00:00:24 -528909.920426] AUTODETECT spr round 1 (radius: 5)
[00:00:24 -528909.920242] SPR radius for FAST iterations: 5 (autodetect)
[00:00:24 -528909.920242] Model parameter optimization (eps = 3.000000)
[00:00:24 -528909.919821] FAST spr round 1 (radius: 5)
[00:00:24 -528899.810941] FAST spr round 2 (radius: 5)
[00:00:24 -528899.810941] Model parameter optimization (eps = 1.000000)
[00:00:24 -528899.802318] SLOW spr round 1 (radius: 5)
[00:00:25 -528899.802317] SLOW spr round 2 (radius: 10)
[00:00:25 -528899.802317] Model parameter optimization (eps = 0.100000)

[00:00:25] ML tree search #11, logLikelihood: -528899.802069

[00:00:25 -672232.973901] Initial branch length optimization
[00:00:25 -541092.248589] Model parameter optimization (eps = 10.000000)
[00:00:26 -528909.920456] AUTODETECT spr round 1 (radius: 5)
[00:00:26 -528909.920248] SPR radius for FAST iterations: 5 (autodetect)
[00:00:26 -528909.920248] Model parameter optimization (eps = 3.000000)
[00:00:26 -528909.919851] FAST spr round 1 (radius: 5)
[00:00:26 -528899.810092] FAST spr round 2 (radius: 5)
[00:00:26 -528899.810092] Model parameter optimization (eps = 1.000000)
[00:00:26 -528899.802262] SLOW spr round 1 (radius: 5)
[00:00:25 -528899.802262] SLOW spr round 2 (radius: 10)
[00:00:25 -528899.802262] Model parameter optimization (eps = 0.100000)

[00:00:25] ML tree search #12, logLikelihood: -528899.802014

[00:00:25 -672232.973901] Initial branch length optimization
[00:00:25 -541092.268959] Model parameter optimization (eps = 10.000000)
[00:00:25 -528909.920454] AUTODETECT spr round 1 (radius: 5)
[00:00:25 -528909.920283] SPR radius for FAST iterations: 5 (autodetect)
[00:00:25 -528909.920283] Model parameter optimization (eps = 3.000000)
[00:00:25 -528909.919849] FAST spr round 1 (radius: 5)
[00:00:25 -528899.810038] FAST spr round 2 (radius: 5)
[00:00:26 -528899.810038] Model parameter optimization (eps = 1.000000)
[00:00:26 -528899.802325] SLOW spr round 1 (radius: 5)
[00:00:27 -528899.802324] SLOW spr round 2 (radius: 10)
[00:00:27 -528899.802324] Model parameter optimization (eps = 0.100000)

[00:00:27] ML tree search #13, logLikelihood: -528899.802069

[00:00:27 -672232.973901] Initial branch length optimization
[00:00:27 -541092.271165] Model parameter optimization (eps = 10.000000)
[00:00:27 -528909.920434] AUTODETECT spr round 1 (radius: 5)
[00:00:27 -528909.920244] SPR radius for FAST iterations: 5 (autodetect)
[00:00:27 -528909.920244] Model parameter optimization (eps = 3.000000)
[00:00:27 -528909.919847] FAST spr round 1 (radius: 5)
[00:00:27 -528899.810070] FAST spr round 2 (radius: 5)
[00:00:28 -528899.810070] Model parameter optimization (eps = 1.000000)
[00:00:28 -528899.802265] SLOW spr round 1 (radius: 5)
[00:00:28 -528899.802264] SLOW spr round 2 (radius: 10)
[00:00:29 -528899.802264] Model parameter optimization (eps = 0.100000)

[00:00:29] ML tree search #14, logLikelihood: -528899.802017

[00:00:29 -672232.973901] Initial branch length optimization
[00:00:29 -541092.261195] Model parameter optimization (eps = 10.000000)
[00:00:29 -528909.920436] AUTODETECT spr round 1 (radius: 5)
[00:00:29 -528909.920249] SPR radius for FAST iterations: 5 (autodetect)
[00:00:29 -528909.920249] Model parameter optimization (eps = 3.000000)
[00:00:29 -528909.919851] FAST spr round 1 (radius: 5)
[00:00:29 -528899.810030] FAST spr round 2 (radius: 5)
[00:00:30 -528899.810030] Model parameter optimization (eps = 1.000000)
[00:00:30 -528899.802267] SLOW spr round 1 (radius: 5)
[00:00:30 -528899.802267] SLOW spr round 2 (radius: 10)
[00:00:31 -528899.802267] Model parameter optimization (eps = 0.100000)

[00:00:31] ML tree search #15, logLikelihood: -528899.802020

[00:00:31 -672232.973901] Initial branch length optimization
[00:00:31 -541092.236610] Model parameter optimization (eps = 10.000000)
[00:00:31 -528909.920468] AUTODETECT spr round 1 (radius: 5)
[00:00:31 -528909.920262] SPR radius for FAST iterations: 5 (autodetect)
[00:00:31 -528909.920262] Model parameter optimization (eps = 3.000000)
[00:00:31 -528909.919869] FAST spr round 1 (radius: 5)
[00:00:31 -528899.809987] FAST spr round 2 (radius: 5)
[00:00:32 -528899.809987] Model parameter optimization (eps = 1.000000)
[00:00:32 -528899.802287] SLOW spr round 1 (radius: 5)
[00:00:32 -528899.802285] SLOW spr round 2 (radius: 10)
[00:00:32 -528899.802285] Model parameter optimization (eps = 0.100000)

[00:00:33] ML tree search #16, logLikelihood: -528899.802025

[00:00:33 -672232.973901] Initial branch length optimization
[00:00:33 -541092.248626] Model parameter optimization (eps = 10.000000)
[00:00:33 -528909.920467] AUTODETECT spr round 1 (radius: 5)
[00:00:33 -528909.920256] SPR radius for FAST iterations: 5 (autodetect)
[00:00:33 -528909.920256] Model parameter optimization (eps = 3.000000)
[00:00:33 -528909.919863] FAST spr round 1 (radius: 5)
[00:00:33 -528899.810060] FAST spr round 2 (radius: 5)
[00:00:34 -528899.810060] Model parameter optimization (eps = 1.000000)
[00:00:34 -528899.802288] SLOW spr round 1 (radius: 5)
[00:00:34 -528899.802286] SLOW spr round 2 (radius: 10)
[00:00:34 -528899.802286] Model parameter optimization (eps = 0.100000)

[00:00:34] ML tree search #17, logLikelihood: -528899.802027

[00:00:35 -672232.973901] Initial branch length optimization
[00:00:35 -541092.239420] Model parameter optimization (eps = 10.000000)
[00:00:35 -528909.920368] AUTODETECT spr round 1 (radius: 5)
[00:00:35 -528909.920249] SPR radius for FAST iterations: 5 (autodetect)
[00:00:35 -528909.920249] Model parameter optimization (eps = 3.000000)
[00:00:35 -528909.919856] FAST spr round 1 (radius: 5)
[00:00:35 -528899.810049] FAST spr round 2 (radius: 5)
[00:00:36 -528899.810049] Model parameter optimization (eps = 1.000000)
[00:00:36 -528899.802292] SLOW spr round 1 (radius: 5)
[00:00:36 -528899.802291] SLOW spr round 2 (radius: 10)
[00:00:36 -528899.802291] Model parameter optimization (eps = 0.100000)

[00:00:36] ML tree search #18, logLikelihood: -528899.802032

[00:00:36 -672232.973901] Initial branch length optimization
[00:00:36 -541092.248716] Model parameter optimization (eps = 10.000000)
[00:00:37 -528909.920435] AUTODETECT spr round 1 (radius: 5)
[00:00:37 -528909.920241] SPR radius for FAST iterations: 5 (autodetect)
[00:00:37 -528909.920241] Model parameter optimization (eps = 3.000000)
[00:00:37 -528909.919846] FAST spr round 1 (radius: 5)
[00:00:37 -528899.810096] FAST spr round 2 (radius: 5)
[00:00:37 -528899.810096] Model parameter optimization (eps = 1.000000)
[00:00:38 -528899.802263] SLOW spr round 1 (radius: 5)
[00:00:38 -528899.802261] SLOW spr round 2 (radius: 10)
[00:00:38 -528899.802261] Model parameter optimization (eps = 0.100000)

[00:00:38] ML tree search #19, logLikelihood: -528899.802015

[00:00:38 -672232.973901] Initial branch length optimization
[00:00:38 -541092.245553] Model parameter optimization (eps = 10.000000)
[00:00:39 -528909.920366] AUTODETECT spr round 1 (radius: 5)
[00:00:39 -528909.920245] SPR radius for FAST iterations: 5 (autodetect)
[00:00:39 -528909.920245] Model parameter optimization (eps = 3.000000)
[00:00:39 -528909.919852] FAST spr round 1 (radius: 5)
[00:00:39 -528899.810094] FAST spr round 2 (radius: 5)
[00:00:40 -528899.810094] Model parameter optimization (eps = 1.000000)
[00:00:40 -528899.802296] SLOW spr round 1 (radius: 5)
[00:00:40 -528899.802295] SLOW spr round 2 (radius: 10)
[00:00:40 -528899.802295] Model parameter optimization (eps = 0.100000)

[00:00:40] ML tree search #20, logLikelihood: -528899.802036


Optimized model parameters:

   Partition 0: noname
   Rate heterogeneity: GAMMA (4 cats, mean),  alpha: 0.307221 (ML),  weights&rates: (0.250000,0.005899) (0.250000,0.110123) (0.250000,0.607733) (0.250000,3.276245)
   Base frequencies (ML): 0.315594 0.185662 0.182809 0.315936
   Substitution rates (ML): 0.999606 1.744919 0.713196 0.668743 1.760275 1.000000


Final LogLikelihood: -528899.801493

AIC score: 1057859.602986 / AICc score: 1057859.609940 / BIC score: 1058174.513157
Free parameters (model + branch lengths): 30

Best ML tree saved to: /home/suki/phylo-class/my_tree.raxml.bestTree
All ML trees saved to: /home/suki/phylo-class/my_tree.raxml.mlTrees
Optimized model saved to: /home/suki/phylo-class/my_tree.raxml.bestModel

Execution log saved to: /home/suki/phylo-class/my_tree.raxml.log

Analysis started: 13-Mar-2025 13:59:17 / finished: 13-Mar-2025 13:59:58

Elapsed time: 40.970 seconds

(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ raxml-ng --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta \
         --model GTR+G \
         --prefix bootstrap_tree \
         --threads 4 \
         --seed 42 \
         --bs-trees 100

RAxML-NG v. 0.9.0 released on 20.05.2019 by The Exelixis Lab.
Developed by: Alexey M. Kozlov and Alexandros Stamatakis.
Contributors: Diego Darriba, Tomas Flouri, Benoit Morel, Sarah Lutteropp, Ben Bettisworth.
Latest version: https://github.com/amkozlov/raxml-ng
Questions/problems/suggestions? Please visit: https://groups.google.com/forum/#!forum/raxml

RAxML-NG was called at 13-Mar-2025 14:06:54 as follows:

raxml-ng --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta --model GTR+G --prefix bootstrap_tree --threads 4 --seed 42 --bs-trees 100

Analysis options:
  run mode: ML tree search
  start tree(s): random (10) + parsimony (10)
  random seed: 42
  tip-inner: OFF
  pattern compression: ON
  per-rate scalers: OFF
  site repeats: ON
  fast spr radius: AUTO
  spr subtree cutoff: 1.000000
  branch lengths: proportional (ML estimate, algorithm: NR-FAST)
  SIMD kernels: AVX2
  parallelization: PTHREADS (4 threads), thread pinning: OFF

[00:00:00] Reading alignment from file: /home/suki/phylo-class/fixed_aligned_sequences.fasta
[00:00:00] Loaded alignment with 12 taxa and 267535 sites

Alignment comprises 1 partitions and 5658 patterns

Partition 0: noname
Model: GTR+FO+G4m
Alignment sites / patterns: 267535 / 5658
Gaps: 43.33 %
Invariant sites: 90.87 %


NOTE: Binary MSA file created: bootstrap_tree.raxml.rba

[00:00:00] Generating 10 random starting tree(s) with 12 taxa
[00:00:00] Generating 10 parsimony starting tree(s) with 12 taxa
[00:00:00] Data distribution: max. partitions/sites/weight per thread: 1 / 1415 / 22640

Starting ML tree search with 20 distinct starting trees

[00:00:01] ML tree search #1, logLikelihood: -528899.801493
[00:00:02] ML tree search #2, logLikelihood: -528899.802127
[00:00:04] ML tree search #3, logLikelihood: -528899.801681
[00:00:05] ML tree search #4, logLikelihood: -528899.801771
[00:00:07] ML tree search #5, logLikelihood: -528899.801916
[00:00:08] ML tree search #6, logLikelihood: -528899.801992
[00:00:09] ML tree search #7, logLikelihood: -528899.802074
[00:00:11] ML tree search #8, logLikelihood: -528899.801722
[00:00:12] ML tree search #9, logLikelihood: -528899.802078
[00:00:14] ML tree search #10, logLikelihood: -528899.801544
[00:00:15] ML tree search #11, logLikelihood: -528899.802069
[00:00:16] ML tree search #12, logLikelihood: -528899.802014
[00:00:17] ML tree search #13, logLikelihood: -528899.802069
[00:00:18] ML tree search #14, logLikelihood: -528899.802017
[00:00:19] ML tree search #15, logLikelihood: -528899.802020
[00:00:20] ML tree search #16, logLikelihood: -528899.802025
[00:00:22] ML tree search #17, logLikelihood: -528899.802027
[00:00:23] ML tree search #18, logLikelihood: -528899.802032
[00:00:24] ML tree search #19, logLikelihood: -528899.802015
[00:00:25] ML tree search #20, logLikelihood: -528899.802036

Optimized model parameters:

   Partition 0: noname
   Rate heterogeneity: GAMMA (4 cats, mean),  alpha: 0.307221 (ML),  weights&rates: (0.250000,0.005899) (0.250000,0.110123) (0.250000,0.607733) (0.250000,3.276245)
   Base frequencies (ML): 0.315594 0.185662 0.182809 0.315936
   Substitution rates (ML): 0.999606 1.744919 0.713196 0.668743 1.760275 1.000000


Final LogLikelihood: -528899.801493

AIC score: 1057859.602986 / AICc score: 1057859.609940 / BIC score: 1058174.513157
Free parameters (model + branch lengths): 30

Best ML tree saved to: /home/suki/phylo-class/bootstrap_tree.raxml.bestTree
All ML trees saved to: /home/suki/phylo-class/bootstrap_tree.raxml.mlTrees
Optimized model saved to: /home/suki/phylo-class/bootstrap_tree.raxml.bestModel

Execution log saved to: /home/suki/phylo-class/bootstrap_tree.raxml.log

Analysis started: 13-Mar-2025 14:06:54 / finished: 13-Mar-2025 14:07:19

Elapsed time: 25.457 seconds

(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$                           