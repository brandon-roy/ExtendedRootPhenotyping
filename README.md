<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <link rel="stylesheet" href="styles.css">
    <!-- Optionally include a CSS framework (like Bootstrap) for easier responsiveness -->
  </head>
  <body>
    <!-- Header Section -->
    <header>
      <nav>
        <ul>
          <li><a href="#overview">Overview</a></li>
          <li><a href="#methods">Methods</a></li>
          <li><a href="#results">Results</a></li>
        </ul>
      </nav>
    </header>
      <h1>Mechanistic underpinnings of above and below-ground plant symptom development upon infection by grapevine fanleaf virus</h1>
      <h2>Repository inquiries should be directed to bgr36 'at' cornell.edu</h2>    
    <!-- Main Content -->
    <main>
      <!-- Overview Section -->
      <section id="overview">
        <h2>Overview</h2>
        <p>
          Grapevine fanleaf virus (GFLV) is a devastating pathogen of <em>Vitis</em> sp. worldwide. Root system architecture analysis as well as molecular host profiling efforts converging in this repository represent recent efforts to understand how GFLV ellicts symptoms in the model host <em>Nicotiana benthamiana</em>.
        </p>
      </section>
    <main>
      <!-- Methods Section -->
      <section id="methods">
        <h2>Methods</h2>
        <!-- Plant Growth -->
        <article>
          <h3>Plant Growth</h3>
          <p>
            Wildtype <em>Nicotiana benthamiana</em> seeds were sown in Cornell LM-3 soilless media for two to three weeks before transplant in a similar growth medium (4:1:1, LM-3:perlite:vermiculite), as previously reported. Seedlings were fertilized weekly with Scott’s Miracle Grow. Growing conditions were maintained at a 16:8 hour light:dark period at 25°C and 70% relative humidity.
          </p>
        </article>
        <!-- GFLV Strains and Plant Inoculation -->
        <article>
          <h3>GFLV Strains and Plant Inoculation</h3>
          <p>
            Infectious clones of GFLV RNA1 and RNA2 in <em>Agrobacterium tumefaciens</em> strain GV3301 were utilized to establish initial systemic infection in planta. Wildtype strains F13 (GenBank accession number NC003615) and GHu (JN391442), along with their respective mutant clones of RNA1 in combination with GFLV-GHu RNA2, were selected for this study. Inoculation was performed on plants at the four- to six-leaf stage using <em>A. tumefaciens</em>, and systemic infection was confirmed by double antibody sandwich enzyme-linked immunosorbent assay (DAS-ELISA) using specific antibodies (Bioreba, Reinach, Switzerland) at two weeks post-inoculation.
          </p>
          <p>
            A total of 14 GFLV strains were used, including wildtype GFLV strains GHu and F13, and 11 GFLV mutants. Three mutants carried protein 1E<sup>Pol*/Sd</sup> tagged with V5 at the C-terminus (GHu, F13, and GHu-1E<sub>K802G-S804N</sub>), while four mutants exhibited single (802nd or 804th) or double (802nd and 804th) amino acid swaps, or a 20-nucleotide swap (2404–2424). Additionally, lyophilized plant material infected with pepper ringspot virus (PepRSV; species <em>Tobravirus capsica</em>, genus <em>Tobravirus</em>, family <em>Virgaviridae</em>) strain CAM (NC003669) was mechanically transmitted into <em>N. benthamiana</em> and passaged across multiple experiments.
          </p>
        </article>
        <!-- Excavation of Root Systems and Analysis -->
        <article>
          <h3>Excavation of Root Systems and Root System Architecture Analysis</h3>
          <p>
            Whole crown root systems of <em>N. benthamiana</em> plants (infected with GFLV strains and PepRSV or uninoculated) were excavated by hand and processed according to our previously described methodology. Key root traits—including total number of root tips, average diameter (mm), number of branch points, and total volume (cubic mm)—were measured with minimal pre-processing and no normalization. PepRSV-infected plants served as a positive control. For GFLV-infected plants with replicates grown for varying durations, a z-score normalization of the RSA traits was performed relative to non-infected controls.
          </p>
        </article>
        <!-- Statistical Analyses and Visualization -->
        <article>
          <h3>Statistical Analyses and Visualization</h3>
          <p>
            All data was analyzed using R and RStudio. Statistical libraries included:
          </p>
          <ul>
            <li>corrplot (v0.92)</li>
            <li>lme4 (v1.1-35.5)</li>
            <li>FSA (v0.9.5)</li>
            <li>emmeans (v1.10.3)</li>
            <li>DESeq2 (v1.44.0)</li>
            <li>clusterProfiler (v4.12.2)</li>
            <li>enrichplot (v1.24.2)</li>
            <li>gprofiler2 (v0.2.3)</li>
            <li>WGCNA (v1.72-5)</li>
            <li>GSEABase (v1.66.0)</li>
          </ul>
          <p>
            Visualization was performed using ggplot2 (v3.5.1) and scatterplot3d (v0.3-44). All code and RMarkdown files are available on the associated GitHub page: <a href="https://github.com/brandon-roy/ExtendedRootPhenotyping">ExtendedRootPhenotyping</a>.
          </p>
        </article>
      </section>
      <!-- Results Section -->
      <section id="results">
        <h2>Results</h2>
        <!-- Root Phenotyping and Data Acquisition -->
        <article>
          <h3>Root System Architecture Traits are Differentially Modified by GFLV Species</h3>
          <p>
            A total of 342 scans of <em>N. benthamiana</em> roots were obtained on a flatbed scanner and 2,555 parsed images were subsequently segmented and analyzed using Rhizovision Explorer, as previously described. RSA traits were extracted per experimental replicate and saved in Microsoft Excel files (<a href="https://doi.org/10.5281/zenodo.14844388" target="_blank">DOI: 10.5281/zenodo.14844388</a>). Outlier experimental replicates (3 and 13) containing too few plants per treatment were excluded from further analyses. Additional outliers were detected using the interquartile range (IQR) exemption, excluding individuals more than 1.5 times the IQR from the mean. Manual exemption of eight additional samples resulted in a final matrix of 1,298 individual plant root systems.
          </p>
          <p>
            The complete dataset is represented by the files <code>RhizoAllCompiled.xlsx</code> (raw data) and <code>RhizoAllNormalized.xlsx</code> (normalized and adjusted data). An example of a processed <em>N. benthamiana</em> root system and its basic measurements is provided for reference (Fig. 3a).
          </p>
      <!-- File Directory & Documentation Section -->
      <section id="files">
        <h2>File Directory & Documentation</h2>
        <p>
          [A detailed explanation of the repository file structure will be provided here. This should include descriptions of scripts, data files, documentation, and other relevant materials.]
        </p>
      </section>
