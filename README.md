# BachelorThesis
This Repo contains my bachelor thesis paper and project files

## WIP! Estimated completion date: 12-31-2025

## Title: Investigating Neuroevolution of Ternary Neural Networks as an Alternative to Reinforcement Learning

## Motivation

AI systems are increasingly constrained by energy, latency, and deployment cost rather
than marginal gains on benchmarks. Ternary neural networks (TNNs) with weights in
{-1, 0, +1} address these constraints by shrinking model size, reducing memory traffic,
and replacing many floating-point multiplies with cheaper operations. However, training
TNNs is difficult: ternarization is non-differentiable, yielding zero gradients almost every-
where and undefined values at thresholds. Neuroevolution, e.g., evolutionary strategies
(ES) and genetic algorithms (GA), offers a gradient-free alternative that searches directly
in discrete weight spaces. This makes training TNNs with ES/GA a seemingly natural fit.
Moreover, the discretized parameterization induces a dramatically smaller search space
than full precision, which may accelerate exploration and improve the chances of finding
competent solutions under tight evaluation budgets.
This thesis asks whether TNNs evolved with ES/GA can match full-precision neural net-
works (FPNNs) evolved with the same ES/GA procedures under equal budgets. We fur-
ther ask whether TNNs under neuroevolutionary training can solve the same suite of tasks
that FPNNs can under identical conditions or whether there exist tasks for which ternar-
ization imposes a fundamental performance ceiling. We evaluate policy/value networks
on a curated set of Gymnasium environments spanning discrete and continuous actions
of varying difficulty. We compare performance (average return, success rate), sample ef-
ficiency (area under the learning curve, steps-to-threshold), stability across seeds, and
model size (number of parameters). In addition to neuroevolutionary comparisons, we
include a strong reinforcement learning baseline Proximal Policy Optimization (PPO) as
a reference for task solvability and attainable performance under dense-gradient training.
Our goal is to quantify the accuracy–efficiency trade-off of TNNs and identify regimes by
task, sparsity, and evolutionary hyperparameters where they outperform, match, or lag
full-precision counterparts.
