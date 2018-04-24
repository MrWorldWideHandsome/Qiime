# Qiime
BIOC3301 ReadMe report codes

The Qiime folder contains the codes that were used for Metagenomic analysis of soil micrbiome

Order of the codes used:
<b>
1. Join Pair Ends
	
	This script takes the forward and reverse Illumina reads and joins them using SeqPrep (method chosen). Index file containing barcodes were included to match the surviving joined pairs to the barcodes. 

2. Split Libraries

	This script performs demultiplexing of Fastq sequence data where barcodes and sequences are contained in two separate fastq which are present on Illumina runs. 

3. Counting Sequences
	
	This script counts the sequences in the seqs.fna file and write the results to the desired output file.

4. Picking OTUs </b>

	Scripts picks OTUs in either closed reference, open reference or de novo reference method; and constructs an OTU table. The table is in a biom format that can be made human readable with the command: biom summarize -i /path/to/table. Default clustering tool was used, uclust. 
	
 4.a <i>Picking OTUs</i> 
 
	4.a1 Picking OTUs Open Reference
	
		- Reads are clustered against a reference sequence collection
		- Reads that do not hit the reference sequence are subsequently clustered de novo

	4.a2 Picking OTUs Closed Reference
	
		- Reads are clustered against a reference sequence collection
		- Reads that do not hit the reference sequence are  excluded from downstream analyses
		
	4.a3 Picking OTUs De novo Reference
	
		- Reads are clustered against one another without any external reference sequence collection
  
5. <b>Core Diversity</b>

	Scripts generates analysis of alpha diversity, beta diversity and taxanomy data. 

 5.a <i>Core Diversity</i>

	5.a1 Core Diversity Open Reference	
	5.a2 Core Diversity Closed Reference
	5.a3 Core Diversity De novo Reference
  
6. <b>adonis Analysis</b>

  6.a <i>adonis Analysis Open Reference Unweighted</i>
	
    6.a1 SampleLongtitude
    6.a2 SampleLatitude
    6.a3 SamplepH
    6.a4 SampleDepth
    6.a5 SamplePhosphorus
    6.a6 SampleNitrogen
    6.a7 SamplePotassium
    
  6.b <i>adonis Analysis Closed Reference Unweighted</i>
	
    6.b1 SampleLongtitude
    6.b2 SampleLatitude
    6.b3 SamplepH
    6.b4 SampleDepth
    6.b5 SamplePhosphorus
    6.b6 SampleNitrogen
    6.b7 SamplePotassium
    
7. <b>ANOSIM Analysis</b>

  7.a <i>ANOSIM Analysis Open Reference Unweighted</i>
	
    7.a1 SampleLongtitude
    7.a2 SampleLatitude
    7.a3 SamplepH
    7.a4 SampleDepth
    7.a5 SamplePhosphorus
    7.a6 SampleNitrogen
    7.a7 SamplePotassium
    
  7.b <i>ANOSIM Analysis Closed Reference Unweighted</i>
	
    7.b1 SampleLongtitude
    7.b2 SampleLatitude
    7.b3 SamplepH
    7.b4 SampleDepth
    7.b5 SamplePhosphorus
    7.b6 SampleNitrogen
    7.b7 SamplePotassium
