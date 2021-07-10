# NMA21-PenTango Project

## About:

We are interested in investigating the hierarchical structure of processing object categorization in the human brain. More specifically we hope to investigate the correlation between RDMs from Cichy et al.,2014 neuroimaging dataset with other attributes of the images they presented to subjects. 

## Question:

Primary question: how do other features/attributes of the images correlate with these RDMs in different brain regions(IT, V1)? 
    * semantics 
        * using pre-trained models to automatically label these images (AP, SE, PM)
        * word2vec to calucalte semantic similarities of these images (HL,AP, AE)
    * sentiment 
        * new data collection and have subjects rate the sentiment of images: postivie to negative
    * visual attributes (HL,
        * pixel analysis: edges, orientations, color 
        * regresss out the pixel similarities (fit a linear model of multiple RDMS on the target RDM)
                * fit a RDM of pixels 
                -
     
        

     

##Decision point 

1. determine the scale for sentiment: gradient, what would be the numeric value assigned to each one? (VALENCE/AROUSAL) 


##Action Items:
1. Nic
1. dec


## Abstract:


We are interested in investigating the hierarchical structure of processing object categorization in the human brain. Cichy and colleagues (2014) have demonstrated how the brain processes objects over time: whereas all individual images are discriminated by earlier visual areas, superordinate, ordinate and subordinate category images emerged later. 
However, the prior study trained the dataset with a supervised machine learning classifier using a predefined category for a given image as the outcome variable, it remains elusive to what extent humans really use this structure of ordinates and subordinate categories to classify images. Therefore, first, we hope to deploy some unsupervised methods to find new ways of clustering images based on neuronal responses (in the format of RMD from MEG) and to understand the structure of these high-dimensional categories. Second, we hope to understand how human brain processes different information to categorize a given image more parsimoniously by looking at the relationships between objective attribute similarity (lines, edges, colors of the images), representational dissimilarity/perceptual similarity in the infero temporal and early visual region, and conceptual similarities of image labels (computed through word embedding model). 



## Methodology






## The team
<table>
<tr>
    <td align="center"><a href="https://github.com/anproulx"><img src="https://github.com/anproulx.png" width="100px;" alt=""/><br /><sub><b>Andréanne Proulx</b></sub></a><br /><a href="https://github.com/physiopy/phys2bids/commits?author=viacovella" title="Code">💻</a></td>
</tr>
<tr>
    <td align="center"><a href="https://github.com/hanxiaolu-5"><img src="https://github.com/hanxiaolu-5.png" width="100px;" alt=""/><br /><sub><b>Hanxiao Lu</b></sub></a><br /><a href="https://github.com/physiopy/phys2bids/commits?author=viacovella" title="Code">💻</a></td>
</tr>
<tr>
    <td align="center"><a href="https://github.com/svanengelen"><img src="https://github.com/svanengelen.png" width="100px;" alt=""/><br /><sub><b>Sydney Van Engelen</b></sub></a><br /><a href="https://github.com/physiopy/phys2bids/commits?author=viacovella" title="Code">💻</a></td>
</tr>
<tr>
    <td align="center"><a href="https://github.com/pablo-mere-hidalgo"><img src="https://github.com/pablo-mere-hidalgo.png" width="100px;" alt=""/><br /><sub><b>Pablo Mere Hidalgo</b></sub></a><br /><a href="https://github.com/physiopy/phys2bids/commits?author=viacovella" title="Code">💻</a></td>
</tr>
<tr>
    <td align="center"><a href="https://github.com/Alfaxad"><img src="https://github.com/Alfaxad.png" width="100px;" alt=""/><br /><sub><b>Alfaxad Eyembe</b></sub></a><br /><a href="https://github.com/physiopy/phys2bids/commits?author=viacovella" title="Code">💻</a></td>
</tr>
</table>
