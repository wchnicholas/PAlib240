Some scripts for parsing NGS data from:
[Functional Constraint Profiling of a Viral Protein Reveals Discordance of Evolutionary Conservation and Functionality](http://journals.plos.org/plosgenetics/article?id=10.1371/journal.pgen.1005310)

* script/Mapper1.py: Mapping and calling mutations
	* Input:
	  * raw sequencing reads in fastq format
		* Fasta/flu3amp.fa
	* Output:	result/AllM_3 

* script/Mapper2.py: Filter clones with >1 mutations and generating a table that contains amino acid information
	* Input:
	  * Fasta/flu3offset
		* Fasta/BarCode
		* result/AllM_3
		* Fasta/flu3info
	* Output:
	  * result/WT_N_Depth
		* result/AGenotypes
		* result/SGenotypes
		* result/SMut'

* script/Mapper3.py: Generate a table only containing mutations with high confidence in fitness estimation (high input frequency)
	* Input:	result/SMut
	* Output:	result/HCMut
		* tmp/sil
		* tmp/mis
		* tmp/non

AN UPDATED VERSION OF Mapper1.py AND Mapper2.py CAN BE FOUND IN REPOSITORY:
https://github.com/wchnicholas/lib240
