# 4. Ressources
	
Cette section regroupe un ensemble de fichier ressources utiles pour le TP

--------------------------------------------------------------------------------
## Données brutes

### Genomic features

Pour ce TP nous utiliserons la version 6.59 du génome de *Drosophila melanogaster* dont les fichiers de séquence au format fasta sont accessibles sur le [site FTP de Flybase](https://s3ftp.flybase.org/genomes/Drosophila_melanogaster/dmel_r6.59_FB2024_04/fasta/index.html).
La liste ci-dessous peut-être importée dans votre serveur Galaxy. 

```
https://s3ftp.flybase.org/genomes/Drosophila_melanogaster/dmel_r6.59_FB2024_04/fasta/dmel-all-chromosome-r6.59.fasta.gz	dmel-r6.59-fasta
https://s3ftp.flybase.org/genomes/Drosophila_melanogaster/dmel_r6.59_FB2024_04/fasta/dmel-all-miRNA-r6.59.fasta.gz	dmel-r6.59-miRNA
https://s3ftp.flybase.org/genomes/Drosophila_melanogaster/dmel_r6.59_FB2024_04/fasta/dmel-all-miscRNA-r6.59.fasta.gz	dmel-r6.59-miscRNA
https://s3ftp.flybase.org/genomes/Drosophila_melanogaster/dmel_r6.59_FB2024_04/fasta/dmel-all-tRNA-r6.59.fasta.gz	dmel-r6.59-tRNA
https://s3ftp.flybase.org/genomes/Drosophila_melanogaster/dmel_r6.59_FB2024_04/gtf/dmel-all-r6.59.gtf.gz	dmel-r6.59-gtf
```

Séquence du transgène PLacZ
```
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_GenomicFeatures/download?path=%2F&files=PLacZ.fasta	PLacZ
```

### Petits ARN

La liste ci-dessous peut-être importée dans votre serveur Galaxy. Attention à ne sélectionner que les lignes correspondant aux deux échantillons sur lesquels vous allez travailler et qui sont indiqués dans le [tableau partagé dans l'onglet "petits ARN"](https://docs.google.com/spreadsheets/d/1ZGyRM1YU9N70Mh-RY5eBubg1dgWqcuvPiPh3lcr1ZeE/edit?gid=243437883).

```
GLKD
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_smallRNAseqData/download?path=%2F&files=ALBA28.fastqsanger.gz	GLKD-ALBA28
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_smallRNAseqData/download?path=%2F&files=ALBA29.fastqsanger.gz	GLKD-ALBA29
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_smallRNAseqData/download?path=%2F&files=ALBA30.fastqsanger.gz	GLKD-ALBA30

WT
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_smallRNAseqData/download?path=%2F&files=ALBA25.fastqsanger.gz	WT-ALBA25
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_smallRNAseqData/download?path=%2F&files=ALBA26.fastqsanger.gz	WT-ALBA26
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_smallRNAseqData/download?path=%2F&files=ALBA27.fastqsanger.gz	WT-ALBA27
```

### ARN

La liste ci-dessous peut-être importée dans votre serveur Galaxy. Attention à ne sélectionner que les lignes correspondant aux deux échantillons sur lesquels vous allez travailler et qui sont indiqués dans le [tableau partagé dans l'onglet "ARN"](https://docs.google.com/spreadsheets/d/1ZGyRM1YU9N70Mh-RY5eBubg1dgWqcuvPiPh3lcr1ZeE/edit?gid=418538100).

```
GLKD
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_RNAseqData/download?path=%2F&files=ALBA1.fastqsanger.gz	GLKD-ALBA1
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_RNAseqData/download?path=%2F&files=ALBA2.fastqsanger.gz	GLKD-ALBA2
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_RNAseqData/download?path=%2F&files=ALBA3.fastqsanger.gz	GLKD-ALBA3

WT
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_RNAseqData/download?path=%2F&files=ALBA4.fastqsanger.gz	WT-ALBA4
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_RNAseqData/download?path=%2F&files=ALBA5.fastqsanger.gz	WT-ALBA5
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_RNAseqData/download?path=%2F&files=ALBA6.fastqsanger.gz	WT-ALBA6
```

### Mesure des niveaux d'expression

La liste ci-dessous peut-être importée dans votre serveur Galaxy. Ces fichiers de comptage ont été obtenus après un alignement des données de RNA-seq sur le génome de la drosophile version r6.59 avec les paramètres de Bowtie -n 1 -m 1 -l 32.

```
GLKD
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_RNAseqData/download?path=%2F&files=featureCounts_GLKD_ALBA1.txt	GLKD-ALBA1-Counts
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_RNAseqData/download?path=%2F&files=featureCounts_GLKD_ALBA2.txt	GLKD-ALBA2-Counts
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_RNAseqData/download?path=%2F&files=featureCounts_GLKD_ALBA3.txt	GLKD-ALBA3-Counts

WT
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_RNAseqData/download?path=%2F&files=featureCounts_WT_ALBA4.txt	WT-ALBA4-Counts
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_RNAseqData/download?path=%2F&files=featureCounts_WT_ALBA5.txt	WT-ALBA5-Counts
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_RNAseqData/download?path=%2F&files=featureCounts_WT_ALBA6.txt	WT-ALBA6-Counts
```


--------------------------------------------------------------------------------
## Amorces de qPCR

Vous pouvez visualiser les amorces que vous avez utilisé lors de vos quantifications par qPCR dans IGV en téléchargeant le fichier [PCRprimers.gff](ressources/PCRprimers.gff).

--------------------------------------------------------------------------------
## ChIP-seq

L'occupation de H3K9me2, H3K9me3 et Rhino (Rhi) a été déterminée par immunoprécipitation de la chromatine suivie de séquençage (ChIP-seq) à partir d'ovaires WT et d'ovaires Kdm3 GLKD.
Les fichiers de couverture ci-dessous ont été obtenus à l'aide de l'outil [BamCompare](https://deeptools.readthedocs.io/en/develop/content/tools/bamCompare.html) (Deeptools Galaxy version 3.3.2.0.0)  avec une taille de bin de 100 pb et le calcul de la différence des lectures IP input en rpm.

```
H3K9me2
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_ChIPseq/download?path=%2F&files=ChIPseq_H3K9me2_Ctrl.bigwig
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_ChIPseq/download?path=%2F&files=ChIPseq_H3K9me2_Kdm3GLKD.bigwig

H3K9me3
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_ChIPseq/download?path=%2F&files=ChIPseq_H3K9me3_Ctrl.bigwig
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_ChIPseq/download?path=%2F&files=ChIPseq_H3K9me3_Kdm3GLKD.bigwig

Rhino
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_ChIPseq/download?path=%2F&files=ChIPseq_Rhino_Ctrl.bigwig
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_ChIPseq/download?path=%2F&files=ChIPseq_Rhino_Kdm3GLKD.bigwig
```

Les données originales sont accessibles dans l'archive tar bigwig "GSE203279_RAW.tar" sur l'[entrepôt de données GEO](https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE203279) en cliquant sur "custom".


--------------------------------------------------------------------------------
## Locus de piRNA

Séquences fasta des piRNA clusters et du transgene lacZ cible. La liste ci-dessous peut-être directement importée dans votre serveur Galaxy.

```
https://psilo.sorbonne-universite.fr/index.php/s/AG_Ressources/download?path=%2F&files=20A.fasta	20A
https://psilo.sorbonne-universite.fr/index.php/s/AG_Ressources/download?path=%2F&files=38C_1.fasta	38C_1
https://psilo.sorbonne-universite.fr/index.php/s/AG_Ressources/download?path=%2F&files=38C_2.fasta	38C_2
https://psilo.sorbonne-universite.fr/index.php/s/AG_Ressources/download?path=%2F&files=38C_3.fasta	38C_3
https://psilo.sorbonne-universite.fr/index.php/s/AG_Ressources/download?path=%2F&files=42AB.fasta	42AB
https://psilo.sorbonne-universite.fr/index.php/s/AG_Ressources/download?path=%2F&files=80F.fasta	80F
https://psilo.sorbonne-universite.fr/index.php/s/AG_Ressources/download?path=%2F&files=flamenco.fasta	Flamenco
https://psilo.sorbonne-universite.fr/index.php/s/AG_Ressources/download?path=%2F&files=PA92_TransgeneCible.fasta	PA92-TransgeneCible
```

Vous pouvez récupérer les coordonnées génomiques des piARN stockés sur la [piRNAdb](https://www.pirnadb.org/download/archive/gff_gtf) aux formats GTF et GFF.

Fichiers des séquences des 142 piRNA clusters

```
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_GenomicFeatures/download?path=%2F&files=Dmel_piRNA_clusters.fa.gz piRNA-clusters
```

--------------------------------------------------------------------------------
## piRNA uniques

Fichiers BAM obtenus après alignement des piRNA sur le génome de la drosophile pour obtenir des piRNA uniques. [Voir le tutoriel sur les petits ARN](/srna/#conserver-les-pirna-uniques)

```
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_smallRNAseqData/download?path=%2F&files=piRNAu_GLKD-ALBA28.bam	GLKD-ALBA28-piRNAu
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_smallRNAseqData/download?path=%2F&files=piRNAu_GLKD-ALBA29.bam	GLKD-ALBA29-piRNAu
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_smallRNAseqData/download?path=%2F&files=piRNAu_GLKD-ALBA30.bam	GLKD-ALBA30-piRNAu
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_smallRNAseqData/download?path=%2F&files=piRNAu_WT-ALBA25.bam	WT-ALBA25-piRNAu
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_smallRNAseqData/download?path=%2F&files=piRNAu_WT-ALBA26.bam	WT-ALBA26-piRNAu
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_smallRNAseqData/download?path=%2F&files=piRNAu_WT-ALBA27.bam	WT-ALBA27-piRNAu
```

--------------------------------------------------------------------------------
## miRNA modifié contre Kdm3

La séquences ci-dessous correspond au miRNA modifié contre Kdm3, si par exemple, vous voulez savoir ou le miRNA contre Kdm3 agit.

```
CAGTTCAGTTAGCGACGTTTA
TAAACGTCGCTAACTGAACTG
```

--------------------------------------------------------------------------------
## Lectures longues

Lectures au format fasta et contigs au format fasta suite au séquençage des ovaires de drosophiles avec le protocole Ultra Long Reds de Nanopore.

```
https://psilo.sorbonne-universite.fr/index.php/s/Kdm3_RNAseqData/download?path=%2F&files=UltraLongDrosoOvaires.tar	Ovaires-Nanopore

```