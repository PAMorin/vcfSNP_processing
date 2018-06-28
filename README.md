# vcfSNP_processing
visualization and re-calling of SNPs from vcf file

This set of R-scripts allows visualization and manipulation of SNP genotype data starting from a vcf file.
1) import a vcf file containing the genotype information from a set of bam files, e.g., from FREEBAYES. 
2) optional extraction of read depth by locus (output = violin plots)
3) optional visualization of depth by samples and loci (output = heatmap)
4) optional check for polymorphic and biallelic loci
5) extract the relevant data from the vcf file, format into a tidy dataframe and parse data.
6) Transform data into matrix of samples by loci, 2 columns per locus; write to .csv for analysis or data checking.
7) Generate similar matrix that also includes read counts for each allele. Write to .csv for data checking.
8) Generate plots of allele counts for each genotype, and at different scales for data checking. Output = pdf of 3 plots per locus, with guide lines for allelic ratios of 0.3 and 0.4 to check how well genotypes fit different calling schemes (e.g., minimum depth, allelic ratio)
9-10) Modify genotypes based on applying new minimum depth (minDP), allelic ratios, and excluded loci. (based on .csv file of parameters for each locus).
11) re-plot data as in 8 to visualize changes
12) optional re-generate genotype matrix for data checking (repeat 9-10 above until all loci are acceptable)
13) remove or re-call individual genotypes (needs work; very labor intensive)
14) transform data for export as sample by locus matrix (ready for import by strataG for various population analyses)
15) re-plot final data set for records
16) export data as one row per genotype (locus, position, sample_ID, genotype, allele1 depth, allele2 depth), for storage in database.
