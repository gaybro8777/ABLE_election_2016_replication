### About
This repo contains replication data and visuals for a pending paper on online misinformation and bias during the 2016 presidential election. The data encompasses all news content distributed per specific news organizations and specific topics. This data is provided purely for research and verification purposes. Everything in this repo is subject to change, and really needs to be moved off github to a public store for large files.

### TLDR
Follow the reassembly steps below, then open ABLE_Results_1_18_18/GoogleLongTermSentimentT3T4Weekly.png. This is the long-term anti-conservative partisan bias of Google News over 6/2011-6/2017. There are histograms as well; these are the link counts per the topics listed in the file name, and show the source bias of Google News.
Poke around different news organization folders and view any file containing "_ppmi_smoothed_2wk_avg.png" but ignore any containing "expected" in the name. These files demonstrate the partisan variation in news reporting per these organizations using temporal sentiment analysis of their content. These plots show the strategic political communication patterns of different orgs, which are clearly evident.

### Reassembly
Github doesn't allow large files (>50mb or so) so the original g-zipped tarball was split into multiple "chunk_*" pieces using split. Hence each chunk_* file is a piece of a gzipped tar archive of the replication data, Replication.tar.gz.
To reassemble the gzipped tar archive Replication.tar.gz, use this command in a linux environment.
* cat chunk_* > Replication.tar.gz

Hash the file to verify it hasn't been modified:
* sha256sum Replication.tar.gz

Make sure it equals bc2c4e0ff9ff28a351f4f5694bfcac43551845bddcc3ed99be878e67bcabdba3
Unzip/untar the gzipped tar archive using:
* tar -xvzf Replication.tar.gz

All together:
1. cat chunk_* > Replication.tar.gz
2. sha256sum Replication.tar.gz  #must equal bc2c4...bcabdba3
3. tar -xvzf Replication.tar.gz

### Directory
1. ABLE_Results_1_18_18: ABLE-ITEM data and results for a variety of news orgs: BBC, RT, NPR, CNN, etc.
2. Harvard_Results_2_18_18: Replication content analyzed by ABLE-ITEM but sourced from the (Faris et al, 2017). This is not the full Harvard web news dataset, but rather the content items analyzed by ABLE-ITEM for specific topical queries.

### Files
* .png: Visuals are self-explanatory, and display various volume metrics or sentiment analyses. The file names describe what query topics and/or method were used to produce them if the text in the visuals don't specify.
* .py: These are replication files, for academic integrity and reproduction. These are the results of ABLE queries that were used as input for the analyses of the provided visuals. That is, for any of the visuals in this repo, I also stored the complete headline datasets that they were based upon.

### Citation
The Harvard data was derived from:
	
		Faris, Robert and Roberts, Hal and Etling, Bruce and Bourassa, Nikki and Zuckerman, Ethan and Benkler, Yochai, 
		Partisanship, Propaganda, and Disinformation: Online Media and the 2016 U.S. Presidential Election (August 2017).
		Berkman Klein Center Research Publication 2017-6. Available at SSRN: https://ssrn.com/abstract=3019414 

If you want to cite/use the Harvard data, use their data directly, which they've made available online, just search for the work cited above. The data posted in this repo is only a subset of specific topics hits, and is purely for verification.

Data in the ABLE_Results folder, was generated by me and can be cited separately. Other datasets per other topics can be generated for the orgs listed in the ABLE_Results folder, and can generate more, but it takes time and funds which I lack.

##### Except for the Harvard_Results_2_18_18 verification data, all contents of this repo are copyright Jesse Waite, 2016, 2017, 2018, including the methods portrayed.
