# Differential Methylated Region Analysis Tool Documentation

dmr_analysis is a software tool for differentially Methylated Regions analysis to rank significant DMRs.



[Home](index.md) | [DMR Block Analysis](dmr_analysis_block.md) | [Combine MultiChr4Rank](dmr_combine_multChrs4rank.md) | [Selected4plot](dmr_selected4plot.md) | [map2genome](dmr_map2genome.md) | [map2chromSegment](dmr_map2chromSegment.md) | [cal2genome_percent](dmr_cal2genome_percent.md) | [cal2chromSegment_percent](dmr_cal2chromSegment_percent.md) | [percent2plot](dmr_percent2plot.md) | [combine2geneAnnot](dmr_combine2geneAnnot.md) | [exportData](dmr_exportData.md)

## bayespi_bar
<p>BayesPI-BAR delta-dbA ranking computation for TFs binding affinity changes affected by DNA mutations. This program computes rankings of given PWMs/clustered PWMs according to predicted effects of given sequence variants. This module needs following paramters. Details are given as under: </p>

### Optional Paramters:
<ul>
  <li><code>chemical_potentials: (str) </code>list of chemical potentials to use (e.g.,none -10 -13 -15 .. ), default is None </li>
  <li><code>reference_sequences: </code>FASTA file with reference sequences, default is None.</li>
  <li><code>alternate_sequences: </code>FASTA file with alternate sequences, default is None.</li>
  <li><code>pwm_folder: </code>Folder containing TF binding models in BayesPI .mlp format, default is None.</li>
  <li><code>iterations: (int) </code>Iteration count for background affinity distribution calculation, default =10000 </li>
  <li><code>p_value_cutoff: (float) </code>maximum dbA p-value to consider protein-DNA binding, default = 0.1.</li>
  <li><code>normalize_dba: </code>divide each dbA value by its standard deviation in the background sequence set, default is False,</li>
  <li><code>start_from_integration: </code>Do not compute delta-dbA values, assume they are already computed. Start from integration. default is False.</li>
  <li><code>reuse_output: </code>Do not recompute dbA values if they are already present in the result folder. This mode can handle partially computed results from an interrupted computation. Only the missing or corrupted output will be recomputed. default is False.</li>
  <li><code>integration: (str) </code> Method to integrate delta-dbA values obtained from different chemical potentials, default is pca. choices=["pca", "mean_ddba", "med_ddba"] </li>
  <li><code>result_folder: (str path) </code>Folder to put the results (will be erased), default=result"</li>
  <li><code>seed: (int) </code>Random seed for background affinity sampling. 0 means time-based seed, default =1 </li>
  <li><code>med_ddba_p_value: (float) </code> A threshold on \"median delta-dbA P-value\",default is None "</li>
  <li><code>max_rank: (int)</code> Maximum number of PWMs to write in each side of the rankings, default =10</li>
 
  </ul>
  
### Parallelization Paramters:
<ul>
  <li><code>use_cores: </code>number of cores to use on one machine </li>
<li><code>use_slurm: </code>use SLURM workload manager to distribute computations across nodes</li>
  <li><code>slurm_account: </code> SLURM account name</li>
<li><code>max_nodes: </code>maximum number of nodes to allocate when using SLURM</li>

</ul>
