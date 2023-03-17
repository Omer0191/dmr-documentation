# Differential Methylated Region Analysis Tool Documentation

dmr_analysis is a software tool for differentially Methylated Regions analysis to rank significant DMRs.



[Home](index.md) | [DMR Block Analysis](dmr_analysis_block.md) | [Combine MultiChr4Rank](dmr_combine_multChrs4rank.md) | [Selected4plot](dmr_selected4plot.md) | [map2genome](dmr_map2genome.md) | [map2chromSegment](dmr_map2chromSegment.md) | [cal2genome_percent](dmr_cal2genome_percent.md) | [cal2chromSegment_percent](dmr_cal2chromSegment_percent.md) | [percent2plot](dmr_percent2plot.md) | [combine2geneAnnot](dmr_combine2geneAnnot.md) | [exportData](dmr_exportData.md)
## check_accuracy4cluster

### Required Parameters:
<ul>
  <li><code> in_cluster_out_path: </code> File path contains all clustered PWMs and uncertain
                        PWMs, such as '../data/out/sep8_run1</li>
<li><code> in_bpb3_ranking_path: </code> File path for bpb3 ranking results, such as ../data/ou
                        t/sep8_run1/test_67snps/foreground/test_seq/rankings/</li>
  <li><code> in_fileString4clustered_pwm: </code> File string or file folder/name used/contained for
                        clustered PWMs such as quality_assessed_out_seed3</li>

    
</ul>


### Optional Parameters:
<ul>
  <li><code>in_separateString4file : </code>string separation for joined new file name, default= ~ </li>
<li><code>in_topRank_cutoff : </code>Top rank cutof value for selected TFs for comparison,
                        default=10 </li>
  <li><code> in_fileString4uncertain_pwm: </code> File strin or file folder/name used/contained for
                        untertain PWMs such as uncertain_pwms</li>

    
</ul>  

[Home](index.md)
