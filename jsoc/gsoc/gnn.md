# Graph Neural Networks - Summer of Code

Graph Neural Networks (GNNs) are deep learning models specifically designed for data structured as graphs, with feature vectors associated with both nodes and edges. They are an expanding research area, with applications spanning complex network analysis, relational reasoning, combinatorial optimization, molecule generation, and numerous other domains

[GraphNeuralNetworks.jl](https://github.com/CarloLucibello/GraphNeuralNetworks.jl) is a pure Julia package for GNNs equipped with many features. It implements common graph convolutional layers, with CUDA support and graph batching for fast parallel operations. There are a number of ways by which the package could be improved.

### Improving performance using sparse linear algebra 

Many graph convolutional layers can be expressed as non-materializing algebraic operations involving the adjacency matrix instead of the slower and more memory-consuming gather/scatter mechanism. We aim at to extend as far as possible and in a GPU-friendly way these *fused* implementations. The project will involve fixing some outstanding issues in CUDA.jl that are blocking sparse adjacency matrix support on GPU.

**Duration**: 350h.

**Expected difficulty**: hard.

**Expected outcome**: A noticeable performance increase for many graph convolutional operations.

### Support for AMGDPU and Apple Silicon

We currently support scatter/gather operation only on CPU and CUDA hardware. We aim to extend this to AMDGPU and Apple Silicon
leveraging KernelAbstractions.jl, AMDGPU.jl, and Metal.jl.

**Duration**: 175h.

**Expected difficulty**: medium.

**Expected outcome**: Graph convolution speedup for AMD GPU and Apple hardware, performance roughly on par with CUDA.

### Adding models and examples

As part of the documentation and for bootstrapping new projects, we want to add fully worked-out examples and applications of graph neural networks. We can start with entry-level tutorials and progressively introduce the reader to more advanced features. 

**Duration**: 175h.  

**Expected difficulty**: easy.  

**Expected outcome**: A few pedagogical and more advanced examples of graph neural network applications.

### Adding graph datasets

Provide Julia-friendly wrappers for common graph datasets in [`MLDatasets.jl`](https://github.com/JuliaML/MLDatasets.jl). Create convenient interfaces
for the Julia ML and data ecosystem. 

**Duration**: 175h.

**Expected difficulty**: easy.  

**Expected outcome**: A large collection of graph datasets easily available to the Julia ecosystem.

## Recommended Skills

Familiarity with graph neural networks and Flux.jl.

## Mentors 
[Carlo Lucibello](https://github.com/CarloLucibello) (author of [GraphNeuralNetworks.jl](https://github.com/CarloLucibello/GraphNeuralNetworks.jl)).
Feel free to contact us on the [Julia Slack Workspace](https://Julialang.slack.com/) or by opening an issue in the GitHub repo.
