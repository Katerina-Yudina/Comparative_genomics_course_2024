**Introduction**

***Arabidopsis thaliana***, as a model organism in the field of plant
genetics and molecular biology, provides unique opportunities for
studying genetic variability and adaptation to various environmental
conditions. Due to its small genome size, short life cycle and extensive
genetic database, *Arabidopsis thaliana* is an ideal model for research
on the genetic mechanisms underlying plant adaptation and evolution.

The *Arabidopsis thaliana* ecotypes, such as Kar-1 and Columbia (Col-0),
represent genetically distinct populations adapted to specific
environmental conditions. Columbia (Col-0) is one of the most studied
ecotypes and is often used as a reference genome in genetic research.
This ecotype is characterized by early flowering, which is associated
with mutations in genes such as FRI (FRIGIDA) and FLC (FLOWERING LOCUS
C), which play a key role in the regulation of flowering. On the other
hand, the Kar-1 ecotype originating from another geographical region
(Kyrgyztan) may exhibit unique genetic features that ensure its
adaptation to specific environmental conditions.

Studying the genetic differences between Kar-1 and Columbia (Col-0) can
provide valuable information about adaptation mechanisms and identify
significant single nucleotide polymorphisms (SNPs).

The purpose of this work is to conduct a comparative analysis of the
genomes of the Kar-1 and Columbia (Col-0) ecotypes in order to identify
significant genetic differences and assess their biological
significance.

**Methods**

The Kar-1 ecotype genome assembly (GCA_036937505.1) was selected for
analysis, representing a population adapted to the conditions of
Kyrgyzstan. Columbia-0 ecotype (GCF_000001735.2) which has been studied
much better was used as a reference genome.

The BUSCO (Benchmarking Universal Single-Copy Orthologs) with the
Embryophyta database was used to evaluate the completeness and quality
of the assembly.

Alignment of the Kar-1 genome to the Columbia-0 reference genome was
performed using minimap2, and the bcftools was used to identify
single-nucleotide polymophysms. SNPs in genes FRI and FLC were selected.

The online tool VEP (Variant Effect Predictor) and the UniProt database
were used for functional annotation of SNPs. Protein structures were
predicted using AlphaFold. The obtained substitutions were filtered
according to their effects on protein structure and function (missense
mutations with SIFT values \< 0.05, which are labelled as deleterious,
were selected). After that, variants with changes in polarity or charge
of the amino acid were selected.

**Results**

1.  **BUSCO analysis**

During the analysis of the genomic assembly of *Arabidopsis thaliana*
(the Kar-1 ecotype genome assembly GCA_036937505.1) using the BUSCO
tool, the following results were obtained:

1.  Main results:

Complete BUSCO genes (C): 99.2%

Single copies (S): 98.3%

Duplicated copies (D): 0.9%

Fragmented BUSCO genes (F): 0.2%

Missing BUSCO genes (M): 0.6%

Total number of BUSCO groups (n): 1614

2.  Interpretation of the results:

High percentage of complete BUSCO genes (99.2%): This indicator
indicates the high completeness and quality of the genomic assembly.
Most of the conserved genes expected in the genome are present and fully
assembled. This indicates that the assembly contains almost all the
necessary functional elements, which makes it reliable for further
genetic and functional studies.

Low percentage of fragmented (0.2%) and missing (0.6%) BUSCO genes: The
low percentage of fragmented and missing genes confirms the high quality
of the assembly. This means that only a small part of the genes is
either partially assembled or missing, which minimizes the likelihood of
losing important genetic information.

Low percentage of duplicated genes (0.9%): A low percentage of
duplicated genes indicates that there are no significant duplication
problems in the genome, which is also a positive indicator.

This is important for the accuracy of functional annotation, as
duplicated genes can complicate the interpretation of data.

3.  Assembly statistics:

Number of scaffolds: 5

Number of contigs: 29

Total length: 134,343,331 bp

Percentage of skips: 0.002%

N50 scaffolds: 25 MB

