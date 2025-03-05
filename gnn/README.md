# GNN (Graph Neural Networks)
- https://arxiv.org/pdf/2010.05234
- 

## Introduction

Graph Neural Networks (GNNs) are NN models that try to leverage graph-structured data. Meaning that can be represented as nodes and edges in a graph.
- Nodes: Vertices on graph (representing items or entities)
- Edges: Connections between the nodes (represent relationships)
- $G = G(V, E)$
- Neighborhoods: subgraphs within a graph
- Features: Quantifiable attributes that are being analyzed. (Ex: age, popularity, etc)
- Embeddings: COmpressed feature representations. 
- Output types: Can think of as converting input graphs into useful embeddings, preforming some down-stream task to simplify into some useful output. 
  - Vertex Level: Requires prediction for each vertex
  - Edge Level: Prediction for each edge
  - Graph Level: Prediction for each graph

 Some areas where they are useful is in areas such as social networks, molecular structures, etc. GNNs work by following a message passing or neighborhoood aggregation paradigm. Each node starts with an initial feature. Then the GNN proceeds in layers where the information is given to its neighbors. As the layers increase, the information spreads throughout the graph, where the GNN hopes to learn patterns from this structured learning. 

 ### Why GNNs? 

 Traditional methods like CNNs or RNNs have trouble with irregular structures of graph, the lack of order, and large numbers of nodes. GNNs provide a framework of message passing / information aggregation that allows neural networks to learn this structure more easily. In addition because of the loose structural requirements, the number of vertices and edges can change. This means GNNs have the ability to handle non-Euclidean unstructured data. In contrast, a CNN for the MNIST problem might require all images in 28 $\times$ 28 format. 

 GNNs relies on message passing and aggregation
- Message Passing: Where each node sends messages to its neighboring nodes. 
- Aggregation: Each node aggregates incoming messages using some function (weighted sum, mean, attention-based, etc.)
- Updating: The information from aggregation is combined with the node's currect information to update it. 

The biggest difference in different GNN structures is how they aggregate and update information. 
- Conv GNNs: Treat neighbor aggregation as a weighted sum based on the graph structure. 
- Attention-based GNNs: Use learnable attention coefficients to learn which connections are more important than others. 
- (More)

### Key Architectures

The biggest difference in different GNN structures is how they aggregate and update information. For example CNNs treat neighbor aggregation as a weighted sum. In contrast attention-based GNNs use learnable attention coefficients to learn which connections are more important than others. 

  1. Recurrent Graph Neural Networks (RGNNs)
     1. Graph LSTMs
     2. Gated GNNs
  2. Convolutional Graph Neural Networks (CGNNS)
     1. Spatial CGNNs
     2. 
  3. Graph Attention Networks (GATs)
  4. Graph Autoencoders (GAEs) / Variational Graph Autoencoders (VGAEs)
  5. Transformer GNNs

### Challenges: 

  1. Scalability
  2. Oversmoothing
  3. GNN - Isomorphism Issue
  4. Heterogeneity / Dynamic Graphs
  5. Interpretability
    
## Application Areas and Research

 ### Biomedical Applications
 - Drug Discovery 
   - Chemoinformatics
   - Drug-target Interaction Prediction
   - Novel Drug Discovery
   - Drug Repurposing
 - Disease Prediction
   - Gene Network Learning
   - Patient Similarity Graphs
   - Multimodal networks
 - Biomedical Imaging
   - Brain Connectivity
   - Cellular Imaging
   - Tumor Classification
   - Interpretability, graph representation


  ### PINNs

  Many physical systems can be represented as graphs, which leads to a combination of PINNs and GNNs. 
  
  - GNNs - Meshes for PDEs
  - Planetary Motion, Molecular Dynamics, (Many particle systems)

## Introductory Project Ideas
- Simple Node Classification
- Physics Simulation

## Add resources
A Gentle Introduction to Graph Neural Networks
Surveys
https://pmc.ncbi.nlm.nih.gov/articles/PMC8360394/#:~:text=perspectives,in%20many%20biological%20tasks%20at

PyTorch Geometric’s documentation and examples, TensorFlow’s Graph Neural Networks guide