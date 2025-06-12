---
layout: default
title: "AI-based Framework for Robust Model-Based Connector Mating in Robotic Wire Harness Installation"
authors:
  - id: claudius_kienle
    aff: [1,4,"&dagger;"]
  - id: benjamin_alt
    aff: [2,4,"&dagger;"]
  - id: finn_schneider
    aff: [3,4]
  - id: tobias_pertlwieser
    aff: [3]
  - id: rainer_jaekel
    aff: [4]
  - id: rania_rayyes
    aff: [3]
aff:
  1: IAS
  2: AICOR
  3: IFL
  4: ArtiMinds
  "&dagger;": "Authors contributed equally to this paper"
links:
  arxiv-id: "2503.09409"
  video: https://youtu.be/Enpk2MVnIac
teaser: 
    image: ./static/images/appmutt/overview_image.svg
    caption: "Robotic mating of electrical connectors in a center console: Using our learned, neural model of the search-and-insertion strategy, the search pattern (bottom left, red) is optimized (green) to ensure robust installation with minimal temporal overhead."
abstract: |
  Despite the widespread adoption of industrial robots in automotive assembly, wire harness installation remains predominantly manual due to the intricate and fine-grained nature of connector mating.

  To address this challenge, we design a novel AI-based framework that automates cable connector mating by integrating force control with deep visuotactile learning. Our system optimizes search-and-insertion strategies using first-order optimization over a multimodal transformer architecture trained on visual, tactile, and proprioceptive data. Additionally, we design a novel automated data collection and optimization pipeline that minimizes the need for machine learning expertise. The framework optimizes robot programs that run natively on standard industrial controllers, permitting human experts to audit and certify them. Experimental validations on a center console assembly task demonstrate significant improvements in cycle times and robustness compared to conventional robot programming approaches.
reference: |
  @misc{kienle2025aibasedframeworkrobustmodelbased,
      title={AI-based Framework for Robust Model-Based Connector Mating in Robotic Wire Harness Installation}, 
      author={Claudius Kienle and Benjamin Alt and Finn Schneider and Tobias Pertlwieser and Rainer Jäkel and Rania Rayyes},
      year={2025},
      eprint={2503.09409},
      archivePrefix={arXiv},
      primaryClass={cs.RO},
      url={https://arxiv.org/abs/2503.09409}
  } 
acknowledgement: This work was supported by the German Ministry for Economic Affairs and Climate Action under grant 13IK026A.
---          
<section>
    <div class="container is-max-desktop">

        <!-- Paper video. -->
        <div class="columns is-centered">
            <div class="column is-four-fifths">
                <h2 class="title is-3">Video about Experiments</h2>
                <div class="publication-video">
                    <iframe src="https://www.youtube.com/embed/Enpk2MVnIac" frameborder="0"
                        allow="autoplay; encrypted-media" allowfullscreen></iframe>
                </div>
            </div>
        </div>
        <div class="columns is-centered" style="margin-top: 40px;">
            <div class="column is-12">
                <h2 class="title is-3">AI-based Framework for Visuotactile Connector Mating</h2>
                <img id="teaser" src="./static/images/appmutt/workflow.svg" />
                <p>
                    An initial robot program is created by the programmer using industry-standard tools ARTM (left).
                    During the ramp-up phase, the robot executes the program repeatedly with varying search
                    parameterizations. The resulting dataset is used to train MuTT,
                    a predictive visuotactile model of the robot and environment dynamics (center).
                    This model then serves as a predictor for the first-order optimizer SPI,
                    which generates parameters that optimize the program for robust and fast connector mating given
                    the
                    observed process variance and the current environment (right).
                </p>
            </div>
        </div>
        <!--/ Paper video. -->
    </div>
</section>


