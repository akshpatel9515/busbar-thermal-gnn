# Busbar Thermal GNN Surrogate

Prediction of the temperature field of a Joule-heated busbar using a graph neural network trained on OpenFOAM conjugate heat-transfer simulations.

## Workflow

1. Generate parametric busbar geometry with Gmsh Python API.
2. Convert mesh to OpenFOAM with `gmshToFoam`.
3. Run CHT simulations with Joule heating using `chtMultiRegionFoam`.
4. Post-process temperature fields.
5. Convert results to PyTorch Geometric graphs.
6. Train and validate a GNN surrogate.
7. Deploy an interactive Gradio web application.

## Main folders

- `scripts/`: Gmsh geometry, OpenFOAM automation, post-processing, dataset creation
- `ml/`: GNN model, training, and evaluation
- `webapp/`: Gradio web application
- `openfoam_template/`: Base OpenFOAM case template
- `cases/`: Generated OpenFOAM simulation cases
- `gnn_dataset/`: Graph dataset created from simulation results

## Software

- OpenFOAM 2606
- Gmsh Python API
- PyTorch
- PyTorch Geometric
- Gradio

