Spatial Relational Graph Visualizer: the SRGViz Library
========================

Srgviz is a C++ framework to manage graphs of 3D transformation. 
It provides the basic features of updating transformation and querying transformation between any pair of frames plus a set of features that distinguishes it from all the other existing framework.

Uncertainty
-------
Srgviz allows to specify every transformation with an associated covariance. Covariances are propagated and added when calculating the transformation between two distant frames. This allows to obtain the uncertainty with which a given transformation is know. 
Uncertainty is managed using the SE(3) ...

Calibration & Fusion
--------
The framework is specialized in solving calibrations and performing sensor fusion.
Calibration is the process of finding the fixed transformation between two different frames, e.g a camera attached to a robot head. This can be done with the support of an intermediate frame for which the transformation with respect to the other two frames is known, e.g a marker. Srgviz allows, once specified the two calibration frames, to calculate their transformation.

There are situation in which the previous approach cannot be used, suppose a 
