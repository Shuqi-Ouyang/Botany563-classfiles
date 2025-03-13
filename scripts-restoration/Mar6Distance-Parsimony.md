
R version 4.4.2 (2024-10-31 ucrt) -- "Pile of Leaves"
Copyright (C) 2024 The R Foundation for Statistical Computing
Platform: x86_64-w64-mingw32/x64

R是自由软件，不附带任何担保。
在某些条件下你可以将其自由分发。
用'license()'或'licence()'来看分发的详细条件。

R是个合作计划，有许多人为之做出了贡献.
用'contributors()'来看合著者的详细情况
用'citation()'会告诉你如何在出版物中正确地引用R或R程序包。

用'demo()'来看一些示例程序，用'help()'来阅读在线帮助文件，或
用'help.start()'通过HTML浏览器来看帮助文件。
输入'q()'退出R.

[Workspace loaded from ~/.RData]

> getwd
function () 
.Internal(getwd())
<bytecode: 0x000001f636eafff0>
<environment: namespace:base>
> setwd("C:/Users/欧阳葭/Desktop")
> 
> library(ape)
> sequences <- read.dna("D_Dataver1.fasta", format = "fasta")
> print(sequences)
8 DNA sequences in binary format stored in a list.

Mean sequence length: 151780.1 
   Shortest sequence: 151493 
    Longest sequence: 152100 

Labels:
MZ160998.1 Vatica odorata chloroplast, complete genome
MZ160997.1 Rubroshorea leprosula chloroplast, complete genom...
MZ160996.1 Anthoshorea roxburghii chloroplast, complete geno...
MZ160995.1 Anthoshorea henryana chloroplast, complete genome
MZ160994.1 Hopea odorata chloroplast, complete genome
MZ160993.1 Hopea mollissima chloroplast, complete genome
...

Base composition:
    a     c     g     t 
0.311 0.188 0.185 0.316 
(Total: 1.21 Mb)
> 
> # 加载所需库
> library(ape)
> library(phangorn)
> 
> # 读取FASTA文件
> sequences <- read.dna("D_Dataver1.fasta", format = "fasta")
> 
> # 计算距离矩阵（使用Kimura 2-parameter模型）
> dist_matrix <- dist.dna(sequences, model = "K80")
错误于as.matrix.DNAbin(x): 
  DNA sequences in list not of the same length.
> aligned_sequences <- read.dna("aligned_sequences.fasta", format = "fasta")
> library(ape)
> 
> # 读取比对后的 FASTA 文件
> dna <- read.dna("C:/Users/欧阳葭/Desktop/aligned_sequences.fasta", format = "fasta")
> 
> # 查看数据
> print(dna)
12 DNA sequences in binary format stored in a matrix.

All sequences of same length: 267535 

Labels:
MZ160998.1 Vatica odorata chloroplast, complete genome
MZ160997.1 Rubroshorea leprosula chloroplast, complete genom...
MZ160996.1 Anthoshorea roxburghii chloroplast, complete geno...
MZ160995.1 Anthoshorea henryana chloroplast, complete genome
MZ160994.1 Hopea odorata chloroplast, complete genome
MZ160993.1 Hopea mollissima chloroplast, complete genome
...

Base composition:
    a     c     g     t 
0.311 0.188 0.185 0.317 
(Total: 3.21 Mb)
> 
> dna
12 DNA sequences in binary format stored in a matrix.

All sequences of same length: 267535 

Labels:
MZ160998.1 Vatica odorata chloroplast, complete genome
MZ160997.1 Rubroshorea leprosula chloroplast, complete genom...
MZ160996.1 Anthoshorea roxburghii chloroplast, complete geno...
MZ160995.1 Anthoshorea henryana chloroplast, complete genome
MZ160994.1 Hopea odorata chloroplast, complete genome
MZ160993.1 Hopea mollissima chloroplast, complete genome
...

Base composition:
    a     c     g     t 
0.311 0.188 0.185 0.317 
(Total: 3.21 Mb)
> class(dna)
[1] "DNAbin"
> as.character(dna)[1:5,1:10]
                                                               [,1]
MZ160998.1 Vatica odorata chloroplast, complete genome         "-" 
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome  "-" 
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome "a" 
MZ160995.1 Anthoshorea henryana chloroplast, complete genome   "-" 
MZ160994.1 Hopea odorata chloroplast, complete genome          "-" 
                                                               [,2]
