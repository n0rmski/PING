Use this to look for any specific sequence on your fastq files.
It is the KFF engine -- virtual SSOP.
put fastq in /Seqs folder
The probes supplied in the /probez folder are designed for resolving some common ambiguities and confirming some tricky alleles

The batch will count the ocurrences of that exact sequence string in each sample.
As general rule for 70k KIR-extracted 2x300 reads, and 50-60 bp probe use an aggregate of 10 hits per probe [(probe + probeRC *1.fastq) + (probe + probeRC *2.fastq)] as positive -but this may need more judgement for borderline cases
The output is allcounts.oot

You can add your own probes to /probez folder -but don't forget the reverse comp
(hint --use the ungapped KIR gene fasta file to check specificity)
