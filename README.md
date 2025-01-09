# EPI Proof-of-Concept Code
Repository that shows code and policies used in the proof-of-concept treated in a recent paper published by the EPI Project [\[1\]](#references).


## Structure
This repository contains two large segments of example code:
1. [`policies/`](./policies/) contains eFLINT snippets that examplify policy used during the proof-of-concept; and
2. [`workflows/`](./workflows/) contains BraneScript snippets that encode the workflows that drove the work done during the proof-of-concept.

Conceptually, the first is used to constrain the system to prevent it from doing somethings undesirable; the second is used to drive it to make it do something useful.

See the respective folders for more information.


## License
The code presented here is licensed under the Apache 2.0 license. See [`LICENSE`](./LICENSE) for more details.


## References
\[1\] Müller, T.; Turner, R.; Amiri, S.; Allaart, C.; et al. (2025). _Optimizing clinical pathways with federated data._ Accepted.

\[2\] Turner, R.; Grunwald, P. (2023). _Safe Sequential Testing and Effect Estimation in Stratified Count Data._ Proceedings of The 26th International Conference on Artificial Intelligence and Statistic, in Proceedings of Machine Learning Research 206:4880-4893 Available from <https://proceedings.mlr.press/v206/turner23a.html>, with the original code corresponding this paper available in an [online repository](https://github.com/rosanneturner/safeSequentialTestingAISTATS2023), and uses code from the [safestats R-package](https://cran.r-project.org/web/packages/safestats/index.html).
