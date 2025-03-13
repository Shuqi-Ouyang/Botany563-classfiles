## **Notebook reproducible script for Botany 563-Shuqi**

<aside>
💡

> Note: All the original scripts, including errors, are restored by date in the “scripts restoration” folder.
> 
</aside>


### Choosing data and performing QC

02/11/2025 Attempt1 

Phylogenetics Course Dataset Description
11 complete chloroplast genomes of Dipterocarpoideae in China (https://pmc.ncbi.nlm.nih.gov/articles/PMC8620154/) and
1 complete chloroplast genome of Vatica guangxiensis (https://pmc.ncbi.nlm.nih.gov/articles/PMC7671599/)


### Installing Windows Subsystem for Linux (WSL)

02/11/2025

Fail to run conda and miniconda on my windows system, thus I decide to install WSL.

1. For Win11 system users like me with a "Destination Folder' cannot contain non-ascii characters" error when installing miniconda, one solution is to install it in another location like "D:\miniconda3", then add the exact location to SystemProperties-Advanced-Environmental Variables-Path.
2. But after that, I found there is no adequate Wins version of Clustalw/T-coffee/Muscle on any channels of Conda. If still want to use Conda to run them, one possible way is to install WSL(Windows Subsystem for Linux setting). If not, just install Muscle online, which should run stably on Win system. The scirpts to install WSL: wsl --install.
3. Restart to check whether WSL is running. If not, make sure if these Windows Features "Windows Subsystem for Linux, Virtual Machine Platform, Windows Hypervisor Platform, and Hyper-V" are on. Then restart.
4. And then miniconda can be installed smoothly, as well as Clustalw and Muscle. However, T-coffee is still not installable.


### Installing Miniconda, Clustalw, Muscle, and Maftt for MSA

02/11/2025 Attempt1
Installing Clustalw and Muscle in Miniconda.

02/18/2025 Attempt2
Adding Maftt in Miniconda.


### Aligning data

02/18/2025 Attempt1
Aligning two taxa, Vatica guangxiensis and Vatica Xishuangbanansis

03/04/2025 Attempt2
1. Aligning total 12 taxa through Maftt
Original Scripts:
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


2. Cutting the unnecessary part in taxa name-line through python.
(base) suki@LAPTOP-5PMP3V9O:~$ conda create -n fasta_clean python=3.9 -y
(fasta_clean) suki@LAPTOP-5PMP3V9O:~$ pip install biopython
(fasta_clean) suki@LAPTOP-5PMP3V9O:~$ from Bio import SeqIO
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



### Distance and parsimony methods on data
03/06/2025 Attempt1
Using Rstudio.
Original scripts:
> setwd("C:/Users/欧阳葭/Desktop")
> 
> library(ape)
> sequences <- read.dna("D_Dataver1.fasta", format = "fasta")
> print(sequences)
> dna <- read.dna("C:/Users/欧阳葭/Desktop/fixed_aligned_sequences.fasta", format = "fasta")
> # 计算距离矩阵（使用 Kimura 2-parameter 模型）
> dist_matrix <- dist.dna(dna, model = "K80")
> # 查看距离矩阵是否正常
> print(dist_matrix)
             MZ160998.1   MZ160997.1   MZ160996.1
MZ160997.1 0.1836115165                          
MZ160996.1 0.1815581687 0.0125499878             
MZ160995.1 0.1808712100 0.1619366759 0.1559154016
MZ160994.1 0.0222515634 0.1777867660 0.1743549718
MZ160993.1 0.0196551134 0.1776097558 0.1745030216
MZ160992.1 0.0557735202 0.2306146819 0.2288480922
MZ160991.1 0.0192417218 0.1852947683 0.1834163117
MZ379792.1 0.0194133941 0.1852018680 0.1833522129
MZ397801.1 0.0039363003 0.1842436092 0.1823708268
MZ397800.1 0.0039366018 0.1833634573 0.1811657134
MT934442.1 0.0007379676 0.1831482460 0.1810650356
             MZ160995.1   MZ160994.1   MZ160993.1
MZ160997.1                                       
MZ160996.1                                       
MZ160995.1                                       
MZ160994.1 0.1760830954                          
MZ160993.1 0.1733155256 0.0052055453             
MZ160992.1 0.2264173701 0.0556593841 0.0533493927
MZ160991.1 0.1813843345 0.0205111593 0.0176533153
MZ379792.1 0.1812862221 0.0205358242 0.0177020740
MZ397801.1 0.1814781989 0.0227173610 0.0200705061
MZ397800.1 0.1826015591 0.0200212303 0.0212224095
MT934442.1 0.1805941676 0.0220303080 0.0194347220
             MZ160992.1   MZ160991.1   MZ379792.1
MZ160997.1                                       
MZ160996.1                                       
MZ160995.1                                       
MZ160994.1                                       
MZ160993.1                                       
MZ160992.1                                       
MZ160991.1 0.0428434089                          
MZ379792.1 0.0428939502 0.0019298904             
MZ397801.1 0.0561077709 0.0194858405 0.0196575673
MZ397800.1 0.0576803704 0.0211256879 0.0212978618
MT934442.1 0.0556180887 0.0190701175 0.0192417218
             MZ397801.1   MZ397800.1
MZ160997.1                          
MZ160996.1                          
MZ160995.1                          
MZ160994.1                          
MZ160993.1                          
MZ160992.1                          
MZ160991.1                          
MZ379792.1                          
MZ397801.1                          
MZ397800.1 0.0068844871             
MT934442.1 0.0037210335 0.0036734442
>  unclass(dna)[1:5,1:10]
           [,1] [,2] [,3] [,4] [,5] [,6] [,7] [,8]
MZ160998.1   04   04   04   04   04   04   04   04
MZ160997.1   04   04   04   04   04   04   04   04
MZ160996.1   88   18   48   88   18   88   88   18
MZ160995.1   04   04   04   04   04   04   04   04
MZ160994.1   04   04   04   04   04   04   04   04
           [,9] [,10]
MZ160998.1   04    04
MZ160997.1   04    04
MZ160996.1   18    18
MZ160995.1   04    04
MZ160994.1   04    04
> typeof(unclass(dna)[1:5,1:10])
[1] "raw"
> object.size(as.character(dna))/object.size(dna)
8 bytes
> library(ape)
> 
> # 计算基因距离矩阵（使用 TN93 模型）
> D <- dist.dna(dna, model = "TN93")
> 
> # 查看矩阵的结构
> class(D)  # 应该返回 "dist"
[1] "dist"
> length(D) # 查看 pairwise 距离数量
[1] 66
> temp <- as.data.frame(as.matrix(D))

NJ tree
> table.paint(temp, cleg=0, clabel.row=.5, clabel.col=.5)
> temp<-t(as.matrix(D))
> temp<-temp[,ncol(temp):1]
> par(mar=c(1,5,5,1))
> dim(temp)
[1] 12 12
> image(x = 1:12, y = 1:12, z = temp,
+       col = rev(heat.colors(100)), xlab = "", ylab = "")
> 
> axis(side=2,at=1:12,lab=rownames(dna),las=2,cex.axis=.5)
> axis(side=3,at=1:12,lab=rownames(dna),las=3,cex.axis=.5)
> tre<-nj(D)
> class(tre)
[1] "phylo"
> tre<-ladderize(tre)
> tre

Phylogenetic tree with 12 tips and 10 internal nodes.

Tip labels:
  MZ160998.1, MZ160997.1, MZ160996.1, MZ160995.1, MZ160994.1, MZ160993.1, ...

Unrooted; includes branch length(s).
> plot(tre,cex=.6)
> title ("Dipterocarpaceae NJ tree ver1.0")


Parsimony Tree
> dna2 <- as.phyDat(dna)
> class(dna2)
[1] "phyDat"
> dna2
12 sequences with 267535 character and 5658 different site patterns.
The states are a c g t 
> tre.ini <- nj(dist.dna(dna,model="raw"))
> tre.ini

Phylogenetic tree with 12 tips and 10 internal nodes.

Tip labels:
  MZ160998.1, MZ160997.1, MZ160996.1, MZ160995.1, MZ160994.1, MZ160993.1, ...

Unrooted; includes branch length(s).
> parsimony(tre.ini, dna2)
[1] 28914
> tre.pars <- optim.parsimony(tre.ini, dna2)
Final p-score 28914 after  0 nni operations 
> tre.pars

Phylogenetic tree with 12 tips and 10 internal nodes.

Tip labels:
  MZ160998.1, MZ160997.1, MZ160996.1, MZ160995.1, MZ160994.1, MZ160993.1, ...

Unrooted; no branch length.
> plot(tre.pars, type="unr", show.tip.label=FALSE, edge.width=2)
> title("Maximum Parsimony Tree")
> 
> plot(tre.pars, type = "unr", show.tip.label = TRUE, edge.width = 2, cex=0.7)
> 
> plot(tre.pars, type="unr", show.tip.label=FALSE, edge.width=2)
> title("Maximum Parsimony Tree")
> 
> # 获取树叶名称（物种编号）
> my_tips <- tre.pars$tip.label
> 
> # 为每个tip添加文字和背景色
> tiplabels(
+     text = my_tips,       # 标签内容（向量，与树的tip顺序一致）
+     bg   = "lightblue",   # 背景颜色（可以是单一颜色或向量）
+     cex  = 0.7,           # 字体大小
+     fg   = "black",       # 字体颜色或边框颜色
+     adj  = 0.5            # 文字相对于tip的对齐方式
+ )
> 
> my_colors <- rainbow(length(my_tips))
> 
> plot(tre.pars, type="unr", show.tip.label=FALSE, edge.width=2)
> title("Maximum Parsimony Tree")
> 
> tiplabels(
+     text = my_tips,
+     bg   = my_colors,  # 为每个物种分配不同颜色
+     cex  = 0.7,
+     fg   = "black"
+ )
> 
> # 如果想加图例：
> legend("bottomleft", legend = my_tips, fill = my_colors, cex = 0.6, bg="white")
> 
> plot(tre.pars, type="fan", show.tip.label=FALSE, edge.width=2)
> 
> plot(tre.pars, type = "unr", show.tip.label = TRUE, edge.width = 2, cex=0.7)
> 
> plot(tre.pars, type="fan", show.tip.label=FALSE, edge.width=2)
> 
> plot(
+     tre.pars, 
+     type = "fan",             # 或 "unr"/"radial"
+     show.tip.label = TRUE,    # 显示 tip label
+     cex = 0.8,                # 调整字体大小
+     label.offset = 0.01,      # 给标签留一点间隔
+     edge.width = 2
+ )
> 
> my_colors <- rainbow(length(my_tips))
> 
> plot(tre.pars, type="fan", show.tip.label=FALSE, edge.width=2)
> title("Maximum Parsimony Tree")
> 
> tiplabels(
+     text = my_tips,
+     bg   = my_colors,  # 为每个物种分配不同颜色
+     cex  = 0.7,
+     fg   = "black"
+ )
> 
> # 如果想加图例：
> legend("bottomleft", legend = my_tips, fill = my_colors, cex = 0.6, bg="white")

### Running RAxML

03/13/2025 Attempt1
Using RAxML-NG to run my data for three times, each time with different setting, using the last time's output.
Original Scripts:
(iqtree-env) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ conda activate raxml-n
g-env
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:/mnt/c/Users/欧阳葭$ raxml-ng --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta \
         --model GTR+G \
         --prefix test_run \
         --seed 12345
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ cat /home/suki/phylo-class
/test_run.raxml.bestTree
(MZ379792.1:0.001131,MZ160991.1:0.001327,(MZ160992.1:0.045484,(((MZ160993.1:0.001916,MZ160994.1:0.003971):0.003316,(MZ160995.1:0.034423,(MZ160997.1:0.013106,MZ160996.1:0.005338):0.030318):0.035859):0.007575,(MZ397801.1:0.002712,((MT934442.1:0.000319,MZ397800.1:0.002830):0.000079,MZ160998.1:0.000639):0.001929):0.013448):0.009202):0.003035):0.0;

#并没有产生phy文件，也许是数据量比较小
(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ raxml-ng --parse --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta --model GTR+G --prefix parsed_data

(raxml-ng-env) suki@LAPTOP-5PMP3V9O:~/phylo-class$ raxml-ng --msa /home/suki/phylo-class/fixed_aligned_sequences.fasta \
         --model GTR+G \
         --prefix my_tree \
         --threads 2 \
         --seed 42

加入了bootstrap, seed设定为42, threads 设定为2
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





