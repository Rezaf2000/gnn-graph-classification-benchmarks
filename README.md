# Graph Neural Network Classification Benchmarks

A PyTorch Lightning and Hydra benchmark comparing graph neural networks on superpixel image graphs and Open Graph Benchmark datasets.

## Task and architectures

Graph classification maps a graph to a label or property. The upstream configurations compare GCN, GIN, GAT, and GraphSAGE. Experiments use hyperparameter search and repeat selected settings across random seeds; the table below reproduces their published README results.

## Repository map

| Path | Purpose |
| --- | --- |
| `src/` | Data modules, graph models, and training logic |
| `configs/` | Hydra experiment and hyperparameter configurations |
| `run.py` | Experiment entry point |
| `benchmarks/`, `notebooks/` | Benchmark and exploratory material |
| `tests/`, `requirements.txt` | Existing tests and dependencies |

## Upstream reported results

| Model | MNIST-sp75 | CIFAR10-sp100 | ogbg-molhiv |
| --- | ---: | ---: | ---: |
| GCN | 0.955 ± 0.014 | 0.518 ± 0.007 | 0.755 ± 0.019 |
| GAT | 0.976 ± 0.008 | 0.617 ± 0.005 | 0.751 ± 0.026 |
| GraphSAGE | 0.981 ± 0.005 | 0.629 ± 0.012 | 0.761 ± 0.025 |

The metrics and their standard deviations are reported by the original project; no experiments were rerun here. The [original README](UPSTREAM_README.md) contains the complete table and setup commands.

## Source and license

Based on and adapted from [ashleve/graph_classification](https://github.com/ashleve/graph_classification). The original documentation, source files, and [MIT license](LICENSE) are retained.