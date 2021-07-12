# NMA21-PenTango Project

## About:

We are interested in investigating the hierarchical structure of processing object categorization in the human brain. More specifically we hope to investigate the correlation between RDMs from Cichy et al.,2014 neuroimaging dataset with other attributes of the images they presented to subjects. 

## Hypotheses:


**Primary question: how do other features/attributes of these 92 images correlate with their RDMs in different brain regions(IT, V1)? We are interested in three other aspects of the images: **


1. Semantics  
    1. using pre-trained models to automatically label these images (AP, SE, PM)
    2. word2vec to calucalte semantic similarities of these images (HL,AP, AE)
2. Sentiment 
    1. new data collection and have subjects rate the sentiment of images: postivie to negative and novelty of the images (HL, SE)
    2. calculate the sentiment and novelty of these images in R. and export the final results in csv. file (HL)
    3. compute correlation/run prediction models 
3. Visual attributes (HL
   1. pixel analysis: edges, orientations, color
   2. compute a RDM of pixels for each image 
   3. regresss out the pixel similarities (fit a linear model of multiple RDMS on the target RDM)
                 
                   
                
**Decision point**

1. determine the scale for sentiment: gradient, what would be the numeric value assigned to each one? (VALENCE/AROUSAL); do we calcualte the average score, or the median, or sum? do we have each indivdual rate all 92 or a subset of it?  using 7 point or 5 point likert scale? 
2. 

## Goals to hit
Monday (July 12th) 
1. HL fix the bugs in the stimuli and look into literature how to calculate 
2. Analysis plans (: 
    1. how is the sentiment data processing/analysis (HL,SE)
4. PM & AP look into featrue extraction and identify featues/attributes that would be meaningful to implenet and calculate 
5. 

 
 
 
 
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

### Minutes document 

[Minutes meeting](https://docs.google.com/document/d/1GsBpHjl7nuiU9_HMjJqHEiLHDkE_u1DGq7H11_nFvM4/edit)

