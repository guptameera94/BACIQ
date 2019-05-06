# BACIQ
Bayesian Confidence Intervals for Multiplexed Proteomics Integrate Ion-Statistics with Peptide Quantification Concordance

This guide provides instructions on how to use the BACIQ software to compute uncertainty in the relative abundance between two channels for multi-peptide proteins. This uncertainty is calculated as the user specified percentage of confidence interval. The code can be slightly modified to output the entire probabilistic distribution of the true fraction of protein in one channel, which can be post processed further as desired by the user. 
System Requirements (Recommended):
a)	Unix/Linux Operating System
b)	Python - 2.7.3* 
	Numpy - 1.13.3* and above
	Pandas -  0.15.2 dev* and above
	Pystan -  2.17.1.0* and above
* This code was tested using the above-mentioned versions of the programs.
1.	How to use this program? 
a.	Copy the folder “BACIQ_v1.0.zip” to the desired directory. Extract the “BACIQ_v1.0.zip” and copy the extracted contents to the desired directory.
b.	Replace SampleInput.csv in the BACIQ_v1.0 folder with your Input CSV file. Please make sure your input CSV file has the same column names as the SampleInput.csv file you are replacing. Also, input file should be in .csv format.
c.	Open Terminal on your Unix System
d.	Navigate to the BACIQ_v1.0 directory path (using “cd /path” command)
e.	Use system command “ls” or “pwd” to ensure you are in the intended directory
f.	Enter the following commands in Terminal to run the program:
> sh run_linux.sh
g.	Keep entering the values as asked (Please ensure that the number of cores input is not more than the total proteins in your Input file)
	
2.	Locating and Interpreting the Output:
a.	Once the program finishes running, you can find then output at the following path: /yourpath/BACIQ_v1.0/Output/outFile_hist.csv (Please ignore other csv files in the Output folder except outFile_hist.csv)
b.	This outFile_hist.csv contains:
i.	Lower end of the confidence interval 
ii.	Median value 
iii.	Higher end of the confidence interval
iv.	Protein name as index 


For any help or questions, please e-mail us at meerag@princeton.edu

