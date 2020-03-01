- [A Survey on Bias and Fairness in Machine Learning (2019)](https://arxiv.org/pdf/1908.09635)  Ninareh Mehrabi, Fred Morstatter, Nripsuta Saxena, Kristina Lerman, Aram Galstyan (University of Southern California)  
  **Key ideas**: Systematically summary and categorize definitions of fairness, methods for fairness-aware machine learning, state challenges and future opportunities  
  (1) Sources Bias -> bias arising from data, bias arising from algorithms  
  (2) Types of fairness-> individual fairness, group fairness, subgroup fairness  
  (3) Methods that target biases in algorithms -> pre-processing, in-processing, post-processing  
  (4) Challenges -> how to transform from equality to equity (each individual or group is given the resources they need to succeed), is one synthetic definition of fairness possible, given a dataset how to identify unfairness  

- [Fairness and Transparency in Ranking (SIGIR'18)](https://dl.acm.org/ft_gateway.cfm?id=3308783&ftid=2036216&dwn=1&CFID=119489206&CFTOKEN=76711083f903224c-E779318B-BFED-B517-2464C9710362C053)	Carlos Castillo	(Universitat Pompeu Fabra)     
  **Key ideas**: A summary of measures and methods for fairness-aware ranking.  
  A new classification mode -> attention/exposure-based measures and probability based measures.  

- [Beyond Parity: Fairness Objectives for Collaborative Filtering (NIPS'17)](https://arxiv.org/pdf/1705.08804) Sirui Yao, Bert Huang (Virginia Tech)  
  **Task**: CF-based recommendation.  
  **Previous works**: Demographic parity (the metric, but is only suitable when preference is unrelated to sensitive features), equal opportunity (basis of this paper)  
  **Challenges**: In recommendation problems preferences are related to sensitive features.  
  **Key ideas**: Define four new metrics to measure unfairness in CF: value unfairness, absolute unfairness, underestimation unfairness, overestimation unfairness and add them as penalty to loss function for optimization.  
  (1) Bias exists even reconstruction error is not high (verify challenge).  
  (2) Optimize the model with the proposed penalty functions can reduce unfairness while maintain reconstruction accuracy.  

- [Fairness-Aware Tensor-Based Recommendation (CIKM'18)](http://faculty.cse.tamu.edu/caverlee/pubs/zhu2018fairness.pdf) Ziwei Zhu, Xia Hu, James Caverlee (Texas A&M University) [[code]](https://github.com/Zziwei/Fairness-Aware_Tensor-Based_Recommendation)  
  **Task**: MF-based recommendation  
  **Previous works**: Matrix factorization, tensor-based method   
  **Challenges**: 2D MF could not deal with multi-interactions, multiple sensitive attributes exist, recommendation quality trade-off  
  **Key ideas**: Tensors, sensitive features are first isolated from recommendation tensors and then sensitive information is extracted.    
  (1) Tensor-based approach -> capture multi-way interactions among users, items, and contexts  
  (2) Isolation -> force two (if the sensitive attribute is a binary case) columns of the latent factor matrix to be sensitive features  
  (3) Extraction -> orthogonal constraint term and L2-norm constraint term are introduced to make sure all sensitive information is extracted to the sensitive features.  

- [Fairness in Deep Learning: A Computational Perspective (2019)](https://arxiv.org/abs/1908.08843)  Mengnan Du, Fan Yang , Na Zou, Xia Hu (Texas A&M University)  
  **Key ideas**: Where DNN unfairness comes from, how interpretability can be made use of  
  (1) DNN unfairness: prediction outcome discrimination (via input and via representation) and prediction quality disparity  
  (2) Input bias -> local interpretation, detect: generate feature importance vector for an input (local approximation based, perturbation based, back-propagation based, and decomposition based methods), mitigate: regularization  
  (3) Representation bias ->  global interpretation, detect: calculate the directional derivative of DNN's prediction to concept activation vector (CAV), adds this CAV to different inputs' intermediate activation and then observe the change of model prediction, mitigate: adversarial training  
  (4) Prediction quality disparity (caused by underrepresentation) -> local and global interpretation-> detect: split data into subgroups, calculate prediction accuracy separately, mitigate: GAN, regularizing, transfer learning, (sanity check in the end) 

- [Fairness in Recommendation Ranking through Pairwise Comparisons (KDD'19)](https://doi.org/10.1145/3292500.3330745) Alex Beutel, Jilin Chen, Tulsee Doshi, Hai Qian, Li Wei, Yi Wu, Lukasz Heldt, Zhe Zhao, Lichan Hong, Ed H. Chi, Cristos Goodrow (Google)  
  **Task**: Neural collaborative filtering based recommendation   
  **Previous works**: Pointwise recommender, pairwise ranking  
  **Challenges**: Most fairness-aware recommenders treats recommendation as a pointwise prediction problem and applying those predictions for ranked list construction but this doesn't indicate the ranked list is fair. Unbiased offline evaluation is large in scale and thus costing in space and time.  
  **Key ideas** introduce Pairwise Fairness and a regularizer  
  (1) pairwise fairness: the likelihood of a clicked item being ranked above another relevant unclicked item is the same across both groups-> intra-group and inter-group.  
  (2) The model is penalized by the regularizer if its ability to predict which item was clicked is better for one group than the other.  
  
- [Fairness Is Not Static: Deeper Understanding of Long Term Fairness via Simulation Studies (FAT'20)](https://dl.acm.org/doi/pdf/10.1145/3351095.3372878?download=true) Alexander D’Amour, Hansa Srinivasan, James Atwood, Pallavi Baljekar, D. Sculley, Yoni Halpern (Google Research) [[code]](https://github.com/google/ml-fairness-gym/)  
  **Task**: Evaluate long-term implications of deploying a fairness-aware machine learning based decision system.  
  **Previous works**: Static problem setting and evaluation    
  **Challenges**: Long term dynamics are hard to assess in real practice  
  **Key ideas**: A simulation framework with agent-environment interaction loop and metrics  
  (1) Fit the problem into the framework of Markov Decision Processes.  
  (2) Agents interact with simulated environments in an alternating loop.  
  (3) Evaluate long-term fairness questions with metrics that characterize the realized consequences of an agent’s policy for different subpopulations by summarizing the the environment’s state over time.

-  [Fairness-Aware Ranking in Search & Recommendation Systems with Application to LinkedIn Talent Search (KDD'19)](https://arxiv.org/pdf/1905.01989) Sahin Cem Geyik, Stuart Ambler, Krishnaram Kenthapadi (LinkedIn Corporation)  
  **Task**: Fairness-aware ranking   
  **Previous works**: Unfair web-scale search and recommendation  
  **Key ideas**: Post-processing, re-rank the top-k items provided by baseline (unfair) ranking algorithms  
  (1) Deterministic Greedy (DetGreedy) algorithm -> generates rankings with as high score candidates as possible  
  (2)Deterministic Conservative (DetCons) algorithm and Deterministic Relaxed (DetRelaxed)-> integrality constraints, deal with cases when minimum representation requirements are violated   
  (3) Deterministic Constrained Sorting (DetConstSort) -> with programming, waits for multiple indices of recommendation before deciding on the next attribute value to get a candidate from, and may change its previous decisions  
  (4) Evaluate the framework on simulated data (majority of the experiments) and online test  
  
- [Compositional Fairness Constraints for Graph Embeddings (ICML'19)](https://arxiv.org/pdf/1905.10674.pdf) Avishek Joey Bose (McGill University, Mila), William L. Hamilton (McGill University, Mila, Facebook Research) [[code]](https://github.com/joeybose/Flexible-Fairness-Constraints)  
  **Task**: (Social) Graph embedding  
  **Previous works**: Implementation of invariance constraints in classification and CF  
  **Challenge**: (Of apply invariance constraints) The non-i.i.d. and non-Euclidean nature of relational, graph data  
  **Key ideas**: Learn a set of adversarial filters to remove information about particular sensitive attributes  
  (1) Enforcing representational invariance constraints on the node embeddings.  
  (2) Function ENC maps node to an embedding -> attribute-specific filter filters sensitive attributes-> compositional encoder to compose the filtered embeddings-> final embedding  
  (3) Adversarial regularizer -> train the compositional encoder

