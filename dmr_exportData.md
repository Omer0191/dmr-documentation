# Differential Methylated Region Analysis Tool Documentation

dmr_analysis is a software tool for differentially Methylated Regions analysis to rank significant DMRs.



[Home](index.md) | [DMR Block Analysis](dmr_analysis_block.md) | [Combine MultiChr4Rank](dmr_combine_multChrs4rank.md) | [Selected4plot](dmr_selected4plot.md) | [map2genome](dmr_map2genome.md) | [map2chromSegment](dmr_map2chromSegment.md) | [cal2genome_percent](dmr_cal2genome_percent.md) | [cal2chromSegment_percent](dmr_cal2chromSegment_percent.md) | [percent2plot](dmr_percent2plot.md) | [combine2geneAnnot](dmr_combine2geneAnnot.md) | [exportData](dmr_exportData.md) 

## highly_mutated_blocks
<p>This program finds which blocks produced by mussd.py have significantly more mutations than would be expected if all mutations were uniformly distributed across regions of interest. </p>

### Required Parameters
<ul>

  <li><code>blocks_folder: </code> The folder containing mussd.py output</li>

</ul>

### Optional Paramters:
<ul>
  <li><code>output_file: </code> Output file name. Each line will contain an ID of a significantly "
                                                "mutated block, default is - </li>
<li><code>p_value: </code>P-value cutoff for the binomial test, default=0.05</li>
  <li><code>correctPval: </code> Whether adjust P-values by bonferroni correction, default is True, if use False then this option will be turned off for correction </li>

</ul>

