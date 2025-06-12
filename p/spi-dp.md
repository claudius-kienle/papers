---
layout: default
title: "Shadow Program Inversion with Differentiable Planning: A Framework
        for Unified Robot Program Parameter and Trajectory Optimization"
authors:
  - id: benjamin_alt
    aff: [1,2,"*"]
  - id: claudius_kienle
    aff: [1,3,"*"]
  - id: darko_katic
    aff: [1,4]
  - id: rainer_jaekel
    aff: [1]
  - id: michael_beetz
    aff: [2]
aff:
  1: ArtiMinds
  2: AICOR
  3: IAS
  4: Stuttgart-HFT
  "*": Authors contributed equally to this paper
links:
  arxiv-id: "2409.08678"
teaser: 
    image: ./static/images/spi-dp/hybrid_spi_overview_pickandplace_for_journal.png
    caption: "SPI-DP optimizes robot programs (left, red) with respect to nearly arbitrary task objectives (Phi)."
abstract: |
    This paper presents Shadow Program Inversion with Differentiable Planning (SPI-DP), a novel first-order optimizer capable of optimizing robot programs with respect to both high-level task objectives and motion-level constraints.  To that end, we introduce Differentiable Gaussian Process Motion Planning for N-DoF Manipulators (dGPMP2-ND), a differentiable collision-free motion planner for serial N-DoF kinematics, and integrate it into an iterative, gradient-based optimization approach for generic, parameterized robot program representations. SPI-DP allows first-order optimization of planned trajectories and program parameters with respect to objectives such as cycle time or smoothness subject to e.g.  collision constraints, while enabling humans to understand, modify or even certify the optimized programs. We provide a comprehensive evaluation on two practical household and industrial applications.
reference: |
    @article{alt2024spidp,
          title={Shadow Program Inversion with Differentiable Planning: A Framework for Unified Robot Program Parameter and Trajectory Optimization}, 
          author={Benjamin Alt and Claudius Kienle and Darko Katic and Rainer Jäkel and Michael Beetz},
          year={2024},
          eprint={2409.08678},
          archivePrefix={arXiv},
          primaryClass={cs.RO},
          url={https://arxiv.org/abs/2409.08678}, 
    }
acknowledgement: This work was supported by the German Federal Ministry of Education and Research (grant 01MJ22003B), the DFG CRC EASE (CRC \#1320) and the EU project euROBIN (grant 101070596).
---
<section class="section">
    <div class="container is-max-desktop">

        <h2 class="title is-3">Cup Experiment</h2>
        <p>A robot program was optimized with <i>SPI-DP</i> to place a cup at four target poses on two shelf levels,
            using approach
            motions based on human demonstrations while avoiding collisions. All trials were collision-free, and the
            target pose was reached with a mean accuracy of 0.6 mm.</p>
        <div class="columns is-centered">

            <div class="column">
                <div class="content">
                    <!-- <img src="./static/images/exp-cup/2023-12-07 14-12-35-out.gif" /> -->
                    <video id="dollyzoom" autoplay controls muted loop playsinline height="100%">
                        <source src="./static/videos/spi-dp/exp1-cup/2023-12-07 14-12-35-out2.mp4" type="video/mp4">
                    </video>
                </div>
            </div>
            <div class="column">
                <div class="content">
                    <video id="dollyzoom" autoplay controls muted loop playsinline height="100%">
                        <source src="./static/videos/spi-dp/exp1-cup/2023-12-07 14-35-49-out2.mp4" type="video/mp4">
                    </video>
                </div>
            </div>

            <div class="column">
                <div class="content">
                    <video id="dollyzoom" autoplay controls muted loop playsinline height="100%">
                        <source src="./static/videos/spi-dp/exp1-cup/2023-12-07 14-47-16-out2.mp4" type="video/mp4">
                    </video>
                </div>
            </div>
            <div class="column">
                <div class="content">
                    <video id="dollyzoom" autoplay controls muted loop playsinline height="100%">
                        <source src="./static/videos/spi-dp/exp1-cup/2023-12-07 14-50-25-out2.mp4" type="video/mp4">
                    </video>
                </div>
            </div>

        </div>
        <h2 class="title is-3">Wineglass Experiment</h2>
        <p>
            The robot program for the cup experiment was optimized again for a wine glass and a changed gripper
            geometry, additionally optimizing the target pose of the transfer skill to minimize cycle time.
            <i>SPI-DP</i> optimization reduced motion length by
            2.8 cm on average and decreased cycle time by 40% while ensuring collision-free movements.
        </p>
        <div class="columns is-centered">

            <div class="column">
                <div class="content">
                    <!-- <img src="./static/images/exp-cup/2023-12-07 14-12-35-out.gif" /> -->
                    <video id="dollyzoom" autoplay controls muted loop playsinline height="100%">
                        <source src="./static/videos/spi-dp/exp2-wineglass/2023-12-15 16-21-00-out2.mp4" type="video/mp4">
                    </video>
                </div>
            </div>
            <div class="column">
                <div class="content">
                    <video id="dollyzoom" autoplay controls muted loop playsinline height="100%">
                        <source src="./static/videos/spi-dp/exp2-wineglass/2023-12-15 16-22-08-out2.mp4" type="video/mp4">
                    </video>
                </div>
            </div>

            <div class="column">
                <div class="content">
                    <video id="dollyzoom" autoplay controls muted loop playsinline height="100%">
                        <source src="./static/videos/spi-dp/exp2-wineglass/2023-12-15 16-22-56-out2.mp4" type="video/mp4">
                    </video>
                </div>
            </div>
            <div class="column">
                <div class="content">
                    <video id="dollyzoom" autoplay controls muted loop playsinline height="100%">
                        <source src="./static/videos/spi-dp/exp2-wineglass/2023-12-15 16-24-10-out2.mp4" type="video/mp4">
                    </video>
                </div>
            </div>

        </div>
        <h2 class="title is-3">Engine Block Experiment</h2>
        <p>
            This experiment evaluates the scalability of joint motion and task-level optimization in complex
            industrial robot programs using a poka-yoke quality assurance task. A UR5 robot arm performs
            force-controlled searches to locate holes on an engine block, with randomized offsets to simulate
            process noise. <i>SPI-DP</i> optimizes the robot's motions and task parameters, improving cycle
            time and success probability. After optimization, hole detection rates increased significantly, with a
            62% reduction in search duration, and motion-level optimization ensured collision-free movements.</p>
        <div class="columns is-centered">
            <div class="column">
                <div class="content"></div>
                <div class="content">
                    <h3 class="title is-4">Unoptimized</h3>
                    <video id="dollyzoom" autoplay controls muted loop playsinline height="100%">
                        <source src="./static/videos/spi-dp/exp3-motorblock/P1250255-out2.mp4" type="video/mp4">
                    </video>
                    <p>Hole 2 faster since directly missed</p>
                </div>
            </div>
            <div class="column">
                <div class="content"></div>
                <div class="content">
                    <h3 class="title is-4">Optimized</h3>
                    <video id="dollyzoom" autoplay controls muted loop playsinline height="100%">
                        <source src="./static/videos/spi-dp/exp3-motorblock/P1250256-out2.mp4" type="video/mp4">
                    </video>
                    <p>Hole 2 slower but found successfully</p>
                </div>
            </div>
        </div>
    </div>
    </div>
</section>
