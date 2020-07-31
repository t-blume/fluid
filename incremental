Existing graph summarization algorithms are tailored to specific graph summary models, only support one-time batch computation, are designed and implemented for a specific task, or evaluated using static graphs. 
Our novel, incremental, parallel algorithm addresses all these shortcomings. 
Our algorithm solves the set union problem following the signal and collect programming model. 
We support all structural graph summary models that are defined in FLUID. All graph summaries can be updated in O(\Delta \cdot d^k), where \Delta is the number 
of additions, deletions, and modifications in the input graph, d is the maximum degree of the input graph, and k is the maximum distance in the subgraphs considered. 
We empirically evaluate the performance of our algorithm on benchmark and real-world datasets. 
Our experiments show that for commonly used summary models and datasets, the incremental summarization algorithm almost always outperforms their batch counterpart, 
even when about $50%$ of the graph database changes. 
The source code and the experimental results are openly available for reproducibility and extensibility.



## General Idea
1. Load the data graph from disk (gzipped, n-triple files)
2. Parse the RDF graph into a spark labeled property graph
3. Phase 0: partition the graph by a random vertex cut such that vertices and their outgoing (or incoming edges for undirected graphs) are in the same partition.
4. Phase 1.1: each vertex computes its own local schema based on vertex label and edge label
5. Phase 1.2: signal and collect the neighbor information to construct complex schemas
6. Phase 2: write the graph to OrientDB, merge on collision.

If incremental computation is used, skip step 6 (phase 2) for all unchanged vertices.
![images/algorithm-idea.png](images/algorithm-idea.png)
Figure 1: Visualizing the idea of the algorithm. Label ofvertices and edges are represented by orange shapes.
