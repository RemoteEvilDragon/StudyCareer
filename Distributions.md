# StudyCareer

## BAUER, WIEST AND REYES (2012): SEGMENTATION OF BRAIN TUMOR IMAGES BASED ON INTEGRATED HIERARCHICAL
CLASSIFICATION AND REGULARIZATION

It's based on classification with integrated hierachical regularization.
Healthy tissues into CSF,WM,GM.Pathologic tissues into necrotic,active,non-enhancing and edema compartment.

Decision forest has the advantage of being able to handle multi-class problems and providing a probablistitc output.

1.The pre-processing phase(denoising,bias-field correction,rescaling,histogram matching),

2.decision forest classifier

3.Segmentation of brain tumor images based on integrated hierachical classification and regularization.

4.Model an energy minmization problem in a conditional random field formulation.

take attention here,we also compared the proposed approach to our previous method which used svms as a classifier instead of decision forests and which had a less sophiscated regularization.

It porints out that,they had come with some generalizaiton problems here.



### BUENDIA, TAYLOR, RYAN AND JOHN (2013): A grouping artificial immune network for segmentation of tumor images

Main method:Grouping Artificial Immune Network+

It's developed for fully automated MRI brain segmentation.

It defines the input pattern with any combination,voxel instensities from 2d or 3d blocks or shapes of varying sizes customized to each MRI sequence,
also include feature and textural patterns such as mean and variance of selected block sizes,slice or radial distance,co-occurrence matrices,among others.

Key point:the size of input pattern size,every byte inside the size denotes a modality.


### CORDIER, MENZE, DELINGETTE AND AYACHE (2013): PATCH-BASED SEGMENTATION OF BRAIN TISSUES

A database of multi-channel local patches is first built from a set of training pathological cases. Then, given a test case, 
similar multi-channel patches are retrieved in the patch database,along with the corresponding labels. Finally, a classification 
map for the test case is inferred as a combination of the retrieved labels during a label fusion step.

And there are quite some shortcomings of this method.



### DOYLE, VASSEUR, DOJAT AND FORBES (2013): FULLY AUTOMATIC BRAIN TUMOR SEGMENTATION FROM MULTIPLE
MR SEQUENCES USING HIDDEN MARKOV FIELDS AND VARIATIONAL EM

EM:**Expectation Maximization** framework.

This approach is fully automatic and requires no training,The model parameters are instead estimated using 
a variational EM algorithm with MRF constraints and the inclusion of a priori probabilistic maps to provide
a stable parameter trajectory during optimization.


### FESTA, PEREIRA, MARIZ, SOUSA AND SILVA (2013): AUTOMATIC BRAIN TUMOR SEGMENTATION OF MULTI-SEQUENCE MR IMAGES USING RANDOM
DECISION FORESTS

preprocessing phase
1.The first aims for the bias field correction with N41TK method.
2.The second normalizes the intensity scale of each sequence to a chosen reference by histogram matching using ITK.
3.all sequence from each subject were cropped to have the same brain volume.

Main method:Random decision forest,which is used based on several features extracted from the training data.
1)MR sequences intensities and the difference between each two sequences
2)neighborhood information with the mean, sum, median and intensity range of 3D cubic neighborhoods
3)context information as the difference between each voxel and the mean value of 3   3   3 mm cubes
4)texture information in all MR sequences, including edge density and local binary partition


### GEREMIA, MENZE AND AYACHE (2012): SPATIAL DECISION FORESTS FOR GLIOMA SEGMENTATION IN MULTI-CHANNEL
MR IMAGES
They present the **Spatially Adaptive Random Forests** to overcome these isssues in the context of volumetric medical images.
SARF buidls on three cutting-edge methods:
1.discriminative random forests
2.an efficient multi-scale 3D image representation
3.structured labeling


### GUO, SCHWARTZ AND ZHAO (2013): SEMI-AUTOMATIC SEGMENTATION OF MULTIMODAL BRAIN TUMOR USING
ACTIVE CONTOURS
this is a semi-automatic segmentation method for multimodal brain tumors,it's highly anchored on manuling part.
The user should draw a ROI roughly surrounding the tumor on a single image.
And then based on the edge-based active con-tours techiniques.


### HAMAMCI AND UNAL (2012): MULTIMODAL BRAIN TUMOR SEGMENTATION USING THE “TUMOR-CUT” METHOD
Main method:**Tumor-Cut**
It's an semi-automatic tumor segmentation method.


