# Week 1

## 4 steps of bioinformatics
  0. Cast a **question** based on extant biological/medical knowledge
  1. Utilize technology (*e.g.* sequencing) to obtain biological/medical data (*i.e.* **information**)
  2. Utilize bioinformatics tools to conduct **analysis** of such information, such as clean & feature extraction, *etc.*
  3. Utilize extant (or construct novel) **probabilistic models or computational algorithms** for better excavation of latent biological paradigms and conclusions
  4. Cast a **question** based on data analysis and finally explain its biological significance

**NOTE1**  There are two types of bioinformatics study patterns (*hypothesis driven*: 0->1->2->3 *v.s.* *data driven*: 1->2->3->4)

**NOTE2**  The differences between models and algorithms:  
    (1). ***MODEL*** is the scaffold where variables are correlated with each other. In a certain model, we use *parameters* to depict the relationships among variables. For different kinds of questions, 'proper' models should be usesd, from the very basic linear models to deep learning.   
    (2). ***Algorithm*** is the method we use to solve a specific programming problem, for instance, to get the parameters of a certain models. Efficient algorithms may help greatly reduce the running time or storage space consumed by a program.


## My learning plan of this course
1. Aside from '*linux*', Use '*python*' to complete every program so as to command common python-based bioinformatics analysis pipelines.
2. Follow the pipelines on the tutorial firstly, and run those analyses with other overt data, to get more familiar with those standard pipelines.
3. Pay more attention on how those analysis methods are constructed and realized rather than simply how to run extant pipelines, and think whether I can contribute to the opimization of extant models or algorithms. : )



# Week 2

## Bioinfomatics examples
### 1-D study: gene prediction for DNA
  Better to say *a gene* is *a piece of information* rather than a segment of DNA (think about protein virus).
  To predict a gene given a segment of DNA? **HMM** and **Viterbi algorithm** to detect the hidden state of DNA (exon or intron)
### 2-D study: structure prediction for RNA
  To recognize a segemnt of RNA: biophysics(spatial structure) *v.s.* linguistics(AUCG sequence)
  Model for RNA 2nd structure prediction: **SCFG (stochastic context free grammar)**
### 3-D study: structure prediction for Protein
  To recognize a 3rd structure: biophysics(energy landscape simulation) *v.s.* linguistics(transformer)
### H-D study: Prediction Medicine for Human
  Question: genetic variation diagnosis & personal health
  
## Linux basic knowledge
  One of **Operating System** (parallel with Mac, Windows *etc.*)
  User -- **Shell(*e.g.* bash)** -- Kernel -- 



# Week 3

## sequence alignment
general approach to pairwise alignment:
1. choose 2 sequences.
2. select an algorithm that generates a score.
3. allow gaps(insertion, deletions)
4. score reflects degree of similarity.
5. alignments can be global or local.
6. estimate probability that the alignment occurred by chance

### score matrix 
  objective: to derive a scoring function that best reflects the evolutionary relationship and biological reality
### N-W algorithm (dynamic programming, global)
  *note*: some highly short moitifs may be ignored because N-W is based on global alignment.
  Max(s) = (#matches)*m - (#mismatches)*s - (#gaps)*d
  score matrix: the max score at each cell is the sum of the original score in the cell and the highest score in the previous column or row.
                after finishing, trace back along the route with all highest scores.
### S-W algorithm (local)
  score matrix: the score in each cell is the max possible score for an alignment of any length ending at the position
                after finishing, find the highest scoring cell, then trace the way back to the beginning

## Blast (Basic Local Alignment Search Tool, *pairwise alignment*)
### heuristic methods: 
  intuition: two biological sequences are likeliy to be similar if the have a sufficient number of short local matches (hits or tuples) that are in the same order.
  method: pre-compute a **hash-table**, which lists a positions every possible tuple.
### Blast statistics:
  p-value: prob that an event occurs by chance
  e-value: correction of the p-value for multiple testing

## conversation analysis (one application of sequence alignment)

 
