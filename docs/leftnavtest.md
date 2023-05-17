<!DOCTYPE html>
<html>
<head>
  <title>Differential Methylated Region Analysis Tool - Documentation</title>
  <style>
    body {
      display: flex;
    }

    nav {
      width: 20%;
      background-color: #f1f1f1;
      padding: 20px;
    }

    main {
      flex: 1;
      padding: 20px;
    }

    nav ul {
      list-style-type: none;
      padding: 0;
      margin: 0;
    }

    nav li {
      margin-bottom: 10px;
    }

    nav a {
      text-decoration: none;
      color: #333;
    }

    nav a:hover {
      color: #000;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <nav>
    <ul>
      <li><a href="index.md">Home</a></li>
      <li><a href="dmr_analysis_block.md">DMR Block Analysis</a></li>
      <li><a href="dmr_combine_multChrs4rank.md">Combine MultiChr4Rank</a></li>
      <li><a href="dmr_selected4plot.md">Selected4plot</a></li>
      <li><a href="dmr_map2genome.md">map2genome</a></li>
      <li><a href="dmr_map2chromSegment.md">map2chromSegment</a></li>
      <li><a href="dmr_cal2genome_percent.md">cal2genome_percent</a></li>
      <li><a href="dmr_cal2chromSegment_percent.md">cal2chromSegment_percent</a></li>
      <li><a href="dmr_percent2plot.md">percent2plot</a></li>
      <li><a href="dmr_combine2geneAnnot.md">combine2geneAnnot</a></li>
      <li><a href="dmr_exportData.md">exportData</a></li>
      <li><a href="dmr_gene_annotation.md">gene annotation</a></li>
    </ul>
  </nav>
  <main>
    <h1>Differential Methylated Region Analysis Tool</h1>
    <h2>check_accuracy4cluster Documentation</h2>
    <p>check_accuracy4cluster is a significant test of TF binding affinity changes between the foreground and the background calculations.</p>

    <h3>Required Parameters</h3>
    <ul>
      <li><code>background_folder</code>: Folder containing the computed background model produced by background_affinity_changes.py</li>
      <li><code>foreground_folder</code>: Folder containing the computed delta-dba values for patient data produced by bayespi_bar.py</li>
    </ul>

    <h3>Optional Parameters</h3>
    <ul>
      <li><code>output_file</code>: Output file name, default is -</li>
      <li><code>p_value</code>: P-value cutoff for the Wilcoxon test, default=0.05</li>
      <li><code>max_rank</code>: Maximum rank of PWM to consider in the patient results, default=15</li>
      <li><code>exact_test</code>: Use exact Wilcoxon rank-sum test from R. R needs to be installed, default is False</li>
    </ul>
  </main>
</body>
</
