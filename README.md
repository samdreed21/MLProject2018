# MLProject2018
CSCI 4622 Project Proposal
Taylor Jesse, Nelson Mitchell, Samuel Reed
October 2018
1 Project Description
For our semester project, we chose to enter the Photometric LSST Astronomical
Time-Series Classification Challenge (PLAsTiCC) on Kaggle. Our group gravitated
towards this project because we are very interested in astronomy. This
project is worth studying because research and technology for space exploration
have grown exponentially over the past decade. With the new advancements in
big data and machine learning, we could help the space community by providing
mass processing and classification tools. Applying our knowledge in machine
learning to a real-world problem will be fun and very rewarding. Additionally,
we are excited to participate in the advancement of science and technology (and
possibly win some money).
2 Why Machine Learning?
Machine learning techniques are incredibly appropriate to solve astronomical
classification problems and can offer insightful observations that may not stand
out from the human point of view. Astronomical observation data is astronomically
large and machine learning can process these massive amounts of
information much more efficiently than humans. Machine learning techniques
also can identify patterns that we may often miss and combined with careful
feature selection these machine learning techniques can provide insightful perspectives
as to why these astronomical events happen the way they do. With
such a large amount of data and such a broad problem, machine learning appears
to be the most fitting way to efficiently classify astronomical objects and
events.
3 Access to Data
The data set is readily available on Kaggle (see the “data” tab).
1
4 Initial Thoughts on Possible Approaches
We are given some basic features to consider, like the location in space of an
object and the dust in that sector of the milky way, but the core of the data is in
multi-channel time-series. Specifically for each example in the training set, we’re
given measurements over time of several bands of light, ranging from infrared
to gamma-rays, with the added caveat that the telescope can only observe one
band at a time. There are obvious statistical features that can be extracted
from each band like mean, standard deviation, etc.; as well as features that can
be engineered from multiple bands, like covariance.
Along the way, we expect to run into challenges posed by the scope of the data,
and must account for examples that exhibit abnormal time-series. For example,
some classes of astronomical events exhibit periodic changes in flux for each
band and would be difficult to classify given only condensed statistical data.
Our initial plan on how to approach this problem is to first extract statistical
features from the time-series data, then perform principal component analysis
on the extracted features to reduce the number of channels in each time-series
and/or process them for efficiency, then apply a recurrent neural network over
the raw time-series data (like the LSTM model from HW3) to leverage the timeseries’
sequential nature and pick up on patterns in the data like periodicity and
spikes.
Link to PLAsTiCC on Kaggle: https://www.kaggle.com/c/PLAsTiCC-2018
2
