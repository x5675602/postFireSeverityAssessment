
## Definitions of Train, Validation, and Test Datasets
The following provides unambiguous definitions of the three terms.
- Training Dataset: The sample of data used to fit the model.
- Validation Dataset: The sample of data used to provide an unbiased evaluation of a model fit on the training dataset while tuning model hyperparameters.
- Test Dataset: The sample of data used to provide an unbiased evaluation of a final model fit on the training dataset.
We make this concrete with a pseudocode sketch.
```
# split data
data = ...
train, validation, test = split(data)

# tune model hyperparameters
parameters = ...
for params in parameters:
	model = fit(train, params)
	skill = evaluate(model, validation)

# evaluate final model for comparison with other models
model = fit(train)
skill = evaluate(model, test)
```
## Use the k-fold cross-validation
Cross-validation is a resampling procedure used to evaluate machine learning models on a limited dataset. The procedure has a single parameter called ![](https://latex.codecogs.com/gif.latex?k) that refers to the number of groups that a given dataset is to be split into. As such, the procedure is oftern called ![](https://latex.codecogs.com/gif.latex?k)-fold cross-validation.
We can make it concrete with the pseudocode as follows:
```
# split data
data = ...
train, test = split(data)

# tune model hyperparameters
parameters = ...
k = ...
for params in parameters:
	skills = list()
	for i in k:
		fold_train, fold_val = cv_split(i, k, train)
		model = fit(fold_train, params)
		skill_estimate = evaluate(model, fold_val)
		skills.append(skill_estimate)
	skill = summarize(skills)

# evaluate final model for comparison with other models
model = fit(train)
skill = evaluate(model, test)
```

## stratified cross-validation
We can split a dataset randomly in such a way that maintains the same class distribution in each subset. This is called stratification or stratified sampling and the class label variable is used to control the sampling process.

For example, we can use a version of ![](https://latex.codecogs.com/gif.latex?k)-fold cross-validation that preserves the imbalanced class distribution in each fold. It is called stratified ![](https://latex.codecogs.com/gif.latex?k)-fold cross-validation and will enforce the class distribution in each split of the data to match the distribution in the complete training dataset.

We can make this concrete with an example.
```
# example of stratified k-fold cross-validation with an imbalanced dataset
from sklearn.datasets import make_classification
from sklearn.model_selection import StratifiedKFold
# generate 2 class dataset
X, y = make_classification(n_samples=1000, n_classes=2, weights=[0.99, 0.01], flip_y=0, random_state=1)
kfold = StratifiedKFold(n_splits=5, shuffle=True, random_state=1)
# enumerate the splits and summarize the distributions
for train_ix, test_ix in kfold.split(X, y):
	# select rows
	train_X, test_X = X[train_ix], X[test_ix]
	train_y, test_y = y[train_ix], y[test_ix]
	# summarize train and test composition
	train_0, train_1 = len(train_y[train_y==0]), len(train_y[train_y==1])
	test_0, test_1 = len(test_y[test_y==0]), len(test_y[test_y==1])
	print('>Train: 0=%d, 1=%d, Test: 0=%d, 1=%d' % (train_0, train_1, test_0, test_1))
```

# Dataset
The dataset for remote sensing with deep learning:
## PatternNet
PatternNet is a large-scale high-resolution remote sensing dataset collected for remote sensing image retrieval. There are 38 classes and each class has 800 images of size 256×256 pixels. The images in PatternNet are collected from Google Earth imagery or via the Google Map API for some US cities. The following table shows the classes and the corresponding spatial resolutions. The figure shows some example images from each class.


[website](https://sites.google.com/view/zhouwx/dataset)

## Others
[website](https://zhangbin0917.github.io/2018/06/12/%E9%81%A5%E6%84%9F%E6%95%B0%E6%8D%AE%E9%9B%86/)


# sourse (tensorflow)

[website](https://github.com/tavgreen/landuse_classification)




## different Types of Convolutions in Deep Learning
### Dilated Convolutions
Its parameter "dilation rate" defines a spacing between the values in a kernel. A 3x3 kernel with a dilation rate of 2 will have the same field of view as a 5x5 kernel, while only using 9 parameters. Imagine taking a 5x5 kernel and deleting every second column and row. It's as follows.
<figure>
  <img src="https://miro.medium.com/max/474/1*SVkgHoFoiMZkjy54zM_SUw.gif"  width="300" alt=".." title="Optional title" />
  <figcaption>2D convolution using a 3 kernel with a dilation rate of 2 and no padding</figcaption>
</figure>
This delivers a wider field of view at the same computational cost. Dilated convolutions are particularly popular in the field of real-time segmentation. Use them if you need a wide field of view and cannot afford multiple convolutions or larger kernels.

### Transposed Convolutions







