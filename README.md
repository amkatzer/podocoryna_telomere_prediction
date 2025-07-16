# podocoryna_telomere_prediction

# Predict Motif using TeloSearchLR
https://github.com/gchchung/TeloSearchLR

```
#unzip fastq
gunzip m54313U_200131_153156.subreads.fastq.gz

#convert fastq to fasta
sed -n '1~4s/^@/>/p;2~4p' m54313U_200131_153156.subreads.fastq > podo_pacbio.subreads.fasta

#find the motif
TeloSearchLR.py -f podo_pacbio.subreads.fasta -k 4 -K 20 -m 1 -M 100 -n 6000

```

