# Using ALE algorithm and machine learning to classify need and desire states

### Personal background

##### Hi! My name is Laurence! I've completed a bachelor's degree in cognitive neuroscience at Montreal University and I am currently a master student in psychology at Montreal University. I am particularly interested in social neurosciences, thereby working at the NeSC (Neuroscience en contextes sociaux)lab. My master project is a coordinate based meta-analysis on social hierarchy.

##### I really wish to contribute to scientific findings by adopting approaches that consider the current issues of reproductibility and social inclusion in neuroscience! I've decided to do brainhack school in order to familiarize myself with coding and neuroimaging datas. 



<a href="https://github.com/lalou97">
   <img src="https://avatars.githubusercontent.com/u/87998890?v=4" width="100px;" alt=""/>
   <br /><sub><b>Laurence Grenier</b></sub>
</a>

* * * 

# Project Definition 
* * * 

## Using ALE algorithm and machine learning to classify need and desire states


### Theoritical background
* * * 
##### Overconsumption is associated with several environmental, social and individual problems (Lipschutz, 2001). One explanation suggested for overconsumption is that "we consume what we want belong what we need" (Stearns, 2006), (Juvénal et al., 2021). Some stimuli are sought for their survival value (food, water,...), while others are sought for their reward value (money, interesting objects,...). While motivation towards the former seems to increase, or even be triggered, by a state of deprivation, motivation towards the latter seems to increase as a function of the previously learned value of the stimulus, corresponding to the association between this stimulus and a reward. However, since a stimulus can be pursued for its *needing* value **AND** for its *wanting* value, for example some kind of food, or even some activities, we can wonder what are the similarities and the differences between those two conditions at a neural level? 


##### To answer this question, we previously made a coordinate-based meta-analysis with the ALE (Activation likelihood estimation) algorithm in order to find the consistent activations reported in the litterature for each of those conditions. Therefore, we identified regions more commonly reported in the experiments regarding *needs* than in the expriment of *wantings*, vice versa. 

#### ALE
* * * 
##### The ALE approach is used to show the convergence between the regions reported in the litterature of a specified topic. For each of the selected studies, the coordinates of the significant voxels are taken (activation peaks). Then, the algorithm is making a gaussian matrice representing the spatial uncertainty, based on the sample of the corresponding study, around the activation peaks reported and thus making what is call a *MA map (main activation map)*.Therefore, each of the experiment has it own *MA map* where each voxels is associated with an activation probability (that increase in the closest to the peaks).Then, the union of the MA maps are taken and the algorithm is making permutations to identify which activations peaks are significantly reported across the experiments, thus representing the convergence of activations. 



### Objectives 
* * * 

##### The goal of the present project is to build a machine learning model which will make the distinction between the studies focusing on the *needs* and the studies focusing on the *wantings* based on the MA maps generated by ALE algorithm during the first step.   

##### The puposes of this project are : 
##### - Build a machine learning model which will classify the *needs* and the *wants* state based on studies included in the meta-analysis to train the model. 
##### - Retrieve the most contributing features in the machine learning classification model and interpret the coefficient's value in comparison of ALE meta-analysis results. 
##### - Familiarize myself with open science pratices, programming and machine learning.   


### Tools
* * * 
##### - Python 
##### - Jupyter notebooks 
##### - [nilearn](https://nilearn.github.io/index.html#)
##### - [scikit-learn](https://scikit-learn.org/stable/index.html) 
##### - github
##### - [nimare](https://nimare.readthedocs.io/en/latest/about.html)  


### Data 
* * * 

#### The dataset is composed of all the activation peaks of included studies in the meta-analysis: 

### *needs* : 38 studies
##### Contrasts of interest were meeting those criterions: 
##### - Perception of a food stimulus during a hunger state > perception of a stimulus during a satiety state.
##### - Perception of a food stimulus during a hunger state > perception of a non-food stimulus during a hunger state. 

### *wantings* : 33 studies 
##### Contrasts of interest were meeting those criterions: 
##### - Perception of a cue announcing a reward (or a larger reward) > perception of a cue not announcing a reward (or a smaller reward).  




### Deliverables 
* * * 
#### At the end of this project, I will have : 
##### - Markdown README.md for the description of the present project 
##### - Jupyter notebook including the code, and the brain images of interest 


# Results 
#### Datas from MA maps : maps generated with [nimare](https://nimare.readthedocs.io/en/latest/about.html)  
#### 



### References 
###### [L. Charbonnier, F. van Meer, A.M. Johnstone, D. Crabtree, W. Buosi, Y. Manios, O. Androutsos, A. Giannopoulou, M.A. Viergever, P.A.M. Smeets, Effects of hunger state on the brain responses to food cues across the life span,NeuroImage,Volume 171,2018,Pages 246-255,ISSN 1053-8119,https://doi.org/10.1016/j.neuroimage.2018.01.012.](https://neurovault.org/collections/3235/)

###### [Simon B. Eickhoff, Danilo Bzdok, Angela R. Laird, Florian Kurth, Peter T. Fox, Activation likelihood estimation meta-analysis revisited, NeuroImage, Volume 59, Issue 3, 2012,Pages 2349-2361,ISSN 1053-8119, https://doi.org/10.1016/j.neuroimage.2011.09.017.](https://www.sciencedirect.com/science/article/abs/pii/S1053811911010627?via%3Dihub)
