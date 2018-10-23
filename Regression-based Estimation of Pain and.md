#Two fold 

##1,  a novel set of Bayesian regression-based learning methods 
###motivation
focus on continuous-valued affect recognition

	 *model imitates a discrete function at the training data points, regressor training is performed using discrete outputs (e.g., AU intensity labels from 0 to5).

goal

	(1) expression components, i.e., Facial Action Units (AUs) of the Facial Action 
	Coding System (FACS) [44], in response to various emotions including pain, and 
	(2) one prototypical expression, i.e., the facial expression of pain, in response to pain induction.

	The research goal can be summarized as obtaining a AU and pain intensity estimation
	 method that (a) treats the face component wise and (b) produces outputs on a 
	continuous scale.

contribution  

	(1) development of a baseline method for automatic estimation of pain / AU intensity based on existing regression techniques,

	(2) development of a new regression approach to the target problem that finds out
	informative facial parts and exploits that knowledge, 
	(3) development of a new regression approach that combines part-based focus with joint target inference, and 
	(4) creation of a new database.
###three novel regression methods
1, Relevance Vector Machine (RVM)  
	
	treats the observed face holistically and estimates the intensity of target expressions 
AU and pain intensity estimation method  

	1, we extract shape-based features (i.e, locations of characteristic facial points) and appearance-based features (Local Binary Patterns (LBPs) [135] and Discrete Cosine Transform (DCT) [4]) from facial images of subjects displaying different intensities of pain.
	2, step, for each set of features we train separate regression models (we employ Relevance VectorRegression (RVR) [174]) for prediction of the pain intensity levels. 
	3, the outputs of theregressors trained using different feature sets are combined in two ways
2, Doubly Sparse RVM (DSRVM)  
		
	automatically learns the importance of various facial parts for the target task  
	by enforcing double sparsity by jointly selecting the most relevant training examples (a.k.a. relevance vectors)and the most important kernels associated with the informative facial parts for estimation of facial expression intensity
3, latent tree (LT) mode  

	jointly learns the inter-dependence of facial parts and multiple AU or pain targets
	that efficiently learns a hidden inference structure between features and targets

####method
pre-processing  

	3 sets of features:  
	FacialLandmark Points (PTS), Local Binary Patterns (LBP) and Discrete Cosine Transform (DCT)	 

###Advantages  
	1, achieves better intensity estimationof AUs compared to existing methods, especially in the presence of noisy inputs.

##2, release a multi-modal database
###EmoPain

	 consists of spontaneously displayed pain-related facial expressions and body movements recorded by multiple modalities, while patients with chronic back-pain were performing instructed physical exercises.



##ps

Face detection  

	* cascade of Ada Boost classifiers and Haar features.
	* Deformable Part Models(DPM)

Facial Landmark Localization  

	“shape” means a set of landmark points
	“appearance” means a set of image pixel intensities
	* e Active Shape Model (ASM)
	* a learned Point Distribution Model (PDM)
	* Active Appearance Models (AAM)
	  piece-wise affine warp (PWA)
	* Constrained Local Models (CLM)
	  Regularized-Landmark Mean-Shift
	* Particle Filtering with Factorized Likelihoods (PFFL)
	* Supervised Descent Method (SDM) 

Face Registration  

	* Procrustes analysis
	* piece-wise affine warp (PWA)
	* extracting pixel regions from patches centered around landmarks (LCP)

Feature Extraction  

	* Facial Landmark Points (PTS)
	* Gabor filter banks
	* Log-normal filters
	* Discrete Cosine Transform(DCT)
	* Histogram of Gradients (HOG)
	* Local Binary Patterns (LBP)
	* scale invariant feature transform

Dimensionality Reduction

	* Vector Quantization (VQ)
	* PCA
	* Independent Component Analysis (ICA)
	*  Non-negative matrix Factorization (NMF)
	*  Linear Discriminant Analysis (LDA)
	*  Spectral Regression (SR)
	*  The Minimal-Redundancy-Maximal-Relevance Criterion (mRMR)
	*  AdaBoost and GentleBoost

Expression Detection  

	* PCA,LDA,SVM
	* RVM
	* AU-specific SVM classifiers based on Gabor features and through SVM
	* AUs detected,LR

Expression Intensity Estimation

static  

	* k-NN
	* SVM
	* Nnet
	* ...

dynamic  

	* Hidden Markov Models (HMM)
	* MRF: Markov Random Field
	* Dynamic Bayesian (DBN)
	* Conditional Random Fields (
	* 
	* CRF)
	* Continuous Conditional Neural Fields (CCNF)
	* Conditional Ordinal Random Field (CORF)

Metrics

	* Pearson productmoment correlation coefficient (CORR)
	* mean squared error (MSE)
	* Intra-class correlation coefficient (ICC)