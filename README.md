# StudyCareer

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


# Athen Summary:
A majority of the top rankings algrorithms relies on discriminative learning approach.

They are like 3 fold up:

1.Generating low-level image feature maps.

2.Generating discriminative classifier.

3.Transforming local features into classifier probabilites with MRF regularization to produce
the final set of segmenation.

