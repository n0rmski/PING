This is to extract reads that map to the KIR region from unmapped fastq files.
For reads already mapped to the genome then take all reads within the (hg19) coordinates  chr19:55228188-55383188 and chr19: unmapped GL000209.1. You may want to look for good quality reads in the unmapped bin as well.
MIRA_cleanReads.bat shortens the read names so that MIRA doesn't crash (not needed if you use the R version of PING or the later versions of MIRA).

2013 is the version used on the IHWG cell lines and Trios for the paper.
BT2 is the Bowtie 2 version, which handles longer reads and indels better.