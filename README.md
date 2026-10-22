# DriveMind

**DriveMind: Mind-Evolving Belief Tracking for Closed-Loop Autonomous Driving**

Yan Shi, Kehua Chen, Jiarui Qi, Yihong Tang, Haicheng Liao, Yinhai Wang

NeurIPS 2026

  **[Project page](https://qijiarui20021031.github.io/DriveMind/)**

## Code coming soon

We are cleaning up the code and will release it here. Star or watch this repository to be notified.

Planned release:

- [ ] Multi-hypothesis belief tracker (hypothesis propagation, VLM scoring, resampling)
- [ ] Belief-conditioned diffusion controller
- [ ] Asynchronous fast-slow closed-loop agent for Bench2Drive (CARLA)
- [ ] Evaluation scripts and checkpoints

## About

MLLM-based drivers reason from scratch at every frame and commit to a single explanation of the scene. DriveMind instead keeps several natural-language hypotheses alive at once, scores them against each new observation, and resamples to maintain diversity, in the spirit of a particle filter. A slow VLM reasoner updates the belief at about 2 Hz while a fast diffusion controller generates trajectories at about 10 Hz conditioned on the latest belief.

On Bench2Drive, adding belief tracking to the same driving pipeline raises the Driving Score from 68.50 to 81.37 and the Success Rate from 41.36% to 54.09%, with the largest gains on ambiguous scenarios such as unsignalized intersections and oncoming-traffic interactions.

## Citation

```bibtex
@inproceedings{drivemind2026,
  title     = {DriveMind: Mind-Evolving Belief Tracking for Closed-Loop Autonomous Driving},
  author    = {Shi, Yan and Chen, Kehua and Qi, Jiarui and Tang, Yihong and Liao, Haicheng and Wang, Yinhai},
  booktitle = {Advances in Neural Information Processing Systems (NeurIPS)},
  year      = {2026}
}
```
