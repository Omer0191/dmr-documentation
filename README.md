# dmr_analysis

usage:  dmr_analysis <task> [<args>]

Tasks available for using:
    dmr_analysis_block 	Predict Differentially Methylated Region (DMR) from genome-wide methylation regions such as by using WGBS or other similar techniques        
    dmr_combine_multChrs4rank 	Combine predicted DMRs/MRs from multiple chromosomes then rank the DMRs by using logistic regresssion model
    dmr_selected4plot 	Plot figure and export raw/smoothed methylation data for selected DMR or MR
    dmr_map2genome 	Map all DMR/MRs to reference genome
    dmr_map2chromSegment 	Map all DMR/MRs to chromation segments generated from 6 human cell lines
    dmr_cal2genome_percent 	Calculate percentage of DMRs intersected with predefined genomic regions such as TSS, TES, 5dist et al.
    dmr_cal2chromSegment_percent 	Calculate percentage of DMRs intersected with chromatin segments generated from 6 human celles 
    dmr_percent2plot 	Plot percentage of DMRs in predefined genomic or chromatin segment regions
    dmr_combine2geneAnnot 	Combine annotations from both predefined genomic regions and chromatin segments (This function is slow and requests both genome and chromatin segment results available)
    dmr_exportData	Plot and export data for DMRs/MRs located in specific regions (e.g., DMRs/MRs intersected with mutation block or enhancer regions)

DMR-Analysis: A Differentially Methylated Region Analysis Tool

positional arguments:
  task        Pipeline task to run

optional arguments:
  -h, --help  show this help message and exit
