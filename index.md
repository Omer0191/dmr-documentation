
 
<img align="center" src="https://user-images.githubusercontent.com/79196757/180248926-efd6e216-0683-4549-99f0-e6783224a2c7.png">
<img align="right" src="https://user-images.githubusercontent.com/79196757/180251608-da859f67-aa58-49e8-bea8-a0258be93635.png"><img align="left" src="https://user-images.githubusercontent.com/79196757/180251606-8e257ad0-86d5-4cb7-b549-ed5e5c0aa9eb.jpg">  





# Differential Methylated Region Analysis Tool 
## dmr_analysis Documentation

dmr_analysis is a software tool for differentially Methylated Regions analysis to rank significant DMRs.




## Modules:
[Home](index.md) | [DMR Block Analysis](dmr_analysis_block.md) | [Combine MultiChr4Rank](dmr_combine_multChrs4rank.md) | [Selected4plot](dmr_selected4plot.md) | [map2genome](dmr_map2genome.md) | [map2chromSegment](dmr_map2chromSegment.md) | [cal2genome_percent](dmr_cal2genome_percent.md) | [cal2chromSegment_percent](dmr_cal2chromSegment_percent.md) | [percent2plot](dmr_percent2plot.md) | [combine2geneAnnot](dmr_combine2geneAnnot.md) | [exportData](dmr_exportData.md)   
## How to start:
<div class="container-fluid abstract_des">
dmr_analysis is written in python. It can be installed and accessed from command line and is avalible for both linux and mac operating systems. The package can be downloaded <strong> here </strong> .

Prior to installing the package, dependencies must be fulfilled. List of dependencies is as follows:
<ul>
	<li>bedtools</li>
	<li>setuptools</li>
	<li>itertools</li>
	<li>pandas</li>
	<li>numpy</li>
	<li>argparse</li>
	<li>os</li>
	<li>shutil</li>
	<li>multiprocessing</li>
	<li>matplotlib</li>
	<li>seaborn</li>
	<li>datetime</li>
	<li>scipy</li>
	<li>tempfile</li>
	<li>time</li>

</ul>
It is advised to install dependencies using miniconda.
Package contains a file requirments.txt which can be used for automatic installation of dependencies from conda or pip.
To install the package, go to the dmr_analysis directory and type: python setup.py install
For more details, follow the readme file in the package.
</div>
	
	
## Installation:
<div class="container-fluid abstract_des">
		
<p>You can download and install the package by follwing steps:
	</p>
<pre class="bash"><code class="hljs"><span class="hljs-comment"> tar -zxf dmr_analysis.tgz</span>
<span class="hljs-comment"> cd dmr_analysis</span>
<span class="hljs-comment"> python setup.py install</span></code></pre>
	</div>	
	
## Contents of the package:
<div class="container-fluid abstract_des">
		
<p>The package folder will contain following:
	</p>
<ul>
	<li><code>final_demo</code> : Contains functions scripts.</li>
	<li><code>dmr_analysis</code> : Contains python soruce code of pipeline.</li>
	<li><code>readme.txt</code> : Instructions about usage of package.</li>
	<li><code>requirments.txt</code> :  List of requirements. Can be used for automatic installation from miniconda or pip.</li>
	<li><code>setup.py</code>: Setup file for package.</li>
	<li><code>final_demo_data</code>: Contains data in and out for the secondary functions.</li>


</ul>	
	
</div>

	
## Pipeline Tasks:
	
<p>The pipeline consists of follwoing tasks. To run a task, type dmr_analysis task args. To see what are the options for each task of the pipeline, please run: dmr_analysis -h </p>

<ul>
<li><code>dmr_analysis_block </code> : Predict Differentially Methylated Region (DMR) from genome-wide methylation regions such as by using WGBS or other similar techniques.</li>
	<li><code>dmr_combine_multChrs4rank </code> : Combine predicted DMRs/MRs from multiple chromosomes then rank the DMRs by using logistic regresssion model. </li>
	<li><code>dmr_selected4plot</code> : Plot figure and export raw/smoothed methylation data for selected DMR or MR.</li>
	<li><code>dmr_map2genome</code> : Map all DMR/MRs to reference genome.</li>
	<li><code>dmr_map2chromSegment</code> : Map all DMR/MRs to chromation segments generated from 6 human cell lines.</li>
	<li><code>dmr_cal2genome_percent</code> : Calculate percentage of DMRs intersected with predefined genomic regions such as TSS, TES, 5dist et al.</li>
	<li><code>dmr_cal2chromSegment_percent</code> :Calculate percentage of DMRs intersected with chromatin segments generated from 6 human celles.</li>
	<li><code>dmr_percent2plot</code> : Plot percentage of DMRs in predefined genomic or chromatin segment regions.</li>
	<li><code>dmr_combine2geneAnnot</code> : Combine annotations from both predefined genomic regions and chromatin segments (This function is slow and requests both genome and chromatin segment results available).</li>
	<li><code>dmr_exportData</code>:  Plot and export data for DMRs/MRs located in specific regions (e.g., DMRs/MRs intersected with mutation block or enhancer regions).</li>
	
</ul>
	
## Demos

[Demo1: FL](demo1.md)
[Demo2: HAP](demo2.md)
[Demo3: RAT](demo3.md)
	
         	
           			
         	
         		
         		
         	
Having trouble with package? Contact us @ junbai.wang@medisin.uio.no and we will be glad to help you.
You can also go to <a href="https://bpb3.github.io/bpb3/">This link (To be updated)</a> for more information on demos and installation.
