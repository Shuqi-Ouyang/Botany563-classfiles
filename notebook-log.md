Phylogenetics Course Dataset Description:
Eleven complete chloroplast genomes of Dipterocarpoideae in China+A complete chloroplast genome of Vatica guangxiensis
Paperlinks:
https://pmc.ncbi.nlm.nih.gov/articles/PMC8620154/
https://pmc.ncbi.nlm.nih.gov/articles/PMC7671599/

03/04/2025Distance and parsimony methods on your data
merged fasta file add to github, distance analysis failed, will keep trying on that
setwd("C:/Users/欧阳葭/Desktop")
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
> library(ape)
> library(phangorn)
> 
> sequences <- read.dna("D_Dataver1.fasta", format = "fasta")
> 
> dist_matrix <- dist.dna(sequences, model = "K80")
错误于as.matrix.DNAbin(x): 
  DNA sequences in list not of the same length.
