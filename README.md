# Pathtracker_Smartphone_Biosensor

## Overview:
This is an image processing project to help identify and count the pathogens in microfluidic chips which is part of the smartphone biosensor named ["Pathtracker"](https://nano.ece.illinois.edu/2017/11/20/lees-research-affects-next-gen-semiconductors/) for infectious disease detection. The algorithm would detect and count a very low number of target DNA copies in the channel. Imagine there are between 1-5 DNA molecules in the entire channel that match the sequence that will be amplified by the “primer” molecules.  Each of those DNA molecules acts as an initiation point, where the number of copies of the molecule will be exponentially increasing (1, 2, 4, 8, 16, 32 …. copies).  The copied DNA is fluorescent-emitting, so when their numbers are big enough, they will become visible in our image as a bright point.  As time moves forward, the initial bright point will expand outward for two reasons:  1.  The number of fluorescent molecules continues to grow, and 2. The molecules will diffuse away from their original locations.   

## Approach:
1. Establishing the regions of interest (ROI) within the image representing the six microfluidic compartments. 2. Using a sequence of images, recognizing the initiation of positive LAMP reactions, establishing the position of amplification loci, and counting the loci. 3. In the presence of previously-identified loci, recognizing the formation of new loci in subsequent images. 4. Track each loci as it expands its footprint and quantify metrics that include loci area, loci “front” velocity, total area percentage occupied by loci, and total area percentage still “free”. 5. Establish a threshold at which loci can no longer be digitally quantified, and transition to conventional “average intensity” method and calculation of amplification threshold time.


## Related Papers:
https://www.ncbi.nlm.nih.gov/pubmed/28819973


## Acknowledgement:
I would like to thank Prof. Brian Cunningham for his mentorship and guidance on this research project. 
