# NMA21-PenTango Project


## Project Title.
![project_title](https://user-images.githubusercontent.com/68440833/126869814-b59e956a-741b-488b-8fec-61fda12516d9.png)


## About:

This project was developed by **PenTango** team from **Oval Bongos** pod during **Neuromatch Academy 2021: Computational-Neuroscience** summer school.We decided to work with data from Cichy et al. 2014 [1]. The data consist of fMRI responses from early visual cortex (EVC) and inferior temporal (IT) cortex and MEG responses at different timepoints in the form of representational dissimilarity matrices (RDMs) to 92 images. These images belong to different categories as shown in the Figure below.We were interested in investigating the hierarchical structure of processing object categorization in the human brain. More specifically we investigated the correlation between RDMs from Cichy et al.,2014 neuroimaging dataset with other attributes of the images they presented to subjects. 


![intro](https://user-images.githubusercontent.com/68440833/126870166-adb705a2-66bd-4d8e-82f7-fba6cce16184.png)




![dataset_des](https://user-images.githubusercontent.com/68440833/126869810-2c91cf0f-68d2-4bca-8eb5-0ece28f31a25.png)



![prior](https://user-images.githubusercontent.com/68440833/126869797-b97c18d9-f061-43c5-82c1-1efae270b00e.png)



## Hypotheses:

After examing the given data, we formulated hypothesis with a primary question which was **How do other features/attributes of these 92 images correlate with their RDMs in different brain regions(IT(Inferotemporal), V1)? **


We  were also  interested in three other aspects of the images as, shown below:

1. Semantics  
    1. using pre-trained models to automatically label these images.
    2. word2vec to calucalte semantic similarities of these images.
2. Sentiment 
    1. new data collection and have subjects rate the sentiment of images: postivie to negative and novelty of the images.
    2. calculate the sentiment and novelty of these images in R. and export the final results in csv file.
    3. compute correlation/run prediction models.
3. Visual attributes (HL)
   1. pixel analysis: edges, orientations, color.
   2. compute a RDM of pixels for each image .
   3. regresss out the pixel similarities (fit a linear model of multiple RDMS on the target RDM).
                
 
 
 
## Abstract:


How do humans and other primates perceive daily objects of various features and categorize these seemingly intuitive and effortless mental representations? Prior literature has mainly focused on investigating this question by applying supervised machine learning classifiers to neural responses recorded from tasks in which humans (and monkeys) were asked to view images of isolated objects (Kriegeskorte et al., 2008; Kiani et al., 2007). These classifiers have demonstrated that neurons in the inferior temporal (IT) cortex distinguish objects through a system of hierarchical categories that is consistent with the experimenter's predefined structure (superordinate, ordinate, subordinate). However, it remains elusive whether the spatio-temporal patterns of BOLD activations are entirely a reflection of these hierarchical categories or if they can also be accounted for by other attributes of these images such as low level image features, sentiment, and familiarity. Therefore, we investigated whether other attributes may have confounded the prior results by computing RDMs of other features of these images, such as lower-level visual attributes, sentiment and familiarity and use them as predictors of the neural RDMs computed in IT regions (fMRI). Behavioural data was collected from voluntary participants (n = 33) with a survey deployed online by evaluating the sentiment and familiarity of the 92 images in the original study. Low level features of the images were extracted using a pre-trained convolutional network model (AlexNet) to compute activation maps for each image. Simple regression models were built in conjunction with a variance partitioning analysis to parsimoniously examine the contribution of new attributes of interest to the neural responses in the IT region, and test whether the initial hierarchical structure of categories remains true after regressing out the influence of these possible confounds.


## Methodology

As mentioned above, we were interested in the question *What other features of images actually contribute to the neural representation of categorization in the human brain? We will do this by investigating whether other attributes may have confounded the prior results by computing representational dissimilarity matrix of other features of these images, such as lower/high-level deep neural network attributes, sentiment and familiarity and use them as predictors of the neural RDMs computed in IT regions (fMRI).*
In addition, behavioural data was collected from voluntary participants (n = 33) with a survey deployed online by evaluating the sentiment and familiarity of the 92 images in the original study.
Then, we followed the approach outlined below to answer this question.

![approach](https://user-images.githubusercontent.com/68440833/126869892-6089249c-e55e-4940-afd2-6f401ced1426.png)



## Results.

We obtained results for visual-attributes, Sentiment-analysis, correlation & Multiple linear regression. The sesults are as outlined below:

1. **Results - Visual attributes.**
Here we present the RDMs computed for each feature of interest: 
   1. This slide shows the RDMs for each convolutional layers computed from the output of AlexNet
   2. The first layer represent lower level attributes such as edges, color and orientation, whereas later layers represent more complex features. 

![archi](https://user-images.githubusercontent.com/68440833/126869865-42bc7de8-d1b2-47cc-b4d6-a263f3b5b8f2.png)


2. **Results-Sentiments.**

After viewing the image for 500ms,people were asked: how do you feel immediately about this image? People rate the sentiment from strongly negative to strongly positive on a 5-point likert scale. 
This is the RDM computed from the data collected for sentiment. As we observe no clear delineation of this heatmap, sentiment response does not give good insight in distinguishing categories of these 92 images.


![res1](https://user-images.githubusercontent.com/68440833/126869905-829a45a9-f1aa-4dc7-82a8-68667438ce9a.png)


3. **Results - Familiarity.**

People were also asked: how likely it is for you to see the content of this image in real life? People also rate the likelihood on a 5-point likert scale from rarely to certainly. 
In this heatmap, we find such a delineation between categories of images, suggesting that familiarity might be an interesting dimension of these images.

![res2](https://user-images.githubusercontent.com/68440833/126869919-ec2c304e-97ee-416a-be66-063c6f93cf6a.png)


4. **Results - Correlation.**

Then we computed the correlation matrix for all the RDMs of interest, including the RDM of neural representation in IT, EVC regions. And here is what we found out:

   1. Sentiment and familiarity RDMs are not in strong correlation with neural representation RDMs
   2.  However low to mid level RDMs from CNN layers do correlate well with the fMRI RDMs  
   3.  Low level layer 2 correlates strongly for both IT and EVC regions.
   4.  In addition, we also observe a medium-size correlation between RDM_layer 8 and familiarity.
 
 
![res3](https://user-images.githubusercontent.com/68440833/126869930-dfbc0417-8bb6-4696-ab23-2c01152ca901.png)

Below there is different figure that highlights the correlation of feature RDMs with neural representation in regions of interest. 


![res4](https://user-images.githubusercontent.com/68440833/126869936-e76175f8-2c0d-421a-a60e-05d7ccc7e7b7.png)



5. **Results - Multiple linear Regression.**

We selected a subset of features to compute multiple linear regression to predict the fMRI RDMs in each brain region and found that our features can explain up to more than 50% of the variance. We also ran a variance partitioning analysis to show the unique contribution of each feature and the variance they commonly shared to explain.

![res5](https://user-images.githubusercontent.com/68440833/126869943-21732fe9-55b8-4566-b3b9-d350c8da8456.png)


## Discussion and Future Direction.

![res6](https://user-images.githubusercontent.com/68440833/126869948-761e57ec-7239-4211-bd79-7a475eafecb3.png)


## Conclusion and Future Direction.


![res7](https://user-images.githubusercontent.com/68440833/126876274-8577fad0-24e2-44da-9463-e329ce8df6c3.png)


## References.

1. Cichy, R., Khosla, A., Pantazis, D. et al. Comparison of deep neural networks to spatio-temporal cortical dynamics of human visual object recognition reveals hierarchical correspondence. Sci Rep 6, 27755 (2016). https://doi.org/10.1038/srep27755
2. Groen II, Greene MR, Baldassano C, Fei-Fei L, Beck DM, Baker CI. Distinct contributions of functional and deep neural network features to representational similarity of scenes in human brain and behavior. Elife. 2018 Mar 7;7:e32962. doi: 10.7554/eLife.32962. PMID: 29513219; PMCID: PMC5860866.
3. Representational similarity analysis – connecting the branches of systems neuroscience. Kriegeskorte et al. Front. Syst. Neurosci., 2008
Resolving human object recognition in space and time. Cichy et al. Nature Neuroscience 2014.
4. Krizhevsky, A., Sutskever, I., & Hinton, G. E. (2012). Imagenet classification with deep convolutional neural networks. Advances in neural information processing systems (pp. 1097–1105).



## The team.



![TA](https://user-images.githubusercontent.com/68440833/126876473-647b1355-043d-489c-85e6-8eaa7a55c285.jpeg)

We could have never accomplish this, without the amazing dedication and support from our beloved Pod TA, **Akanksha Gupta(picture above)**, who is *RA at Institut de Neurosciences des Systèmes (INS)*, our beloved project TA **Nicholas Blauch(picture below)**, who is a *Ph.D. candidate in Neural Computation Carnegie Mellon*, our beloved mentor **Vy Vo(picture below)**, who is a *AI/ML Research Scientist at Intel Labs*, and last but not the least our **Oval Bongos** pod members(pictures below) and the team as a whole. Special thanks to **Neuromatch Academy** for giving us this special opportunity and moments that lasts a lifetime, it was a really wonderful and amazing experience.



![penteam](https://user-images.githubusercontent.com/68440833/126876337-1e34e6f1-80be-4ca9-b427-6a8829783583.png)



**Oval bongos**(below).

![Oval_Bongos](https://user-images.githubusercontent.com/68440833/126877019-bab06a98-4e44-4d1a-9268-34c78f201dbc.png)
















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















