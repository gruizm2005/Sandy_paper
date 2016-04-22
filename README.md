# Sandy_paper
Code for SANDY: a Matlab tool to estimate the sediment size distribution from a sieve analysis in CAGEO

This directory contains the Matlab script to compute the sediment size distribution of one or multiple sediment samples from a sieve analysis.

The tool has been developed for professionals involved in the study of sediment transport along coastal margins, estuaries, rivers and desert dunes. The algorithm uses several types of statistical analyses to obtain the main textural characteristics of the sediment sample (D50, mean, sorting, skewness and kurtosis). SANDY includes the method of moments (geometric, arithmetic and logarithmic approaches) and graphical methods (geometric, arithmetic and mixed approaches). In addition, it provides graphs of the sediment size distribution and its classification. The computational tool automatically exports all the graphs as enhanced metafile images and the final report is also exported as a plain text file. Parameters related to bed roughness such as Nikuradse and roughness length are also computed. Theoretical depositional environments are established by a discriminant function analysis. Using the uniformity coefficient the hydraulic conductivity of the sand as well as the porosity and void ratio of the sediment sample are obtained. The maximum relative density related to sand compaction is also computed. 

Reference:
Ruiz-Martinez, G., Rivillas-Ospina, D., Mariño-Tapia, I., Posada-Venegas, G. (2016). SANDY: a Matlab tool to estimate the sediment size distribution from a sieve analysis. Computers & Geosciences. DOI: 10.1016/j.cageo.2016.04.010.

Instructions:
1. SANDY requires two input parameters for computing the sediment size sediment: nominal sieve openings and cumulative mass of material retained on each sieve. This information is provided to the program through a plain text file (*.txt) arranged in two columns, which should be separated by a tab space and must be located in subfolder. This subfolder should be in the same folder where the SANDY script is. The data in the first column correspond to the nominal sieve openings (in mm) and the second column must refer to the cumulative mass of material retained on each sieve (in grams). The data must be sorted in descending order, following the nominal sieve openings.
2. In order to perform the sieve analysis of one or several samples of sand, it is necessary to create a folder; this is the main folder for the program. For each sediment sample that requires analysis, a subfolder of the sample should be created and the input file should be within this subfolder. The main folder should contain the SANDY program and one or more subfolders. When the program starts, the main folder is reviewed to determine whether one subfolder (“a sample”) should be analysed or several subfolders (multiple analyses).
3. To run SANDY, in Matlab Command Window should write the command:
run('Sandy.m')
