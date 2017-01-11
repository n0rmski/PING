# PING
These are the scripts and pipelines for calling KIR genotypes from NGS data; they form the components of PING (Pushing Immunogenetics to the Next Generation)

The scripts for harvesting KIR specific reads are here:
https://web.stanford.edu/~n0rmski/projectH/PING/0_harvestKIR_reads/

There are three levels of KIR genotyping software included in the other folders:

1. The scripts that were used to generate the allele calls from the IHWG cell lines, which are reported in the paper  (Supplementary Table S3)
These are the static, working and complete versions of PING that will not be changed
https://web.stanford.edu/~n0rmski/projectH/PING/1_PING_scripts/

2. As we moved to longer reads we updated all of the scripts and programs, and these are also included (e.g the BT2 versions).
These later versions will be updated as we find more alleles etc, and are recommended for use over the older versions.
 -in these, the scripts used to generate vcf (SOS) remain separate from the algorithms that call the alleles (jSOS).
https://web.stanford.edu/~n0rmski/projectH/PING/2_SOS_BT2_KFF/

3. Finally, we have ported the scripts into standalone R programs.
The latest versions can be found at https://github.com/wesleymarin . These versions contain parameters optimized for 2x300bp MiSeq reads.
-PINGgc can be used with any fastq reads and presents the opportunity to set your own threshold values (explained in the manual).
-PINGallele reads in the output from PINGgc, uses the presence/absence information to determine which genes to target for each sample, and incorporates the copy number information to determine the final allelic genotype.
PING allele combines information from alignment (SOS) and virtual probes (subsets of KFF) to call the final genotypes.
The full scale KFF can be used as backup for ambiguity resolution if needed, and remains unchanged from the version in folder 1.

If you use any of these please cite:

Norman PJ, Hollenbach JA, Nemat-Gorgani N, Marin WM, Norberg SJ, Ashouri E, Jayaraman J, Wroblewski EE, Trowsdale J, Rajalingam R, Oksenberg JR, Chiaroni J, Guethlein LA, Traherne JA, Ronaghi M, Parham P. Defining KIR and HLA Class I Genotypes at Highest Resolution via High-Throughput Sequencing. American Journal of Human Genetics. 99 (2), 375–391. 2016
