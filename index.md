[Xiaoli Wang<sup>1</sup>](https://github.com/lily983){:target="_blank"}, [Sipu Ruan<sup>1</sup>](https://ruansp.github.io/){:target="_blank"}, [Xin Meng<sup>1</sup>](https://github.com/XinnMeng){:target="_blank"}, [Gregory Chirikjian<sup>1*</sup>](https://cde.nus.edu.sg/me/staff/chirikjian-gregory-s/){:target="_blank"}

<sup>1</sup>Department of Mechanical Engineering, National University of Singapore, Singapore

<sup>*</sup>Department of Mechanical Engineering, University of Delaware, USA

Published in __IEEE Robotics and Automation Letters (RA-L)__

## Abstract
Probabilistic collision detection (PCD) is essential in motion planning for robots operating in unstructured environments, where considering sensing uncertainty helps prevent damage. Existing PCD methods mainly use simplified geometric models and address only position estimation errors. This paper presents an enhanced PCD method with two key advancements: (a) using superquadrics for more accurate shape approximation and (b) accounting for both position and orientation estimation errors to improve robustness under sensing uncertainty. Our method first computes an enlarged surface for each object that encapsulates its observed rotated copies, thereby addressing the orientation estimation errors. Then, the collision probability is formulated as a chance-constraint problem that is solved with a tight upper bound. Both steps leverage the recently developed closed-form normal parameterized surface expression of superquadrics. Results show that our PCD method is twice as close to the Monte-Carlo sampled baseline as the best existing PCD method and reduces path length by 30% and planning time by 37%, respectively. A Real2Sim2Real pipeline further validates the importance of considering orientation estimation errors, showing that the collision probability of executing the planned path is only 2%, compared to 9% and 29% when considering only position estimation errors or no errors at all.

## Links
- [Paper](https://ieeexplore.ieee.org/document/9829274){:target="_blank"}
- Code: 
  - [Core C++ library](https://github.com/ChirikjianLab/cfc-collision.git){:target="_blank"}, [API documentation]({{site.baseurl}}/resources/doc/v0.1.0){:target="_blank"}: templated header-only library for collision detection algorithms
  - [ROS package](https://github.com/ChirikjianLab/cfc_collision_ros.git){:target="_blank"}: application in motion planning, including visualization
  - [MATLAB implementation](https://github.com/ChirikjianLab/cfc-collision-matlab.git){:target="_blank"}: MATLAB version for algorithms. It also includes visualizaions for figures in the paper and benchmark results from C++ implementations.

## Supplementary Video
<iframe width="640" height="340" src="https://www.youtube.com/embed/qcjZRinQ66k" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

## Citation
If you find our work useful in your research, please consider citing:

- S. Ruan, X. Wang and G. S. Chirikjian, "Collision Detection for Unions of Convex Bodies With Smooth Boundaries Using Closed-Form Contact Space Parameterization," in IEEE Robotics and Automation Letters, vol. 7, no. 4, pp. 9485-9492, Oct. 2022, doi: 10.1109/LRA.2022.3190629.

- BibTeX
```
@ARTICLE{ruan2022collision,
  author={Ruan, Sipu and Wang, Xiaoli and Chirikjian, Gregory S.},
  journal={IEEE Robotics and Automation Letters}, 
  title={Collision Detection for Unions of Convex Bodies With Smooth Boundaries Using Closed-Form Contact Space Parameterization}, 
  year={2022},
  volume={7},
  number={4},
  pages={9485-9492},
  doi={10.1109/LRA.2022.3190629}}
```