### MEIER, BAUER, SLOTBOOM, WIEST AND REYES (2013): APPEARANCE- AND CONTEXT-SENSITIVE FEATURES FOR BRAIN
TUMOR SEGMENTATION
Main method
Very important 3 parts:
1.a feature extraction yielding a voxel-wise feature vector
2.a classification step and a subsequent spatial regularization
3.preprocess the multimodal image data which encompasses noise-reduction,bias-field correction and intensity normalization.

which depends an forest classifier, posterior probobility output to define the predicted labels.

some unknow pairwise potential stuff here.

It has problem with discrimination between edema and non-enhancing tumor.


### MENZE, VAN LEEMPUT, LASHKARI, WEBER, AYACHE AND GOLLAND (2012): SEGMENTING GLIOMA IN MULTI-MODAL IMAGES USING A GENERATIVE MODEL FOR BRAIN LESION
SEGMENTATION
it's a generative model:The method represents a tumor appearance model for multi-dimensional sequences that provides channel-specific segmentation 
A discriminative classifier filters all tumor segments removing those that are most likely to be false positives,primarily
evaluating shape and location of the tumor regions returned from the generative model.


### MENZE, GEREMIA, AYACHE AND SZEKELY (2012): SEGMENTING GLIOMA IN MULTI-MODAL IMAGES USING A GENERATIVE-DISCRIMINATIVE MODEL FOR BRAIN LESION
SEGMENTATION
It returns probability maps for healthy tissues,and probability maps for the presences of characteristic hypo- or hyper- intense changes in each 
of the image volumes.
First,it extracts tumor related image features in a robust fashion .

Random forests as our discriminative model returns class probabilities,


### REZA AND IFTEKHARUDDIN(2013):Multi-class abnormal brain tissue segmentation using texture features.
extract feature and associating with random forest classifier

### RIKLIN RAVIV,VAN LEEMPUT AND MENZE(2012):MULTI-MODAL BRAIN TUMOR SEGMENTATION VIA LATENT ATLASES
It's based on a generative approach for patient-specific segmentation.With prior approximate tumor center and extent manually annoted.


### SHIN(2012):HYBRID CLUSTERING AND LOGISTIC REGRESSION FOR MULTI-MODAL BRAIN TUMOR SEGMENTATION
Neural network model was not used for the challenge however,because the improvement of classification accuracy was small relatively to the higher complexity compared to 
the logistic regression model.


### SUBBANNA, PRECUP, COLLINS AND ARBEL (2012): HIERARCHICAL PROBABILISTIC GABOR AND MRF
SEGMENTATION OF BRAIN TUMOURS IN MRI VOLUMES
The algorithm consists of two stages.
At the first stage,the goal is to coarsely segment tumors(and associated sub-classes)
from surrounding healthy tissues using texture features.
During training,specialized Gabor functions are developed to optimally separate tumors from surrounding healthy tissues based on
combined-space coefficients of tumors in multispectral brain MRIs.
A Bayesian classification framework is designed based on combined space Gabor decomposition.


###  TAYLOR, JOHN, BUENDIA AND RYAN (2013): MAP-REDUCE ENABLED HIDDEN MARKOV MODELS FOR HIGH THROUGHPUT
MULTIMODAL BRAIN TUMOR SEGMENTATION
We have developed a novel Map-Reduce enabled extension to hidden markov models to enable **high-throughput** training and segmentation of tumors
and edema in multimodal magnetic resonance images of the brain.
1.preprocessing part
2.Training the HMM,involves extracting a feature vector for each voxel in the source case.With map reducer produce new featur vector.
3.A final controller normalizes the probabilities in the HMM(initial ,transition,emission)and stores the HMM to a file.
Segmentation and Results:


### TUSTISON, WINTERMARK, DURST AND AVANTS (2013): ANTS AND ÁRBOLES
Main method:Regression forest

They are professional,use their own framework,has got very detailed steps to implement their method,and their methods cost a bulk of time to get the results.

### ZHAO AND CORSO (2012): BRAIN TUMOR SEGMENTATION WITH MRF ON SUPERVOXELS
Main method: MRF on supervoxels

### ZHAO, SARIKAYA AND CORSO (2013): AUTOMATIC BRAIN TUMOR SEGMENTATION WITH MRF ON SUPERVOXELS
Main method: MRF on supervoxels

### ZIKIC, GLOCKER, KONUKOGLU, SHOTTON, CRIMINISI, YE, DEMIRALP, THOMAS, DAS, JENA, AND PRICE (2012):
CONTEXT-SENSITIVE CLASSIFICATION FORESTS FOR SEGMENTATION OF BRAIN TUMOR TISSUES
This submission is based on a classsification forest,which is used such as to produce context-sensitivve predictions.





