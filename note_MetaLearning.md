


课题还是需要解决实际问题。我关心：（1）小样本问题；（2）样本不匀衡问题；(3) 有已有灾后评定模型的基础上，对新数据的处理问题;（4）已有经验模型的迁移问题。

## Remote Sensing
A general definition of Remote Sensing is “the science and technology by which the characteristics of objects of interest can be identified, measured or analyzed the characteristics without direct contact” (JARS, 1993).
NASA Training webinars:
- [Fundamentals of Remote Sensing](https://appliedsciences.nasa.gov/join-mission/training/english/fundamentals-remote-sensing)
Remote sensing is obtaining information about an object from a distance. A photograph is a very common form of remote sensing. There are different ways to collect data, and different sensors are used depending on the application. What information do you need? How much detail? How frequently do you need the data? Satellites carry instruments or sensors that measure electromagnetic radiation coming from the Earth-atmosphere system. The energy Earth receives from the sun is called electromagnetic radiation. 

<p align="center"><img align="center" width="500" src="./notePic/electromagnetic spectrum.png"></p>
Fig. electromagnetic spectrum.

That radiation is reflected, absorbed, and emitted by the Earth's atmosphere or surface, as shown by the figure. Satellite sensors are calibrated to detect various wavelengths along the electromagnetic spectrum, often including visible light. Different materials reflect and absorb different wavelengths of electromagnetic radiation. Because of this, you can look at the reflected wavelengths detected by a sensor and determine the type of material it reflected off of. This is known as a spectral signature. In the graph below, compare the relationship between percent reflectance and the reflective wavelengths of different components of the Earth’s surface. 

<p align="center"><img align="center" width="500" src="./notePic/the spectral signatures of some materials.png"></p>
Fig. the spectral signatures of some material in Earth.

Healthy vegetation absorbs blue and red wavelengths, but reflects green and infrared. Since we can't see infrared radiation, we see healthy vegetation as green.

Longer visible wavelengths (green and red) and near-IR radiation are absorbed more by water than shorter visible wavelengths (blue) – so water usually looks blue or blue-green. The water will appear brighter if there is sediment in the upper layers of the water.

By using the way the electromagnetic radiation spectrum interacts with the atmosphere, satellites are able to provide information about the atmosphere’s composition. This includes the presence of particulates that may contribute to air pollution, clouds, and precipitation.

Solar radiation passes through the atmosphere and hits a target surface such as a forest, water, or built up area. Different materials reflect, emit, and absorb at different wavelengths.

Polar Orbiting provides global coverage and its measurement frequency can vary from 1 measurement per day to 1 per month, but Non-Polar Orbiting does not provide global coverage and its measurement frequency can vary every few hours to a few weeks.

There are two types of ways remote sensing data is collected: passive and active remote sensing. Passive remote sensing: depends on changes in gravity or reflected and emitted radiation from the Earth. For instance, the Grace Follow-On satellites measure changes in the Earth’s gravity. Landsat, the MODIS sensor onboard Terra & Aqua, and Aqua’s AIRS sensor, all depend on changes in the reflected and emitted radiation from the Earth for data. The typical passive remote sensors are Landsat, MODIS (Terra/Aqua), AIRS (Aqua), GRACE Active remote sensing: an instrument sends beams of radiation and measures its return, such as Radar and LIDAR.

Spatial resolution is the geographical area covered by a pixel in a satellite's image. Generally, the higher the spatial resolution, the less area is covered by a single pixel.

Temporal resolution is the revisit period of a satellite. It is the time it takes for a satellite to image the same area at the same viewing angle a second time. It depends on the satellite and sensor capabilities, the overlap of the satellite's path, and latitude of the satellite. Some satellites have greater temporal resolution because: (1) they are able to maneuver their sensors; (2) they have increasing overlap at higher latitudes.

Spectral resolution describes the ability of a sensor to detect fine wavelength intervals. Instruments detect different ranges of wavelengths along the electromagnetic spectrum, referred to as bands. The narrower a wavelength range is, the finer the spectral resolution is.  More and finer spectral channels enable remote sensing of different parts of the Earth’s surface.

Radiometric resolution describes a sensor's ability to discriminate differences in energy (or radiance). The better the radiometric resolution, the more sensitive the sensor is to small differences in energy. It is determined by multiple factors, chief among these are the saturation radiance - the "brightest" thing detectors can measure - and how the radiance measurements are quantized (turned into a digital bit stream).

Satellite data is available at different stages (or levels) of processing, going from raw data collected from the satellite to polished products that visualize information. NASA takes the data from satellites and processes it to make it more usable for a broad array of applications. There is a set of terminology that NASA uses to refer to the levels of processing it conducts: Level 0 & 1 is the raw instrument data that may be time-referenced. It is the most difficult to use. Level 2 is Level 1 data that has been converted into a geophysical quantity through a computer algorithm (known as retrieval). This data is geo-referenced and calibrated. Level 3 is Level 2 data that has been mapped on a uniform space-time grid and quality controlled. Level 4  is Level 3 data that has been combined with models or other instrument data.

Remote Sensing Advantages: (1) Provides information where there are no ground-based measurements; (2) Provides globally consistent observations; (3) Can provide direction on where to place ground-based sensors; (4) Provides continuous monitoring of our planet.
Remote Sensing Disadvantages: (1) It is very difficult to obtain high spectral, spatial, temporal, and radiometric resolution all at the same time; (2) Large amounts of data in a variety of formats can lead to more time and processing; (3) Applying satellite data may require additional processing, visualization, and other tools.






- [Land Cover Classification with Satellite Imagery](https://appliedsciences.nasa.gov/join-mission/training/english/land-cover-classification-satellite-imagery)
Objects: Understand how to access and download Landsat imagery; Become familiar with Landsat bands and color combinations; earn the basic steps for conducting a supervised land cover classification by analyzing differences in spectral signatures with the SCP plugin within QGIS software.
- [Remote Sensing for Monitoring Land Degradation and Sustainable Cities SDGs](https://appliedsciences.nasa.gov/join-mission/training/advanced-webinar-remote-sensing-monitoring-land-degradation-and-sustainable)
- [Understanding Phenology with Remote Sensing](https://appliedsciences.nasa.gov/join-mission/training/english/understanding-phenology-remote-sensing)
- [etc.](https://appliedsciences.nasa.gov/join-mission/training)

## Few-Shot Learning
few-shot learning比普通机器学习的不同之处是它可以利用前验知识。
Few-Shot Learning (FSL) is a type of machine learning problems (specified by emperience E, task T and performance measure P), where E contains only a limited number of examples with supervised information for the target T[[Wang, 2019](#Wang2019)].
FSL is applied in the following three typical scenarios:
- Acting as a test bed for learning like human. 
- Learning for rare cases. 
- Reducing data gathering effort and computational cost. 

Some algorithms related to Few-Shot Learning:
- Weakly supervised learning [163] learns from experience E containing only weak supervision (such as incomplete, inexact, inaccurate or noisy supervised information). 
- Imbalanced learning learns from experience E with a skewed distribution for y. 
- Transfer learning transfers knowledge from the source domain/task, where training data is abundant, to the target domain/task, where training data is scarce. 
- Meta-learning improves the performance measure P of the new task T by the provided data set and the metaknowledge extracted across tasks by a meta-learner [[Hochreiter, 2001](#Hochreiter2001)].

A survey post about Meta-Learning:[Meta-Learning: Learning to Learn Fast](https://lilianweng.github.io/lil-log/2018/11/30/meta-learning.html)

Long Short Term Memory networks (LSTMs) are a special kind of RNN, capable of learning long-term dependencies. LSTMs were introduced by Hochreiter & Schmidhuber [[Hochreiter, 1997](#Hochreiter1997)]. Refer to the post by colah: [Understanding LSTM Networks](https://colah.github.io/posts/2015-08-Understanding-LSTMs/). Bidirectional LSTMs are an extension of traditional LSTMs that can improve model performance on sequence classification problems, providing additional context to the network and resulting in faster and even fuller learning on the problem, whitch is detailed in the post [How to Develop a Bidirectional LSTM For Sequence Classification in Python with Keras](https://machinelearningmastery.com/develop-bidirectional-lstm-sequence-classification-python-keras/#:~:text=Last%20Updated%20on%20January%208,LSTMs%20on%20the%20input%20sequence.).

### Matching Learing
The task of Matching Networks [[Vinyals et al., 2016](#Vinyals2016)] is to learn a classifier ![](https://latex.codecogs.com/gif.latex?c_S) for any given (small) support set ![](https://latex.codecogs.com/gif.latex?S=\\{x_i,y_i\\}^k_{i=1}) (k-shot classification). This classifier defines a probability distribution over output labels ![](https://latex.codecogs.com/gif.latex?y) given a test example ![](https://latex.codecogs.com/gif.latex?\mathbf{x}). Similar to other metric-based models, the classifier output is defined as a sum of labels of support samples weighted by attention kernel ![](https://latex.codecogs.com/gif.latex?a(\mathbf{x},\mathbf{x}_i)) - which should be proportional to the similarity between ![](https://latex.codecogs.com/gif.latex?\mathbf{x}) and ![](https://latex.codecogs.com/gif.latex?\mathbf{x}_i).

<p align="center"><img align="center" width="500" src="https://lilianweng.github.io/lil-log/assets/images/matching-networks.png"></p>
Fig. The architecture of Matching Networks. (Image source: [[Vinyals et al., 2016](#Vinyals2016)])

![](https://latex.codecogs.com/gif.latex?c_S(\mathbf{x})=P(y\vert\mathbf{x},S)=\sum_{i=1}^ka(\mathbf{x},\mathbf{x}_i)y_i,\\,\\,\\text{where}S=\\{(\mathbf{x}_i,y_i)\\}_{i=1}^k)

where ![](https://latex.codecogs.com/gif.latex?x_i), ![](https://latex.codecogs.com/gif.latex?y_i) are the samples and labels from the support set ![](https://latex.codecogs.com/gif.latex?S=\\{x_i,y_i\\}^k_{i=1}), and a is an attention mechanism.

The attention kernel ![](https://latex.codecogs.com/gif.latex?a(\cdot,\cdot)) depends on two embedding functions, ![](https://latex.codecogs.com/gif.latex?f) and ![](https://latex.codecogs.com/gif.latex?g), for encoding the test sample and the support set samples respectively. The attention weight between two data points is the cosine similarity, ![](https://latex.codecogs.com/gif.latex?cosine(.)), between their embedding vectors, normalized by softmax:

![](https://latex.codecogs.com/gif.latex?a(\mathbf{x},\mathbf{x}_i)=\frac{\exp(\\text{cosine}(f(\mathbf{x}),g(\mathbf{x}_{i})))}{\sum_{j=1}^k\exp(\text{cosine}(f(\mathbf{x}),g(\mathbf{x}_j)))})

There are the following two kind of embedding functions:
(1) Simple Embedding

In the simple version, an embedding function is a neural network with a single data sample as input. Potentially we can set ![](https://latex.codecogs.com/gif.latex?f=g).

(2) Full Context Embeddings
The embedding function ![](https://latex.codecogs.com/gif.latex?f) for an example ![](https://latex.codecogs.com/gif.latex?\hat{x}) in the predictoin set (or query set) ![](https://latex.codecogs.com/gif.latex?B) is as follows:

![](https://latex.codecogs.com/gif.latex?f(\hat{x};S)=\\text{attLSTM}(f'(\hat{x});g(S);K))

where, ![](https://latex.codecogs.com/gif.latex?f') is a neural network (e.g., VGG or Inception networks), ![](https://latex.codecogs.com/gif.latex?K) is the number of processing steps in this embedding function ![](https://latex.codecogs.com/gif.latex?f). ![](https://latex.codecogs.com/gif.latex?g(S)) represents the embedding function ![](https://latex.codecogs.com/gif.latex?g) applied to each element ![](https://latex.codecogs.com/gif.latex?x_i) from the support set ![](https://latex.codecogs.com/gif.latex?S).

Its calculate steps is as following:
1. First the test sample goes through a simple neural network, such as a CNN, to extract basic features, ![](http://latex.codecogs.com/gif.latex?f'(x)).

2. Then an LSTM is trained with a read attention vector over the support set ![](https://latex.codecogs.com/gif.latex?S) as part of the hidden state:
![](https://latex.codecogs.com/gif.latex?\begin{aligned}\\hat{\mathbf{h}}_t,\mathbf{c}_t&=\\text{LSTM}(f'(\mathbf{x}),[\mathbf{h}_{t-1},\mathbf{r}_{t-1}],\mathbf{c}_{t-1})\\\\\mathbf{h}_t&=\\hat{\mathbf{h}}_t+f'(\mathbf{x})\\\\\mathbf{r}_{t-1}&=\sum_{i=1}^ka(\mathbf{h}_{t-1},g(\mathbf{x}_i))g(\mathbf{x}_i)\\\\a(\mathbf{h}_{t-1},g(\mathbf{x}_i))&=\\text{softmax}(\mathbf{h}_{t-1}^{\\top}g(\mathbf{x}_i))=\frac{\exp(\mathbf{h}_{t-1}^{\\top}g(\mathbf{x}_i))}{\sum_{j=1}^k\exp(\mathbf{h}_{t-1}^{\\top}g(\mathbf{x}_{\\top}))}\end{aligned})

3. Eventually ![](https://latex.codecogs.com/gif.latex?f_\\theta(\mathbf{x},S)=\mathbf{h}_K) if we do ![](https://latex.codecogs.com/gif.latex?K)  processing steps.

Noting that ![](https://latex.codecogs.com/gif.latex?a) is commonly referred to as a content based attention, and the above softmax normalizes ![](https://latex.codecogs.com/gif.latex?g(x_i)).

For the embedding function ![](https://latex.codecogs.com/gif.latex?g), we described the encoding function ![](https://latex.codecogs.com/gif.latex?g(x_i;S)) for the elements in the support set ![](https://latex.codecogs.com/gif.latex?S) as a bidirectional LSTM.

The above embedding method is called “Full Contextual Embeddings (FCE)”. Interestingly it does help improve the performance on a hard task (few-shot classification on mini ImageNet), but makes no difference on a simple task (Omniglot).

### Model-Agnostic Meta-Learning (MAML)
we consider a model represented by a parametrized function ![](https://latex.codecogs.com/gif.latex?f_\theta) with parameters ![](https://latex.codecogs.com/gif.latex?\theta). When adapting to a new task ![](https://latex.codecogs.com/gif.latex?\mathcal{T}_i), the model’s parameters ![](https://latex.codecogs.com/gif.latex?\theta) become ![](https://latex.codecogs.com/gif.latex?\theta'_i). In our method, the updated parameter vector ![](https://latex.codecogs.com/gif.latex?\theta'_i) is computed using one or more gradient descent updates on task ![](https://latex.codecogs.com/gif.latex?\mathcal{T}_i). For example, when using one gradient update,

![](https://latex.codecogs.com/gif.latex?\theta^\prime_i=\theta-\alpha\nabla_{\theta}L_{\mathcal{T}_i}(f_\theta))

Where, the step size ![](https://latex.codecogs.com/gif.latex?\alpha) may be fixed as a hyperparameter or metalearned.

The model parameters are trained by optimizing for the performance of ![](https://latex.codecogs.com/gif.latex?f_{\theta^{\prime}_i}) with respect to ![](https://latex.codecogs.com/gif.latex?\theta) across tasks sampled from ![](https://latex.codecogs.com/gif.latex?p(\mathcal{T})). More concretely, the meta-objective is as follows:

![](https://latex.codecogs.com/gif.latex?\min_{\theta}\sum_{\mathcal{T}_{i}\sim{p(\mathcal{T})}}\mathcal{L}_{\mathcal{T}_{i}}\left(f_{\theta_{i}^{\prime}}\right)=\sum_{\mathcal{T}_{i}\sim{p(\mathcal{T})}}\mathcal{L}_{\mathcal{T}_{i}}\left(f_{\theta-\alpha\nabla_{\theta}\mathcal{L}_{\mathcal{T}_{i}}\left(f_{\theta}\right)}\right))

Note that the meta-optimization is performed over the model parameters ![](https://latex.codecogs.com/gif.latex?\theta), whereas the objective is computed using the updated model parameters ![](https://latex.codecogs.com/gif.latex?\theta^{\prime}). In effect, our proposed method aims to optimize the model parameters such that one or a small number of gradient steps on a new task will produce maximally effective behavior on that task.

The meta-optimization across tasks is performed via stochastic gradient descent (SGD), such that the model parameters ![](https://latex.codecogs.com/gif.latex?\theta) are updated as follows:

![](https://latex.codecogs.com/gif.latex?\theta\leftarrow\theta-\beta\nabla_{\theta}\sum_{\mathcal{T}_{i}\sim{p(\mathcal{T})}}\mathcal{L}_{\mathcal{T}_{i}}\left(f_{\theta_{i}^{\prime}}\right))

where ![](https://latex.codecogs.com/gif.latex?\beta) is the meta step size.

<p align="center"><img align="center" width="500" src="https://github.com/x5675602/postFireSeverityAssessment/blob/master/notePic/MAML%20algorithm.png"></p>

## Reference
<span id="Wang2019">[Wang2019] Wang, Yaqing, et al. "Generalizing from a few examples: A survey on few-shot learning." ACM Computing Surveys (CSUR) (2019).</span>

<span id="Hochreiter2001">[Hochreiter2001] S. Hochreiter, A. S. Younger, and P. R. Conwell. 2001. Learning to learn using gradient descent. In International Conference on Artificial Neural Networks. 87–94.</span>

<span id="Hochreiter1997">[Hochreiter1997] Hochreiter, Sepp, and Jürgen Schmidhuber. "Long short-term memory." Neural computation 9.8 (1997): 1735-1780.</span>

<span id="Vinyals2016">[Vinyals2016] Vinyals, Oriol, et al. "Matching networks for one shot learning." Advances in neural information processing systems. 2016.</span>






















