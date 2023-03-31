# SKNN

Approximating K-Nearest-Neighbors with Siamese neural nets.
----

One component K-Nearest-Neighbors algorithm (KNN) is the similarity metric $\kappa(a, b)$ that indicates how similar $a$ and $b$ are. This metric is often chosen on the bases of some performance criterion. The second component is a support set, also known as prototypes set, which contains a some samples that sparsely cover the data manifold. For any new example $x$, KNN then compares $x$ to every prototype $x_1, \ldots, x_N$ and picks the $k$ most similar ones. Finally, the prediction $\hat{y}$ of $x$ is given by the average of outcomes associated to this subset of prototypes.

The curse-of-dimensionality hurts KNNs, because hand-crafted similarity metrics fail at discriminating distances in high dimensions. As a result, the algorithm requires (exponentially) more examples do alleviate the similarity metric's shortcomings. In this project, I explore learning the similarity metric from data. Anyone reading this can be 100% sure this idea is not novel. Despite me not citing prior work. With that said, I am exploring an idea that occurred to me. Instead of pre-training the similarity metric on a training dataset, I train it on the prototype set directly by employing a bootstrapping technique.


