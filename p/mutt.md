---
layout: default
title: "MuTT: A Multimodal Trajectory Transformer for Robot Skills"
authors:
  - id: claudius_kienle
    aff: [1]
  - id: benjamin_alt
    aff: [1]
  - id: onur_celik
    aff: [2]
  - id: philipp_becker
    aff: [2]
  - id: darko_katic
    aff: [1]
  - id: rainer_jaekel
    aff: [1]
  - id: gerhard_neumann
    aff: [2]
aff:
  1: ArtiMinds
  2: ALR
links:
  arxiv-id: "2407.15660"
abstract: |
  High-level robot skills represent an increasingly popular paradigm in robot programming.  However, configuring the skills' parameters for a specific task remains a manual and time-consuming endeavor.  Existing approaches for learning or optimizing these parameters often require numerous real-world executions or do not work in dynamic environments.

  To address these challenges, we propose MuTT, a novel encoder-decoder transformer architecture designed to predict environment-aware executions of robot skills by integrating vision, trajectory, and robot skill parameters.  Notably, we pioneer the fusion of vision and trajectory, introducing a novel trajectory projection.  Furthermore, we illustrate MuTT's efficacy as a predictor when combined with a model-based robot skill optimizer.

  This approach facilitates the optimization of robot skill parameters for the current environment, without the need for real-world executions during optimization.  Designed for compatibility with any representation of robot skills, MuTT demonstrates its versatility across three comprehensive experiments, showcasing superior performance across two different skill representations.
reference: |
  @article{kienle2024mutt,
      title={MuTT: A Multimodal Trajectory Transformer for Robot Skills},
      author={Kienle, Claudius and Alt, Benjamin and Celik, Onur and Becker, Philipp and Katic, Darko and J{\"a}kel, Rainer and Neumann, Gerhard},
      journal={arXiv preprint arXiv:2407.15660},
      year={2024}
  }
---