N50 contigs: 10 MB

4.  Conclusion

BUSCO analysis results demonstrate that the genomic assembly of
*Arabidopsis thaliana* (GCA_036937505.1) It has high quality and
completeness. High N50 values and a low percentage of missions indicate
that the assembly consists of large, well-assembled fragments, which
also confirms its high quality. These results provide a solid basis for
further study of the genetic differences between *Arabidopsis thaliana*
ecotypes and their adaptation to different environmental conditions.

2.  **SNP\`s analysis**

From the annotation of the reference genome GCF_000001735.2 (downloaded
from NCBI), the FRI and FLC genes were isolated, of which we got 100 and
then we look for SNPs in the genes of interest - there are 1160 of them,
of which we will look for those SNPs that will affect the function of
the protein.

After VEP prediction and filtering with SIFT \< 0.05 (A SIFT value below
0.05 is usually interpreted as a high probability that the substitution
will not be tolerant and may disrupt the normal function of the protein.
Substitutions predicted as \"deleterious\" may be associated with
changes in protein structure, stability, or interactions with other
molecules) we got the number of missense mutations was 17, all of them
are presented in the list below:

 | Location          | Allele | Consequence      | IMPACT   | SYMBOL | Gene     | Feature_type | Feature     | BIOTYPE       | EXON | INTRON | HGVSc | HGVSp | cDNA_position | CDS_position | Protein_position | Amino_acids | Codons | Existing_variation | REF_ALLELE | UPLOADED_ALLELE | DISTANCE | STRAND | FLAGS | SYMBOL_SOURCE | HGNC_ID | SIFT                      | CLIN_SIG | SOMATIC | PHENO |
|-------------------|--------|------------------|----------|--------|----------|--------------|-------------|---------------|------|--------|-------|-------|---------------|--------------|------------------|-------------|--------|-------------------|------------|-----------------|----------|--------|-------|---------------|---------|--------------------------|----------|---------|-------|
| CP002684.1:27000454-27000454 | A      | missense_variant | MODERATE | CSTF64  | AT1G71800 | Transcript   | AT1G71800.1 | protein_coding | 5/11 | -      | -     | -     | 684           | 452          | 151              | G/D         | gGt/gAt | ENSVATH00137905   | G          | G/A             | -        | 1      | -     | EntrezGene    | -       | deleterious(0.01)        | -        | -       | -     |
| CP002684.1:29040967-29040967 | A      | missense_variant | MODERATE | EFS     | AT1G77300 | Transcript   | AT1G77300.2 | protein_coding | 17/17 | -      | -     | -     | 4610          | 4475         | 1492             | A/V         | gCa/gTa | ENSVATH00145915   | G          | G/A             | -        | -1     | -     | EntrezGene    | -       | deleterious_low_confidence(0.01) | -        | -       | -     |
| CP002684.1:29047745-29047745 | G      | missense_variant | MODERATE | EFS     | AT1G77300 | Transcript   | AT1G77300.1 | protein_coding | 2/18  | -      | -     | -     | 1353          | 1066         | 356              | G/R         | Ggt/Cgt | ENSVATH00145945   | C          | C/G             | -        | -1     | -     | EntrezGene    | -       | deleterious_low_confidence(0.02) | -        | -       | -     |
| CP002684.1:29047745-29047745 | G      | missense_variant | MODERATE | EFS     | AT1G77300 | Transcript   | AT1G77300.2 | protein_coding | 2/17  | -      | -     | -     | 1201          | 1066         | 356              | G/R         | Ggt/Cgt | ENSVATH00145945   | C          | C/G             | -        | -1     | -     | EntrezGene    | -       | deleterious_low_confidence(0.01) | -        | -       | -     |
| CP002685.1:6190124-6190124   | G      | missense_variant | MODERATE | TBL13   | AT2G14530 | Transcript   | AT2G14530.1 | protein_coding | 6/6   | -      | -     | -     | 1339          | 1226         | 409              | I/S         | aTc/aGc | ENSVATH00228698   | T          | T/G             | -        | 1      | -     | EntrezGene    | -       | deleterious(0)           | -        | -       | -     |
| CP002685.1:15819995-15819995 | C      | missense_variant | MODERATE | TBL15   | AT2G37720 | Transcript   | AT2G37720.1 | protein_coding | 3/3   | -      | -     | -     | 225           | 225          | 75               | L/F         | ttG/ttC | ENSVATH00263752   | G          | G/C             | -        | 1      | -     | EntrezGene    | -       | deleterious_low_confidence(0.03) | -        | -       | -     |
| CP002685.1:16840717-16840717 | C      | missense_variant | MODERATE | TBL33   | AT2G40320 | Transcript   | AT2G40320.1 | protein_coding | 2/6   | -      | -     | -     | 539           | 290          | 97               | L/P         | cTg/cCg | ENSVATH01972775   | T          | T/C             | -        | 1      | -     | EntrezGene    | -       | deleterious(0.01)        | -        | -       | -     |
| CP002686.1:500602-500602     | A      | missense_variant | MODERATE | TBL20   | AT3G02440 | Transcript   | AT3G02440.1 | protein_coding | 3/3   | -      | -     | -     | 1355          | 1355         | 452              | C/F         | tGt/tTt | ENSVATH00302265   | C          | C/A             | -        | -1     | -     | EntrezGene    | -       | deleterious(0)           | -        | -       | -     |
| CP002686.1:500602-500602     | A      | missense_variant | MODERATE | TBL20   | AT3G02440 | Transcript   | AT3G02440.2 | protein_coding | 3/3   | -      | -     | -     | 1383          | 1379         | 460              | C/F         | tGt/tTt | ENSVATH00302265   | C          | C/A             | -        | -1     | -     | EntrezGene    | -       | deleterious(0)           | -        | -       | -     |
| CP002686.1:1835566-1835566   | A      | missense_variant | MODERATE | TBL10   | AT3G06080 | Transcript   | AT3G06080.1 | protein_coding | 3/3   | -      | -     | -     | 1401          | 937          | 313              | T/S         | Acc/Tcc | ENSVATH00308697   | T          | T/A             | -        | -1     | -     | EntrezGene    | -       | deleterious(0.01)        | -        | -       | -     |
| CP002686.1:1835566-1835566   | A      | missense_variant | MODERATE | TBL10   | AT3G06080 | Transcript   | AT3G06080.2 | protein_coding | 3/4   | -      | -     | -     | 1401          | 937          | 313              | T/S         | Acc/Tcc | ENSVATH00308697   | T          | T/A             | -        | -1     | -     | EntrezGene    | -       | deleterious(0.02)        | -        | -       | -     |
| CP002686.1:3459029-3459029   | T      | missense_variant | MODERATE | TBL32   | AT3G11030 | Transcript   | AT3G11030.1 | protein_coding | 1/5   | -      | -     | -     | 352           | 272          | 91               | S/Y         | tCt/tAt | ENSVATH05807538   | G          | G/T             | -        | -1     | -     | EntrezGene    | -       | deleterious(0.04)        | -        | -       | -     |
| CP002687.1:269189-269189     | A      | missense_variant | MODERATE | FRI     | AT4G00650 | Transcript   | AT4G00650.1 | protein_coding | 1/3   | -      | -     | -     | 289           | 164          | 55               | F/Y         | tTt/tAt | ENSVATH10471557   | T          | T/A             | -        | 1      | -     | EntrezGene    | -       | deleterious(0.02)        | -        | -       | -     |
| CP002687.1:467605-467605     | A      | missense_variant | MODERATE | TBL26   | AT4G01080 | Transcript   | AT4G01080.1 | protein_coding | 2/3   | -      | -     | -     | 473           | 454          | 152              | L/F         | Ctt/Ttt | ENSVATH00450986   | G          | G/A             | -        | -1     | -     | EntrezGene    | -       | deleterious(0.01)        | -        | -       | -     |
| CP002687.1:6764891-6764891   | C      | missense_variant | MODERATE | TBL23   | AT4G11090 | Transcript   | AT4G11090.1 | protein_coding | 3/3   | -      | -     | -     | 1161          | 1053         | 351              | N/K         | aaT/aaG | ENSVATH00489181   | A          | A/C             | -        | -1     | -     | EntrezGene    | -       | deleterious(0.02)        | -        | -       | -     |
| CP002688.1:35463-35463       | G      | missense_variant | MODERATE | FRB1    | AT5G01100 | Transcript   | AT5G01100.1 | protein_coding | 7/8   | -      | -     | -     | 1633          | 1390         | 464              | I/L         | Atc/Ctc | ENSVATH06900697   | T          | T/G             | -        | -1     | -     | EntrezGene    | -       | deleterious(0.02)        | -        | -       | -     |
| CP002688.1:20975851-20975851 | A      | missense_variant | MODERATE | YLS7    | AT5G51640 | Transcript   | AT5G51640.1 | protein_coding | 4/4   | -      | -     | -     | 1202          | 1056         | 352              | K/N         | aaA/aaT | ENSVATH00727220   | T          | T/A             | -        | -1     | -     | EntrezGene    | -       | deleterious(0.03)        | -        | -       | -     |

### We filter the SNPs by charge:
| Location               | Allele | Consequence     | IMPACT  | SYMBOL | Gene     | Feature_type | Feature    | BIOTYPE        | EXON | INTRON | HGVSc | HGVSp | cDNA_position | CDS_position | Protein_position | Amino_acids | Codons | Existing_variation | REF_ALLELE | UPLOADED_ALLELE | DISTANCE | STRAND | FLAGS | SYMBOL_SOURCE | HGNC_ID | SIFT                  | CLIN_SIG | SOMATIC | PHENO |
|------------------------|--------|-----------------|---------|--------|----------|--------------|------------|----------------|------|--------|-------|-------|---------------|--------------|------------------|-------------|--------|--------------------|------------|-----------------|----------|--------|------|---------------|---------|-----------------------|----------|---------|-------|
| CP002684.1:27000454-27000454 | A      | missense_variant | MODERATE | CSTF64  | AT1G71800 | Transcript   | AT1G71800.1 | protein_coding | 5/11 | -      | -     | 68445 | 2151          | G/D         | gGt/gAt          | ENSVATH00137905 | GG/A   | -1                 | -          | EntrezGene      | deleterious(0.01) | -        | -       |
| CP002684.1:29047745-29047745 | G      | missense_variant | MODERATE | EFS     | AT1G77300 | Transcript   | AT1G77300.1 | protein_coding | 2/18 | -      | -     | 13531 | 066356        | G/R         | Ggt/Cgt          | ENSVATH00145945 | CC/G   | -1                 | -          | EntrezGene      | deleterious_low_confidence(0.02) | -        | -       |
| CP002684.1:29047745-29047745 | G      | missense_variant | MODERATE | EFS     | AT1G77300 | Transcript   | AT1G77300.2 | protein_coding | 2/17 | -      | -     | 12011 | 066356        | G/R         | Ggt/Cgt          | ENSVATH00145945 | CC/G   | -1                 | -          | EntrezGene      | deleterious_low_confidence(0.01) | -        | -       |
| CP002687.1:6764891-6764891   | C      | missense_variant | MODERATE | TBL23   | AT4G11090 | Transcript   | AT4G11090.1 | protein_coding | 3/3  | -      | -     | 11611 | 053351        | N/K         | aaT/aaG          | ENSVATH00489181 | AA/C   | -1                 | -          | EntrezGene      | deleterious(0.02) | -        | -       |
| CP002688.1:20975851-20975851 | A      | missense_variant | MODERATE | YLS7    | AT5G51640 | Transcript   | AT5G51640.1 | protein_coding | 4/4  | -      | -     | 12021 | 056352        | K/N         | aaA/aaT          | ENSVATH00727220 | TT/A   | -1                 | -          | EntrezGene      | deleterious(0.03) | -        | -       |
### And by polarity:

| Location               | Allele | Consequence     | IMPACT  | SYMBOL | Gene     | Feature_type | Feature    | BIOTYPE        | EXON | INTRON | HGVSc | HGVSp | cDNA_position | CDS_position | Protein_position | Amino_acids | Codons | Existing_variation | REF_ALLELE | UPLOADED_ALLELE | DISTANCE | STRAND | FLAGS | SYMBOL_SOURCE | HGNC_ID | SIFT                  | CLIN_SIG | SOMATIC | PHENO |
|------------------------|--------|-----------------|---------|--------|----------|--------------|------------|----------------|------|--------|-------|-------|---------------|--------------|------------------|-------------|--------|--------------------|------------|-----------------|----------|--------|------|---------------|---------|-----------------------|----------|---------|-------|
| CP002685.1:6190124-6190124 | G      | missense_variant | MODERATE | TBL13   | AT2G14530 | Transcript   | AT2G14530.1 | protein_coding | 6/6  | -      | -     | 13391 | 226409        | I/S         | aTc/aGc          | ENSVATH00228698 | TT/G   | -1                 | -          | EntrezGene      | deleterious(0) | -        | -       |
| CP002686.1:500602-500602   | A      | missense_variant | MODERATE | TBL20   | AT3G02440 | Transcript   | AT3G02440.1 | protein_coding | 3/3  | -      | -     | 13551 | 355452        | C/F         | tGt/tTt          | ENSVATH00302265 | CC/A   | -1                 | -          | EntrezGene      | deleterious(0) | -        | -       |
| CP002686.1:500602-500602   | A      | missense_variant | MODERATE | TBL20   | AT3G02440 | Transcript   | AT3G02440.2 | protein_coding | 3/3  | -      | -     | 13831 | 379460        | C/F         | tGt/tTt          | ENSVATH00302265 | CC/A   | -1                 | -          | EntrezGene      | deleterious(0) | -        | -       |
| CP002687.1:269189-269189   | A      | missense_variant | MODERATE | FRI     | AT4G00650 | Transcript   | AT4G00650.1 | protein_coding | 1/3  | -      | -     | 28916 | 455          | F/Y         | tTt/tAt          | ENSVATH10471557 | TT/A   | -1                 | -          | EntrezGene      | deleterious(0.02) | -        | -       |

The mutation for the FRI gene was found in the polarity change:
FRI (F/Y)
Substitution: Phenylalanine (F) for Tyrosine (Y)
Polarity: Both are aromatic, but tyrosine is more polar.
SIFT: deleterious(0.02)
Interpretation: Substitution may affect interaction with other molecules due to a change in polarity, SIFT indicates a possible negative effect.

3.  **Discussion**
We have identified the SNP that causes amino acid substitution in the FRI gene. This SNP is located in the coding region of the gene and leads to the replacement of phenylalanine with tyrosine.
Using SIFT allowed us to evaluate the possible effect of this substitution on protein function. A SIFT value of 0.02 indicates a potential negative impact, which makes this SNP interesting for further study. Genes such as FRI play a role in regulating flowering time in plants. Changes in their sequence can lead to significant phenotypic changes, which is important for adaptation and evolution.
After analyzing two protein configurations using AlphaFold (a protein variant from the reference and from the genome under study), there were no striking differences between the protein configurations (at least visually detectable). I put forward my hypothesis that this mutation did not significantly affect the phenotypic differences. But AlphaFold is not sure about its protein configuration either, because it gave me little confidence in its decision. I enclose the results of the configuration of this protein from the reference and the studied sequence, respectively:
![image](https://github.com/user-attachments/assets/34296f18-49ab-4a4f-882e-81eb82f6ebcd)
![image](https://github.com/user-attachments/assets/96741224-ee89-4ff8-899f-9b4a93a1e974)

