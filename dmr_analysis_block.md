
# Differential Methylated Region Analysis Tool 
## dmr_analysis Documentation

dmr_analysis is a software tool for differentially Methylated Regions analysis to rank significant DMRs.



[Home](index.md) | [DMR Block Analysis](dmr_analysis_block.md) | [Combine MultiChr4Rank](dmr_combine_multChrs4rank.md) | [Selected4plot](dmr_selected4plot.md) | [map2genome](dmr_map2genome.md) | [map2chromSegment](dmr_map2chromSegment.md) | [cal2genome_percent](dmr_cal2genome_percent.md) | [cal2chromSegment_percent](dmr_cal2chromSegment_percent.md) | [percent2plot](dmr_percent2plot.md) | [combine2geneAnnot](dmr_combine2geneAnnot.md) | [exportData](dmr_exportData.md)   


## DMR Block Analysis

Significant test of TF binding affinity changes between the foreground and the background calculations

## Required Paramters
<p>Required:</p>
<ul>
  <li><code>-in IN_FILE_FOLDER, --in_file_folder IN_FILE_FOLDER</code><br>input file folder for DNA methylation data such as WGBS. In this folder, all samples are provided in each chromosome folder with BED format where sample name is indicated by file name.</li>
  <li><code>-chr CHROMOSOME, --chromosome CHROMOSOME</code><br>select a chromosome for running dmr_analysis_block. For example, a chromosome (e.g., chrY) file folder under --in_file_folder that contains methylation data of samples in a chromosome (e.g., chrY)</li>
  <li><code>-gkey GROUP_KEY, --group_key GROUP_KEY</code><br>group key name, all bed files name contain this group_key will be combined together for dmr_analysis_block. In other words, only bed file name with this group_key will be selected in analysis. Usually, it is the same as the file folder (or chromosome name) in --chromosome.</li>
</ul>



## Optional Parameters

<ul>
  <li><code>output_file: </code> Output file name, default is - </li>
<li><code>p_value: </code> P-value cutoff for the Wilcoxon test, default=0.05</li>
  <li><code>max_rank: </code> Maximum rank of PWM to consider in the patient results, default=15 </li>
<li><code>exact_test: </code> Use exact Wilcoxon rank-sum test from R. R needs to be installed, default is False"</li>
  <li><code>pval_correction: </code> Whether adjust P-values by bonferroni correction, default is False"</li>
<li><code>: </code></li>
  
</ul>