MZ160998.1 Vatica odorata chloroplast, complete genome         "-" 
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome  "-" 
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome "t" 
MZ160995.1 Anthoshorea henryana chloroplast, complete genome   "-" 
MZ160994.1 Hopea odorata chloroplast, complete genome          "-" 
                                                               [,3]
MZ160998.1 Vatica odorata chloroplast, complete genome         "-" 
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome  "-" 
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome "g" 
MZ160995.1 Anthoshorea henryana chloroplast, complete genome   "-" 
MZ160994.1 Hopea odorata chloroplast, complete genome          "-" 
                                                               [,4]
MZ160998.1 Vatica odorata chloroplast, complete genome         "-" 
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome  "-" 
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome "a" 
MZ160995.1 Anthoshorea henryana chloroplast, complete genome   "-" 
MZ160994.1 Hopea odorata chloroplast, complete genome          "-" 
                                                               [,5]
MZ160998.1 Vatica odorata chloroplast, complete genome         "-" 
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome  "-" 
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome "t" 
MZ160995.1 Anthoshorea henryana chloroplast, complete genome   "-" 
MZ160994.1 Hopea odorata chloroplast, complete genome          "-" 
                                                               [,6]
MZ160998.1 Vatica odorata chloroplast, complete genome         "-" 
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome  "-" 
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome "a" 
MZ160995.1 Anthoshorea henryana chloroplast, complete genome   "-" 
MZ160994.1 Hopea odorata chloroplast, complete genome          "-" 
                                                               [,7]
MZ160998.1 Vatica odorata chloroplast, complete genome         "-" 
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome  "-" 
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome "a" 
MZ160995.1 Anthoshorea henryana chloroplast, complete genome   "-" 
MZ160994.1 Hopea odorata chloroplast, complete genome          "-" 
                                                               [,8]
MZ160998.1 Vatica odorata chloroplast, complete genome         "-" 
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome  "-" 
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome "t" 
MZ160995.1 Anthoshorea henryana chloroplast, complete genome   "-" 
MZ160994.1 Hopea odorata chloroplast, complete genome          "-" 
                                                               [,9]
MZ160998.1 Vatica odorata chloroplast, complete genome         "-" 
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome  "-" 
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome "t" 
MZ160995.1 Anthoshorea henryana chloroplast, complete genome   "-" 
MZ160994.1 Hopea odorata chloroplast, complete genome          "-" 
                                                               [,10]
MZ160998.1 Vatica odorata chloroplast, complete genome         "-"  
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome  "-"  
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome "t"  
MZ160995.1 Anthoshorea henryana chloroplast, complete genome   "-"  
MZ160994.1 Hopea odorata chloroplast, complete genome          "-"  
> unclass(dna)[1:5,1:10]
                                                               [,1]
MZ160998.1 Vatica odorata chloroplast, complete genome           04
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome    04
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome   88
MZ160995.1 Anthoshorea henryana chloroplast, complete genome     04
MZ160994.1 Hopea odorata chloroplast, complete genome            04
                                                               [,2]
MZ160998.1 Vatica odorata chloroplast, complete genome           04
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome    04
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome   18
MZ160995.1 Anthoshorea henryana chloroplast, complete genome     04
MZ160994.1 Hopea odorata chloroplast, complete genome            04
                                                               [,3]
MZ160998.1 Vatica odorata chloroplast, complete genome           04
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome    04
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome   48
MZ160995.1 Anthoshorea henryana chloroplast, complete genome     04
MZ160994.1 Hopea odorata chloroplast, complete genome            04
                                                               [,4]
MZ160998.1 Vatica odorata chloroplast, complete genome           04
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome    04
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome   88
MZ160995.1 Anthoshorea henryana chloroplast, complete genome     04
MZ160994.1 Hopea odorata chloroplast, complete genome            04
                                                               [,5]
MZ160998.1 Vatica odorata chloroplast, complete genome           04
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome    04
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome   18
MZ160995.1 Anthoshorea henryana chloroplast, complete genome     04
MZ160994.1 Hopea odorata chloroplast, complete genome            04
                                                               [,6]
MZ160998.1 Vatica odorata chloroplast, complete genome           04
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome    04
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome   88
MZ160995.1 Anthoshorea henryana chloroplast, complete genome     04
MZ160994.1 Hopea odorata chloroplast, complete genome            04
                                                               [,7]
