# Final Project
## Comparison of peptide-MHC-I Binding Prediction Models

Author: Vishal Lashkari

Purpose: to use descriptive and inferential statistics to compare the predictions made by well-established models (NetMHCpan) against predictions made by models with newer architectures (HLApollo).

Here, human chromosome 21 is tiled into 9mers. Duplicates are removed. Some duplicate peptides were retained if the flanking regions are distinct as this is an additional input to HLApollo.
Data from UniProt: https://www.uniprot.org/proteomes/UP000005640

Predictions on the tiled chromosome were made with:

NetMHCpan 4.1 https://services.healthtech.dtu.dk/services/NetMHCpan-4.1/

HLApollo https://github.com/Genentech/HLApollo

Predictions were made only for HLA-A*02:01, the most common allele in the United States.

The relevant metric is the percentile rank which both models output. A stronger binder will have a lower value for its percentile rank.

NetMHCpan predictions were made only on the 9mer sequence in question.

HLApollo predictions were made by additionally supplying the 10 aa flanking the 9mer on either side in the native protein sequence. 
