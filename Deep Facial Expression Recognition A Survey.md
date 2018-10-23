#paper path: https://arxiv.org/pdf/1804.08348.pdf
开始的重点： 

1. 熟悉什么是 情感计算 （Affective computing）， 什么是 facial expression， 什么是 facial action unit  
	
		1. FACIAL expression:  signals for human beings to convey their emotional states and intentions.  
		2. FAU:uses the groups of facial muscles, that can be moved independently, as atomic building blocks
		3. 

2. 熟悉人脸 facial action 中的位置和意义

3. 熟悉 AU recognition 和 AU intensity estimation 的任务 和基本的方法，包括历史方法。 

				

4. 熟悉 Recognition 和 Intensity estimation Deep Leanring 有关的方法 （重点）


FER systems, main categories:  

	static image FER:
	*feature:spatial information
	dynamic sequence FER:
	*feature:relation among frames
Based on these two vision-based methods, other modalities,
such as audio and physiological channels, have also been
used in multimodal systems to assist the recognition of expression.  

Motivation:  

	 we focus our research on deep learning technology for facial emotion recognition tasks based on both static images and videos (image sequences).

Historical Method:

	*local binary patterns (LBP)
	*non-negative matrix factorization (NMF)
	*CNN,RCNN,3D-CNN
	*DBN
	*DAE
	*RNN,LSTM

#DEEP FER  
##THE STATE OF THE ART: 

###Static 

Pre-training and fine-tuning  

	*multistage fine-tuning
	*FaceNet2ExpNet
Diverse network input  

	*mapped LBP
	*scale-invariant feature transform
	*3D Angle+Gradient+Edge(AGE)
	*deep multilevel CNN
	*neighbor-center difference vector (NCDV)
	*deep sparse autoencoder

Auxiliary blocks & layers  
	
	*HoloNet
	*three different layer embedded
	*island loss  and locality-preserving loss (LP loss) 
	*exponential triplet-based loss and (N+M)-tuples  luster loss
	
Network ensemble

	(1)sufficient diversity of the networks to ensure complementarity, and
	(2) an appropriate ensemble method that can effectively aggregatethe committee networks.

Multitask networks  

	* a higher-order Boltzmann machine(disBM)
	* selectivejoint multitask (SJMT)
	* identity-aware CNN (IACNN)
	* a multisignal CNN (MSCNN)

Cascaded networks  

	* ...
	* multiscale contractive convolutional network(CCNET)
	* ...
	* a novel boosted DBN (BDBN)


existing well-constructed deep FER systems focus  
	
	? the lack of plentiful diverse data 
	* Pretraining and fine-tuning
	A practical technique that proved to be particularly useful is pretraining and fine-tuning the network in multiple stages using auxiliary data from large-scale objection or face recognition datasets to small-scale FER datasets, i.e., from large to small and from  eneral to specific
	? expression unrelated variation
	* 
###Dynamic 
####Frame aggregation
decision-level frame aggregation  

feature-level frame aggregation  

####Expression Intensity network

	* peak-piloted deep network(PPDN)
	  peakgradient suppression (PGS)
	* deeper cascaded peak-piloted network (DCPN)
	  cascade finetuning
	* ...
####Deep spatio-temporal FER network
	
RNN and C3D  

	*
Facial landmark trajectory  

	* a deep temporal geometry network (DTGN) 
	* part-based hierarchical bidirectional recurrent neural network (PHRNN)
####Cascaded networks
	
	* long-term recurrent convolutional network (LRCN)
	* ...
####ensemble

###ADDITIONAL RELATED ISSUES

	* DBNs with mPoT
	* ...
	*

###Chanllenge

#ps:  
  
	*ViolaJones (V&J) face detector 
	*IntraFace
	*supervised descent method (SDM)
	*mixtures of trees (MoT)
	*discriminative response map fitting (DRMF)
	*multitask cascaded convolutional networks (MTCNN)
	*DenseReg
	*Tiny Faces
	*


##paper
https://arxiv.org/pdf/1804.08348.pdf  
https://www.doc.ic.ac.uk/~rw2614/  