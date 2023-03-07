This repository complements an academic report titled "Human Brain Networks" that I submitted as part of the MSc in Mathematical Modelling and Scientific Computing at the University of Oxford. The report compares various datasets of human brain networks to small-world and scale-free networks to gain insight into the basic mechanisms of the human brain. Additionally, I analysed the resulting Laplacian matrices and proposed a novel generative model.

Datasets:

- `100307_connectome_scale500.mat`: 1st brain dataset
- `100408_connectome_scale500.mat`: 2nd brain dataset
- `101006_connectome_scale500.mat`: 3rd brain dataset
- `101107_connectome_scale500.mat`: 4th brain dataset
- `101309_connectome_scale500.mat`: 5th brain dataset

Main codes:

- `brains.m`: computes adjacency matrix, laplacian and spectrum of the datasets
- `comparison.m`: compares Watts-Strogatz, Barabasi-Albert and the proposed model with the data
- `distributions.m`: finds the interpolant for the degree distribution of the data
- `motifs.m`: computes the motif analysis of the data (codes can be found at https://sites.google.com/site/bctnet/)
- `tables.m`: tables of measures (from `measures.m`) on data, some random samples, and the proposed model

Auxiliary codes:

- `BarabasiAlbert.m`: scale-free network using Barabasi-Albert algorithm
- `charpath.m`: characteristic path length
- `clustering.m`: global clustering coefficient
- `degreedist.m`: degree distributions
- `efficiency.m`: global efficiency
- `measures.m`: number of  nodes, of edges, maximum degree, clustering coefficient, efficiency
- `Model.m`: candidate neural model
- `rewire.m`: rewires edges so as to randomise the network (based on Maslov and Sneppen)
- `spec.m`: spectrum of normalised Laplacian
- `WattsStrogatz.m`: small-world network using Watts-Strogatz algorithm

The dataset `full_computed_data.mat` contains all the results we computed using the previous codes:

- `AdjData.m`: adjacency matrices of the data
- `CoefDist.m`: coefficients of the interpolant of the degree distribution
- `EigData.m`: eigenvalues of laplacians of the data
- `GamData.m`: gamma distribution of EigData
- `GamMod.m`: mean gamma distribution of eigenvalues from the models (WS, BA, proposed)
- `LaplData.m`: laplacians of the data
- `Motifs.m`: motif fingerprints of the data
- `TabData.m`: measures from the data
- `TabMod.m`: mean measures from the proposed model
- `TabRand.m`: mean measures from the data after randomisation
