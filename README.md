# lgrenier_project

##### My name is Laurence, but let's call me Lalou! 

##### I am a master student in psychology at Montreal University. I am particularly interested in social neurosciences, thereby working at the NeSC (Neuroscience en contextes sociaux)lab. My master project is a coordinate based meta-analysis on social hierarchy. Using the ALE algorithm, the main objective is to provide an overview of neural correlates underlying social hierarchy treatment. 

##### I really wish to contribute to science findings by adopting approaches that consider the current issues of reproductibility and social inclusion!   



<a href="https://github.com/lalou97">
   <img src="https://avatars.githubusercontent.com/u/87998890?v=4" width="100px;" alt=""/>
   <br /><sub><b>Laurence Grenier</b></sub>
</a>

# Project Definition 

## Doing machine learning with the results of neuroimaging studies to classify need and desire states


### Background
##### Overconsumption is associated with several environmental, social and individual problems (Lipschutz, 2001). One explanation suggested for overconsumption is that "we consume what we want belong what we need" (Stearns, 2006), (Juvénal et al., 2021). Some stimuli are sought for their survival value (food, water,...), while others are sought for their reward value (money, interesting objects,...). While motivation towards the former seems to increase, or even be triggered, by a state of deprivation, motivation towards the latter seems to increase as a function of the previously learned value of the stimulus, corresponding to the association between this stimulus and a reward. However, since a stimulus can be pursued for its *needing* value **AND** for its *wanting* value, for example some kind of food, or even some activities, we can wonder what are the similarities and the differences between those two conditions at a neural level? 

##### To answer this question, we previously made a coordinate-based meta-analysis with the ALE (Activation likelihood estimation) algorithm in order to find the consistent activations reported in the litterature for each of those conditions. Therefore, we identified regions more commonly reported in the experiments regarding *needs* than in the expriment of *wantings*, vice versa. 

#### ALE
##### The ALE approach is used to show the convergence between the regions reported in the litterature of a specified topic. For each of the selected studies, the coordinates of the significant voxels are taken (activation peaks). Then, the algorithm is making a gaussian matrice representing the spatial uncertainty, based on the sample of the corresponding study, around the activation peaks reported and thus making what is call a *MA map (main activation map)*.Therefore, each of the experiment has it own *MA map* where each voxels is associated with an activation probability (that increase in the closest to the peaks).Then, the union of the MA maps are taken and the algorithm is making permutations to identify which activations peaks are significantly reported across the experiments, thus representing the convergence of activations. 

##### The goal of the present project is to build a machine learning model which will make the distinction between the studies which focused on the *needs* and the studies focused on the *wantings* based on the MA maps generated by ALE algorithm during the firts step.   

##### The puposes of this project are : 
##### - Generating a machine learning model which will classify the *needings* and the *wantings* state based on studies included in the meta-analysis to train the model.
##### - Verify if the features used by the model to make the classification are similar as the regions identified in the meta-analysis.  
##### - Verify if a machine learning model based on significant activation peaks of different studies can be generalize single subject's datas. 




### Tools
##### - Python 
##### - Jupyter notebooks 
##### - nilearn 
##### - sklearn 
##### - github
##### - nimare 



### Data 
#### Activation peaks of included studies in the meta-analysis (training dataset): 
##### The machine learning model will be train with the activation peaks of the included studies of the coordinate-based meta-analysis. All of the contrasts selected represents either the *needs* or the *wantings*.

### *needs* : 38 
##### Contrasts of interest were meeting those criterions: 
##### - Perception of a food stimulus during a hunger state > perception of a stimulus during a satiety state.
##### - Perception of a food stimulus during a hunger state > perception of a non-food stimulus during a hunger state. 

### *wantings* : 33 
##### Contrasts of interest were meeting those criterions: 
##### - Perception of a cue announcing a reward (or a larger reward) > perception of a cue not announcing a reward (or a smaller reward).  

#### Datas from MA maps : maps generated with [nimare](https://nimare.readthedocs.io/en/latest/about.html)  

### Deliverables 
##### - ? Preprocessing pipeline for reducing the dimensionality of the activation peaks based on an atlas (ROI's from the ALE map) 
##### - Machine learning classification model for the *needs* and the *wantings* 
##### - Brain map representating the visualisation of the features used by the model to make the prediction 



# Results 




### References 
###### [L. Charbonnier, F. van Meer, A.M. Johnstone, D. Crabtree, W. Buosi, Y. Manios, O. Androutsos, A. Giannopoulou, M.A. Viergever, P.A.M. Smeets, Effects of hunger state on the brain responses to food cues across the life span,NeuroImage,Volume 171,2018,Pages 246-255,ISSN 1053-8119,https://doi.org/10.1016/j.neuroimage.2018.01.012.](https://neurovault.org/collections/3235/)

###### [Simon B. Eickhoff, Danilo Bzdok, Angela R. Laird, Florian Kurth, Peter T. Fox, Activation likelihood estimation meta-analysis revisited, NeuroImage, Volume 59, Issue 3, 2012,Pages 2349-2361,ISSN 1053-8119, https://doi.org/10.1016/j.neuroimage.2011.09.017.](https://www.sciencedirect.com/science/article/abs/pii/S1053811911010627?via%3Dihub)
