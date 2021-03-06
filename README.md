ILSTP
=====
Hi! You are welcome to visit here!<br>
This repository is used to release the code of ILSTP, a newly proposed model for session-based recommendation by our research team. **ILSTP** stands for **Integration of Long- and Short-Term Preferences for session-based recommendation**, which combines time interval embedding function, self-attention, hybrid aggregator, gated graph neural network, and attention aggregator to effectively integrate both users’ long- and short-term preferences together to produce accurate recommendations. ILSTP's research paper, titled "**Integrating Users’ Long- and Short-Term Preferences for Session-based Recommendation**", has been published in the proceedings of the 2022 IEEE 25th International Conference on Computer Supported Cooperative Work in Design (IEEE CSCWD 2022). The citation format is as follows:

Hanlin Liu, Zhuoming Xu, Qianqian Zhang, Yan Tang, "Integrating Users’ Long- and Short-Term Preferences for Session-based Recommendation," *2022 IEEE 25th International Conference on Computer Supported Cooperative Work in Design (CSCWD)*, 2022, pp. 611-616. https://doi.org/10.1109/CSCWD54268.2022.9776254.

We used TensorFlow to implement our ILSTP model based on the self-attention based sequential model SASRec [proposed by Wang-Cheng Kang et al., ICDM'18, https://doi.org/10.1109/ICDM.2018.00035] and the GNN-based session-based recommendation model SR-GNN [proposed  by Shu Wu et al., AAAI'19, https://doi.org/10.1609/aaai.v33i01.3301346]. Our main modifications include: i) Python code of the time interval embedding function was added before the self-attention in SASRec; ii) Python code of the hybrid aggregator was added after the self-attention in SASRec; iii) Python code of the preference integration layer was added based on SR-GNN.


Three real-world datasets (XING, Reddit, and MovieLens 20M) were used to empirically evaluate the performance of ILSTP, and the experimental results show that ILSTP achieves new state-of-the-art performance for next item recommendation in terms of recommendation accuracy. Detailed information about the experimental datasets and the comparison models are given below.


Experimental Datasets
--
* **XING** (https://www.xing.com/en). This dataset contains interactions (click, bookmark, reply, and delete) on job postings for 770,000 users over an 80-day period. As in [1], the interaction data were partitioned into sessions by using a 30-minute idle threshold. Interactions of type ‘delete’ were discarded; continuously repeated interactions of the same type within a session were also discarded in order to reduce noise. Finally, we removed sessions with less than 3 interactions and users with less than 5 sessions.

* **Reddit** (https://www.kaggle.com/colemaclean/subreddit-interactions). This dataset contains a log of user interaction (i.e., adding comments to threads by users) with timestamps on different subreddits. We preprocessed the data and partitioned the user interactions into sessions in the same way as in [2].

* **MovieLens 20M** (https://grouplens.org/datasets/movielens/20m/) [3]. This dataset contains approximately 20 million user ratings for movies (i.e., interaction data) on the MovieLens website. We extracted the interaction data from 2005 to 2015 from the original dataset, and segmented the user’s daily interaction data into sessions.


References:

[1] Massimo Quadrana, Alexandros Karatzoglou, Balázs Hidasi, Paolo Cremonesi: Personalizing Session-based Recommendations with Hierarchical Recurrent Neural Networks. RecSys 2017: 130-137. https://doi.org/10.1145/3109859.3109896


[2] Massimiliano Ruocco, Ole Steinar Lillestøl Skrede, Helge Langseth: Inter-Session Modeling for Session-Based Recommendation. DLRS@RecSys 2017: 24-31. https://doi.org/10.1145/3125486.3125491


[3] F. Maxwell Harper, Joseph A. Konstan: The MovieLens Datasets: History and Context. ACM Trans. Interact. Intell. Syst. 5(4): 19:1-19:19 (2016). https://doi.org/10.1145/2827872


Comparison Models
------
* **FPMC** is a personalized Markov chain based sequential prediction method.<br>
*`Paper:`* Steffen Rendle, Christoph Freudenthaler, Lars Schmidt-Thieme: Factorizing personalized Markov chains for next-basket recommendation. WWW 2010: 811-820. https://doi.org/10.1145/1772690.1772773<br>
*`Code:`* https://github.com/khesui/FPMC
* **GRU4Rec** is the first RNN-based SR model that uses Gated Recurrent Unit to model high-order dependencies within a session.<br>
*`Paper:`* Balázs Hidasi, Alexandros Karatzoglou, Linas Baltrunas, Domonkos Tikk: Session-based Recommendations with Recurrent Neural Networks. ICLR (Poster) 2016. http://arxiv.org/abs/1511.06939<br>
*`Code:`* https://github.com/hidasib/GRU4Rec
* **SR-GNN** is the first GNN-based SR model that uses GNN to capture complex transitions among items within a session.<br>
*`Paper:`* Shu Wu, Yuyuan Tang, Yanqiao Zhu, Liang Wang, Xing Xie, Tieniu Tan: Session-Based Recommendation with Graph Neural Networks. AAAI 2019: 346-353. https://doi.org/10.1609/aaai.v33i01.3301346<br>
*`Code:`* https://github.com/CRIPAC-DIG/SR-GNN
* **GC-SAN** is a graph contextualized self-attention network which can learn both local and long-range dependencies hidden in the current session.<br>
*`Paper:`* Chengfeng Xu, Pengpeng Zhao, Yanchi Liu, Victor S. Sheng, Jiajie Xu, Fuzhen Zhuang, Junhua Fang, Xiaofang Zhou: Graph Contextualized Self-Attention Network for Session-based Recommendation. IJCAI 2019: 3940-3946. https://doi.org/10.24963/ijcai.2019/547<br>
*`Code:`* https://github.com/johnny12150/GC-SAN
* **MTD** is a multi-task learning framework that models both intra-session item relations and relations between items in the current sessions of different users.<br>
*`Paper:`* Chao Huang, Jiahui Chen, Lianghao Xia, Yong Xu, Peng Dai, Yanqing Chen, Liefeng Bo, Jiashu Zhao, Jimmy Xiangji Huang: Graph-Enhanced Multi-Task Learning of Multi-Level Transition Dynamics for Session-based Recommendation. AAAI 2021: 4123-4130. https://ojs.aaai.org/index.php/AAAI/article/view/16534<br>
*`Code:`* https://github.com/sessionRec/MTD
* **DHCN** is a dual channel hypergraph convolutional network that captures the beyond-pairwise relations between items in the current sessions of different users.<br>
*`Paper:`* Xin Xia, Hongzhi Yin, Junliang Yu, Qinyong Wang, Lizhen Cui, Xiangliang Zhang: Self-Supervised Hypergraph Convolutional Networks for Session-based Recommendation. AAAI 2021: 4503-4511. https://ojs.aaai.org/index.php/AAAI/article/view/16578<br>
*`Code:`* https://github.com/xiaxin1998/DHCN
* **II-RNN** is a two-level RNN model that uses two RNNs to capture both users’ long- and short-term preferences from historical and current sessions.<br>
*`Paper:`* Massimiliano Ruocco, Ole Steinar Lillestøl Skrede, Helge Langseth: Inter-Session Modeling for Session-Based Recommendation. DLRS@RecSys 2017: 24-31. https://doi.org/10.1145/3125486.3125491<br>
*`Code:`* https://github.com/olesls/master_thesis
* **HRNN** is a hierarchical RNN model that uses session-level and user-level RNNs to model users’ short-term and long-term preferences.<br>
*`Paper:`* Massimo Quadrana, Alexandros Karatzoglou, Balázs Hidasi, Paolo Cremonesi: Personalizing Session-based Recommendations with Hierarchical Recurrent Neural Networks. RecSys 2017: 130-137. https://doi.org/10.1145/3109859.3109896<br>
*`Code:`* https://github.com/mquad/hgru4rec
* **SHAN** is a two-layer hierarchical attention network that can simultaneously capture both user’s long-term and short-term preferences.<br>
*`Paper:`* Haochao Ying, Fuzhen Zhuang, Fuzheng Zhang, Yanchi Liu, Guandong Xu, Xing Xie, Hui Xiong, Jian Wu: Sequential Recommender System based on Hierarchical Attention Networks. IJCAI 2018: 3926-3932. https://doi.org/10.24963/ijcai.2018/546<br>
*`Code:`* https://github.com/TsingZ0/SHAN
* **TiSASRec** is time interval aware self-attention based sequential recommendation method without differentiating between long-term and short-term preferences.<br>
*`Paper:`* Jiacheng Li, Yujie Wang, Julian J. McAuley: Time Interval Aware Self-Attention for Sequential Recommendation. WSDM 2020: 322-330. https://doi.org/10.1145/3336191.3371786<br>
*`Code:`* https://github.com/JiachengLi1995/TiSASRec
* **A-PGNN** is a personalized graph neural networks with attention mechanism which models the effects of user’s historical sessions on the current session.<br>
*`Paper:`* Mengqi Zhang, Shu Wu, Meng Gao, Xin Jiang, Ke Xu, Liang Wang: Personalized Graph Neural Networks with Attention Mechanism for Session-Aware Recommendation. IEEE Trans. Knowl. Data Eng. 15 October 2020 (Early Access). https://doi.org/10.1109/TKDE.2020.3031329<br>
*`Code:`* https://github.com/CRIPAC-DIG/A-PGNN
