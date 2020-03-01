- [A Survey on Bias and Fairness in Machine Learning (2019)](https://arxiv.org/pdf/1908.09635)  Ninareh Mehrabi (University of Southern California), Fred Morstatter (University of Southern California), Nripsuta Saxena (University of Southern California) Kristina Lerman (University of Southern California), Aram Galstyan (University of Southern California)  
Key ideas: Systematically summary and categorize definitions of fairness, methods for fairness-aware machine learning, state challenges and future opportunities  
(1) Sources Bias-> bias arising from data, bias arising from algorithms  
(2) Types of fairness-> individual fairness, group fairness, subgroup fairness  
(3) Methods that target biases in algorithms-> pre-processing, in-processing, post-processing  
(4) Challenges-> how to transform from equality to equity (each individual or group is given the resources they need to succeed), is one synthetic definition of fairness possible, given a dataset how to identify unfairness  
- [Fairness and Transparency in Ranking (SIGIR'18)](https://dl.acm.org/ft_gateway.cfm?id=3308783&ftid=2036216&dwn=1&CFID=119489206&CFTOKEN=76711083f903224c-E779318B-BFED-B517-2464C9710362C053)	Carlos Castillo	(Universitat Pompeu Fabra)     
Key ideas: A summary of measures and methods for fairness-aware ranking.  
A new classification mode -> attention/exposure-based measures and probability based measures.  
- [Beyond Parity: Fairness Objectives for Collaborative Filtering (NIPS'17)](https://arxiv.org/pdf/1705.08804) Sirui Yao (Virginia Tech), Bert Huang (Virginia Tech)  
Task: CF-based recommendation.  
Previous work: demographic parity (the metric, but is only suitable when preference is unrelated to sensitive features), equal opportunity (basis of this paper)  
Challenge: In recommendation problems, preferences are related to sensitive features.  
Key ideas: Define four new metrics to measure unfairness in CF: value unfairness, absolute unfairness, underestimation unfairness, overestimation unfairness and add them as penalty to loss function for optimization.  
(1) Bias exists even reconstruction error is not high (verify challenge).  
(2) Optimize the model with the proposed penalty functions can reduce unfairness while maintain reconstruction accuracy.  
- [Fairness-Aware Tensor-Based Recommendation (CIKM'18)](http://faculty.cse.tamu.edu/caverlee/pubs/zhu2018fairness.pdf) Ziwei Zhu (Texas A&M University), Xia Hu (Texas A&M University), James Caverlee (Texas A&M University) [[code]](https://github.com/Zziwei/Fairness-Aware_Tensor-Based_Recommendation)
Task: MF-based recommendation.  
Previous work: Matrix factorization, tensor-based method.  
Challenge: 2D MF could not deal with multi-interactions, multiple sensitive attributes exist, recommendation quality trade-off
Key ideas: Tensors, sensitive features are first isolated from recommendation tensors and then sensitive information is extracted.    
(1) Tensor-based approach-> capture multi-way interactions among users, items, and contexts  
(2) Isolation-> Force two (if the sensitive attribute is a binary case) columns of the latent factor matrix to be sensitive features.  
(3) Extraction-> Orthogonal constraint term and L2-norm constraint term are introduced to make sure all sensitive information is extracted to the sensitive features.
