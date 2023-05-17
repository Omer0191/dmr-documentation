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
    <h2>dmr_analysis Documentation</h2>
    <p>dmr_analysis is a software tool for differentially Methylated Regions analysis to rank significant DMRs.</p>

    <h3>DMR Block Analysis</h3>
    <p>Significant test of TF binding affinity changes between the foreground and the background calculations</p>

    <h3>Required Parameters</h3>
    <p>Required:</p>
    <ul>
      <li><code>-in IN_FILE_FOLDER, --in_file_folder IN_FILE_FOLDER</code>: input file folder for DNA methylation data such as WGBS. In this folder, all samples are provided in each chromosome folder with BED format where sample name is indicated by file name.</li>
      <li><code>-chr CHROMOSOME, --chromosome CHROMOSOME</code>: select a chromosome for running dmr_analysis_block. For example, a chromosome (e.g., chrY) file folder under --in_file_folder that contains methylation data of samples in a chromosome (e.g., chrY)</li>
      <li><code>-gkey GROUP_KEY, --group_key GROUP_KEY</code>: group key name, all bed files name contain this group_key will be combined together for dmr_analysis_block. In other words, only bed file name with this group_key will be selected in analysis. Usually, it is the same as the file folder (or chromosome name) in --chromosome.</li>
    </ul>

    <h3>Optional Parameters</h3>
    <ul>
      <li><code>-out, --out_file_folder</code>: output file folder that stores all results computed by dmr_analysis_block, default is out/</li>
      <li><code>-ncol, --need_column</code>: select a column name from bed file that will be used by dmr_analysis_block. For example, there are only six columns allowed in a bed file and the column labels will be added automatically such as (Chrs, Starts, Ends, Methylation, Total_counts, Strand) after loading the data. Here, if we assume the fourth column of the input bed file is the methylation level, then --need_column = Methylation, default = Methylation</li>
      <!-- ... continue with the rest of the optional parameters ... -->
    </ul>
  </main>
</body>
</html>