MZ160998.1 Vatica odorata chloroplast, complete genome           04
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome    04
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome   88
MZ160995.1 Anthoshorea henryana chloroplast, complete genome     04
MZ160994.1 Hopea odorata chloroplast, complete genome            04
                                                               [,8]
MZ160998.1 Vatica odorata chloroplast, complete genome           04
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome    04
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome   18
MZ160995.1 Anthoshorea henryana chloroplast, complete genome     04
MZ160994.1 Hopea odorata chloroplast, complete genome            04
                                                               [,9]
MZ160998.1 Vatica odorata chloroplast, complete genome           04
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome    04
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome   18
MZ160995.1 Anthoshorea henryana chloroplast, complete genome     04
MZ160994.1 Hopea odorata chloroplast, complete genome            04
                                                               [,10]
MZ160998.1 Vatica odorata chloroplast, complete genome            04
MZ160997.1 Rubroshorea leprosula chloroplast, complete genome     04
MZ160996.1 Anthoshorea roxburghii chloroplast, complete genome    18
MZ160995.1 Anthoshorea henryana chloroplast, complete genome      04
MZ160994.1 Hopea odorata chloroplast, complete genome             04
> library(ape)
> dna <- read.dna("C:/Users/欧阳葭/Desktop/fixed_aligned_sequences.fasta", format = "fasta")
> 
> class(dna)
[1] "DNAbin"
> as.character(dna)[1:5,1:10]
           [,1] [,2] [,3] [,4] [,5] [,6] [,7] [,8]
MZ160998.1 "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-" 
MZ160997.1 "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-" 
MZ160996.1 "a"  "t"  "g"  "a"  "t"  "a"  "a"  "t" 
MZ160995.1 "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-" 
MZ160994.1 "-"  "-"  "-"  "-"  "-"  "-"  "-"  "-" 
           [,9] [,10]
MZ160998.1 "-"  "-"  
MZ160997.1 "-"  "-"  
MZ160996.1 "t"  "t"  
MZ160995.1 "-"  "-"  
MZ160994.1 "-"  "-"  
> library(ape)
> 
> # 读取对齐后的 FASTA 文件
> dna <- read.dna("C:/Users/欧阳葭/Desktop/aligned_sequences.fasta", format = "fasta")
> 
> # 去除全是 gap 的列
> dna_clean <- del.gaps(dna, "all")  # 只删除全是 gap 的位点
错误于del.gaps(dna, "all"): 参数没有用("all")
> dna <- read.dna("C:/Users/欧阳葭/Desktop/fixed_aligned_sequences.fasta", format = "fasta")
> library(ips)  # del.gaps() 在 ips 包里
错误于library(ips): 不存在叫‘ips’这个名称的程序包
> library(ape)
> 
> # 计算距离矩阵（使用 Kimura 2-parameter 模型）
> dist_matrix <- dist.dna(dna, model = "K80")
> 
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
> 
> > unclass(dna)[1:5,1:10]
错误: 意外的'>'在">"里
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
> 
> temp <- as.data.frame(as.matrix(D))
> table.paint(temp, cleg=0, clabel.row=.5, clabel.col=.5)
错误于table.paint(temp, cleg = 0, clabel.row = 0.5, clabel.col = 0.5): 
  没有"table.paint"这个函数
> library(ade4)
> 
> # 画出 pairwise 距离矩阵的可视化表格
> table.paint(temp, cleg=0, clabel.row=.5, clabel.col=.5)
> 
> temp<-t(as.matrix(D))
> temp<-temp[,ncol(temp):1]
> par(mar=c(1,5,5,1))
> image(x=1:80,y=1:80,temp,col=rev(heat.colors(100)),xaxt="n",yaxt="n",
+       + xlab="",ylab="")
错误: 意外的'=' 于
"image(x=1:80,y=1:80,temp,col=rev(heat.colors(100)),xaxt="n",yaxt="n",
      + xlab="
> image(x=1:80,y=1:80,temp,col=rev(heat.colors(100)),xaxt="n",yaxt="n", xlab="",ylab="")
错误于image.default(x = 1:80, y = 1:80, temp, col = rev(heat.colors(100)), : 
  z的大小应该等于length(x)(-1)乘length(y)(-1)
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