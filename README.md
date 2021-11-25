ILSTP
=====
Hi! You are welcome to visit here!<br>
This library will be used to release the source code of ILSTP, a newly proposed model for session-based recommendation. The research paper of ILSTP has been submitted to an International conference. ***PLEASE NOTE THAT*** *this library is ***temporarily anonymized***, and ILSTP’s code will ***not*** be released immediately (postponed until the paper is accepted and published).* <br>
<br>
ILSTP stands for Integrating Users’ Long- and Short-Term Preferences for session-based recommendation. Three real-world datasets (XING, Reddit, MovieLens 20M) were used to empirically evaluate ILSTP with eleven representative recommendation models, and the experimental results show that ILSTP achieves new state-of-the-art performance in next interaction (item) recommendation. As a supplement to the content of the paper, additional information about these comparison models is given below.

Comparison Models
------
* **FPMC** is a personalized Markov chain based sequential prediction method.<br>
*`Paper:`* Rendle, S., Freudenthaler, C., Schmidt-Thieme, L.: Factorizing personalized Markov chains for next-basket recommendation. WWW 2010: 811–820. https://doi.org/10.1145/1772690.1772773<br>
*`Code:`* https://github.com/khesui/FPMC
* **GRU4Rec** is the first RNN-based SR model that uses Gated Recurrent Unit to model high-order dependencies within a session.<br>
*`Paper:`* Hidasi, B., Karatzoglou, A., Baltrunas, L., et al.: Session-based Recommendations with Recurrent Neural Networks. ICLR (Poster) 2016. http://arxiv.org/abs/1511.06939<br>
*`Code:`* https://github.com/hidasib/GRU4Rec
* **SR-GNN** is the first GNN-based SR model that uses GNN to capture complex transitions among items within a session.<br>
*`Paper:`* Wu, S., Tang, Y., Zhu, Y., et al.: Session-Based Recommendation with Graph Neural Networks. AAAI 2019: 346–353. https://doi.org/10.1609/aaai.v33i01.3301346<br>
*`Code:`* https://github.com/CRIPAC-DIG/SR-GNN
* **GC-SAN** is a graph contextualized self-attention network which can learn both local and long-range dependencies hidden in the current session.<br>
*`Paper:`* Xu, C., Zhao, P., Liu, Y., et al.: Graph Contextualized Self-Attention Network for Session-based Recommendation. IJCAI 2019: 3940-3946. https://doi.org/10.24963/ijcai.2019/547<br>
*`Code:`* https://github.com/johnny12150/GC-SAN
* **MTD** is a multi-task learning framework that models both intra-session item relations and relations between items in the current sessions of different users.<br>
*`Paper:`* Huang, C., Chen, J., Xia, L., et al.: Graph-Enhanced Multi-Task Learning of Multi-Level Transition Dynamics for Session-based Recommendation. AAAI 2021: 4123-4130. https://ojs.aaai.org/index.php/AAAI/article/view/16534<br>
*`Code:`* https://github.com/sessionRec/MTD
* **DHCN** is a dual channel hypergraph convolutional network that captures the beyond-pairwise relations between items in the current sessions of different users.<br>
*`Paper:`* Xia, X., Yin, H., Yu, J., et al.: Self-Supervised Hypergraph Convolutional Networks for Session-based Recommendation. AAAI 2021: 4503-4511. https://ojs.aaai.org/index.php/AAAI/article/view/16578<br>
*`Code:`* https://github.com/xiaxin1998/DHCN
* **II-RNN** is a two-level RNN model that uses two RNNs to capture both users’ long- and short-term preferences from historical and current sessions.<br>
*`Paper:`* Ruocco, M., Skrede, O.S.L., Langseth, H.: Inter-Session Modeling for Session-Based Rec-ommendation. DLRS@RecSys 2017: 24–31. https://doi.org/10.1145/3125486.3125491<br>
*`Code:`* https://github.com/olesls/master_thesis
* **HRNN** is a hierarchical RNN model that uses session-level and user-level RNNs to model users’ short-term and long-term preferences.<br>
*`Paper:`* Quadrana, M., Karatzoglou, A., Hidasi, B., et al.: Personalizing Session-based Recom-mendations with Hierarchical Recurrent Neural Networks. RecSys 2017: 130–137. https://doi.org/10.1145/3109859.3109896<br>
*`Code:`* https://github.com/mquad/hgru4rec
* **SHAN** is a two-layer hierarchical attention network that can simultaneously capture both user’s long-term and short-term preferences.<br>
*`Paper:`* Ying, H., Zhuang, F., Zhang, F., et al.: Sequential Recommender System based on Hierarchical Attention Networks. IJCAI 2018: 3926–3932. https://doi.org/10.24963/ijcai.2018/546<br>
*`Code:`* https://github.com/TsingZ0/SHAN
* **TiSASRec** is time interval aware self-attention based sequential recommendation method without differentiating between long-term and short-term preferences.<br>
*`Paper:`* Li, J., Wang, Y., McAuley, J.J.: Time Interval Aware Self-Attention for Sequential Rec-ommendation. WSDM 2020: 322–330. https://doi.org/10.1145/3336191.3371786<br>
*`Code:`* https://github.com/JiachengLi1995/TiSASRec
* **A-PGNN** is a personalized graph neural networks with attention mechanism which models the effects of user’s historical sessions on the current session.<br>
*`Paper:`* Zhang, M., Wu, S., Gao, M., et al.: Personalized Graph Neural Networks with Attention Mechanism for Session-Aware Recommendation. IEEE Trans. Knowl. Data Eng. 15 Octo-ber 2020 (Early Access). https://doi.org/10.1109/TKDE.2020.3031329<br>
*`Code:`* https://github.com/CRIPAC-DIG/A-PGNN
