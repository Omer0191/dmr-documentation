
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
  <li><strong>-out , --out_file_folder</strong>: output file folder that store all results computed by dmr_analysis_block, default is out/</li>
  <li><strong>-ncol , --need_column</strong>: select a columan name from bed file that will be used by dmr_analysis_block. For example, there are only six columns allowed in a bed file and the column labels will be added automatically such as (Chrs, Starts, Ends, Methylation, Total_counts, Strand) after loading the data. Here, if we assumes the fourth column of the input bed file is the methylation level, then --need_column = Methylation, default = Methylation</li>
  <li><strong>-wtStr , --wildType_fileString</strong>: Use the first few character string of a file name to indicate it is a normal/wide type sample, or to labele this file/sample as wide type/normal condition. For example, if a file name under a chromosome folder of --in_file_folder starts with gcb_meht1_* is a wild type/control/normal sample, then --wildType_fileString is gcb. Default is gcb in the program</li>
  <li><strong>-dstart , --data_start_position</strong>: data start position, a start column position for input dataframe after methylation levels of multiple samples are combined into one file , default is 3 for chrY demo. Please note, it starts from 0 index at here. for example, in file chrY_MR_data4maxBlockDistanc*.gz, column labels are started from "chrs", "pos_start", "pos_end", "data1" "data2", ..., "datam", where the first 3 columns are chromosome positions, then the --data_start_position is 3. From the data_start_position to the data_end_position are all availble data columns of combined samples. For example, there are 12 samples in chrY demo, then th data_start_position=3 and data_end_position=15, which is the default setting in the program. Usually, these two parameters do not need to be changed if data size of input file is the same format as chrY_MR_data4maxBlockDistance*.gz</li>
  <li><strong>-dend , --data_end_position</strong>: data end position, an end column position for input dataframe after methylation levels of multiple samples are combined into one file, default is 15 for chrY demo. More information please refer to "--data_start_position". Please note that data_end_position - data_start_position = total number of input samples</li>
  <li><strong>-mxL , --maximum_adjacency_length</strong>: maximum length of adjancey CpG sites is allowed in a methylation region (MR) , default = 250</li>
  <li><strong>-minS , --minimum_block_size</strong>: minimum number of CpG sites is requested in a block/methylatoin region (MR), default = 5</li>
  <li><strong>-nDP , --number_of_data_points</strong>: the number of data points (or rows from a dataframe) will be considered in analysis, default=0 that means all data points (or the combined dataframe from all samples and CpG sites) will be used. if it sets =1000 then only the first 1000 rows of dataframe will be used in the analysis. This option is for debuging purforse when using a small sample for testing</li>
  <li><strong>-pC , --

