# StudyCareer


## Recommended guide line to analyse the 3 articles:
（1）背景知识，包括这个医学背景、问题、数据和挑战赛背景；（2）参赛各组的情况，他们用了什么方法，效果如何；（3）这两个最新的工作的效果，相同和差异，以及实现的总体思路是什么（这个暂时不需要太理解，可以等你了解了深度学习的一些背景情况后再补上）

1.The basic background of the brats chanllenge and 
it's medical background,
it's releated questions,
it's releated data source,

2.The resulting display.
How did people acheive in the challenge,what's their perfomance?
Which kind of approach are they using?

3.What about the other 2 method?
what's the common part and how do they differentiate?

## Kernel Confusing Concepts:
### Spatial regularity
>Most generative and discriminative segmentation approaches exploit **spatial regularity**,
often with extensions along the temporal dimension for longitudinal tasks.

### Conditional random fileds(CRF)
>Similarly,conditional random fields(CRF) help enforce --or prohibit-- the adjacency of wider 
spatial content of voxels.

### Markov random filed(MRF)
>Optimisation in an MRF probelme involves finding the **maximum of the joint probablity over the
graph**,usually with some of the variables given by some observed data,

### Map reduce 
# Athen Summary:
A majority of the top rankings algrorithms relies on discriminative learning approach.

They are like 3 fold up:

1.Generating low-level image feature maps.

2.Generating discriminative classifier.

3.Transforming local features into classifier probabilites with MRF regularization to produce
the final set of segmenation.



limitation of the current brats challenge:
1.Usually,it's very difficult to explain why a particular algorithm does well or not.

2.The selection of an appropriate overall evaluation metric that can be used to rank all competing algorithms,cause different metrics are sensitive to different types of segmentation error.


It is worth pointing out that the individual rater's manual segmentations of the training data are also available,so that groups that do not trust the consensus labels we provide, can generate their own training labels using a fusion method of their choice.




Some lessons learned.
It's recommended to generate multiple annotations for the test data,cause the larger the lesser inconsistent errors,At the same time,most algorithms will benefit from having larger training datasets,and their performances will be improved.

It may be useful to make unprocessed data available as well,and providing participants with maximally homogenized datasets,interpolated to a standard resolution and nomalized.Thus we could facilitate comparisions of the segmenation methods independently of preprocessing issues.


And Future work here.
Implementation of the latest advanced algorithms to the wider clinical research community.
Use longitudinal settings including both pre and post operative images.

Conclusion
It indicates that,brain tumor segmentation is difficult even for human raters,currently available algorithms can reach Dice scores of 0.8 for whole tumor segmentation.
Core region 0.7.Active region 0.6.No single method perfomed best for all tumor regions considered.
Fusing different segmenters boosts performance significantly,applying hierachical majority vote to fixed groups bring better perfomances.
This suggests that, in addition to pushing the limits of individual tumor segmentation algorithms, future gains (and ultimately clinical implementations) may also be obtained by investigating how to implement and fuse several different algorithms,either by majority vote or other fusing strategies.








