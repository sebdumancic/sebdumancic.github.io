---
layout: page
title: Probabilistic Programming Seminar
description: Research seminar on Probabilistic programming in the TU Delft's CS Master programme
img: 
importance: 1
category: course
---

## Description

Probabilistic programming languages (PPLs) use the syntax and semantics of programming languages to define probabilistic models. Using computer programs as a representation of probabilistic models yields two benefits. First, any computable process can be modelled as a probabilistic program. Second, PPLs enable a diverse audience -- data scientists, systems designers, medical doctors, etc. -- to design and reason about probabilistic systems. PPLs are becoming one of the central topics in probabilistic reasoning and programming languages, with increasing interest from industry and academia.

This course will:
  1. introduce the core ideas of probabilistic programming -- probabilistic inference, language design, and applications -- as well as state-of-the-art ideas in the field that make PPLs more reliable, usable, and faster. 
  2. teach you how to critically analyse state-of-the-art ideas, their strengths and weaknesses, and propose improvements.

At the end of the course, you will be able to:
  - read and write probabilistic programs
  - understand how probabilistic programming languages are implemented and how they can be extended
  - understand the basic and state-of-the-art probabilistic inference procedures (which are applicable beyond probabilistic programs)


## Prerequisites

The target audience for this course are Master's and PhD students. The are no formal prerequisites, but the students are expected to be comfortable with programming and mathematical notation. Basic familiarity with probability theory, artificial intelligence and machine learning is expected (equivalent to a Bachelor's level course).
We will not revise these topics during the lectures, but refresher materials are listed below.

## Course Format

The course will consist of lectures by the instructors, paper reviews, student presentations on research papers and a project. The points are distributed as follows:
 - 60%: Presentations and reviews. The points include:
    - one paper presentation (40% of the category), 
    - paper reviews and class participation (60%)
 - 40%: Project.  

**Paper reviews.** 
The course will take the format of a research seminar. 
This means that there will be no textbook and blackboard lectures; instead, we will be reading and discussing state of the art papers in the field. 
You are expected to read and review every paper before the class. 
The paper reviews will not be extensive: they consist of a few questions to answer regarding the main idea of the paper and are there to help you study. 

**Paper presentation.** 
You are expected to present one of the assigned papers. 
You will understand the paper in details, including searching for additional literature that helps you to understand the paper and why it works, and present it to your colleagues. 



**Class participation.** 
As this is a seminar course, you are expected to *actively participate* in class. 
You cannot pass the course by only submitting the reviews and the project without saying anything during lectures. 
See [how to do well in a seminar course.](#how-to-do-well-in-a-seminar-course) 

**Project.** 
The project will take the form of a competition. 
You compete in groups of 2 or 3 with the goal to write the fastest inference procedure for the given problems. 


For more details about the grading scheme, see [here](#grading-scheme).

## Schedule

The materials are split in two categories:
 - **Required literature**: these are the paper we cover in class. They form the mandatory literature. 
 - **If you want to know more**: these papers are not mandatory reading, but rather interesting references you can use to further study the topic. 

You do not have to read every paper from the required literature. 
You will be divided in groups (group split is on Brightspace) and each group reads only one paper for the class. 
You will learn about the other paper from the presentation of your colleagues.

Each lecture  comes with a reading guide. 
This guide explains what you should get from the papers (and what is perhaps not relevant!). 
Use it to focus your efforts on important stuff.
Of course, you are not discouraged to go into depths of every paper.

<style scoped>
table {
  font-size: 13px;
}
</style>
 Lecture <br> and presenters | Topic and readings | 
-----|:----------------------|
W1 L1 <br> September 5 <br><br> Sebastijan | **Topic** <br/> Introduction to probabilistic programming. Thinking generatively. What kind of problems can be solved with probabilistic programming? The anatomy of a probabilistic program. <br><a href="{{ 'teaching/probprog/Lecture1.pdf' | prepend: '/assets/pdf/' | prepend: site.baseurl | prepend: site.url }}">[Slides]</a> <br><br> **Required readings** (not before class) <br> Chapters 1-3 [Probabilistic  Models of Cognition](https://probmods.org/index.html) <br> Chapter 1 from [An introduction to probabilistic programming](https://arxiv.org/pdf/1809.10756.pdf) <br><br> **Reading guide** <br> Focus on model-based reasoning and how it contrasts to machine learning. Understand what 'thinking generatively' means and work out some examples. Understand how probabilistic programming differs from standard programming, how its key elements -- sample and observe -- influence its execution, and how to interpret the program as a density. | 
W1 L2 <br> September 8 <br><br> Sebastijan |  **Topic** <br/> Basic inference procedures: Enumeration, Rejection sampling, Importance sampling, Metropolis-Hastings MCMC, Particle filtering. Why do  they work? <br><a href="{{ 'teaching/probprog/Lecture2.pdf' | prepend: '/assets/pdf/' | prepend: site.baseurl | prepend: site.url }}">[Slides]</a> <br><br> **Required readings** <br> [Chapter 8](https://probmods.org/chapters/inference-algorithms.html) from [Probabilistic models of cognition](https://probmods.org) <br> Sections 4.1-4.3 from [An introduction to probabilistic programming](https://arxiv.org/pdf/1809.10756.pdf) <br><br> **Reading guide** <br> ProbMods chapter will give you nice intuition of the inference algorithms. Focus on understanding the role of sample and observe statements in each inference algorithm. Introduction to ProbProg chapter will formally describe all the algorithms. Directly connect the algorithms to how we interpret programs as densities, and why do they work. While reading this chapter, ignore the parts about inference on graphs, Aside notes, Addressing transformation, and section 4.3.5.  |   
W2 L3 <br> September 12 <br><br> | No lecture. Read papers for the next one.   | 
W2 L4 <br> September 15 <br><br> Group discussion | **Topic**<br/> How do we implement probabilistic programs?  <br/><br/> **Required literature**<br> [C3: Lightweight Incrementalized MCMC for Probabilistic Programs using Continuations and Callsite Caching](https://arxiv.org/pdf/1509.02151.pdf) <br> [Lightweight Implementations of Probabilistic Programming Languages Via Transformational Compilation](http://proceedings.mlr.press/v15/wingate11a/wingate11a.pdf) <br> Sections 6.1, 6.4-6.7 from [An introduction to probabilistic programming](https://arxiv.org/pdf/1809.10756.pdf) <br> <br> **Reading guide**<br> Distill the main idea and  don't get stuck on implementation details if the paper discusses it (e.g., data structures used, etc.). What is the main computational (program execution/transformation) principle? Why is it useful? How does it interact with the sample and observe statements? Build up one of the inference algorithms in all 3 paradigms. <br><br>**If you want to know more**<br/>[Design and Implementation of Probabilistic Programming Language Anglican](https://dl.acm.org/doi/10.1145/3064899.3064910)<br/>[Gen: a general-purpose probabilistic programming system with programmable inference](https://dl.acm.org/doi/pdf/10.1145/3314221.3314642) <br> [DynamicPPL: Stan-like Speed for Dynamic Probabilistic Models](https://arxiv.org/pdf/2002.02702.pdf) <br> [A New Approach to Probabilistic Programming Inference](https://arxiv.org/pdf/1507.00996.pdf) <br> [Functional Programming for Modular Bayesian Inference](https://www.denotational.co.uk/publications/scibior-kammar-ghahramani-funcitonal-programming-for-modular-bayesian-inference.pdf) <br/>[MiniPyro](https://pyro.ai/examples/minipyro.html)  | 
W3 L5 <br> September 19 <br><br> Gautham <br> Jaap  | **Topic**<br/>  How do we automatically improve the performance of PPs through rewrites? <br/><br/> **Required literature**<br/>[R2: An Efficient MCMC Sampler for Probabilistic Programs](https://sf.snu.ac.kr/publications/r2.pdf) [[Review form]](#w3-l5-p1) <a href="{{ 'teaching/probprog/2022-2023/ProbProg-R2.pdf' | prepend: '/assets/pdf/' | prepend: site.baseurl | prepend: site.url }}">[Slides]</a> <br/> [Automatic Reparameterisation of Probabilistic Programs](https://proceedings.mlr.press/v119/gorinova20a/gorinova20a.pdf) [[Review form]](#w3-l5-p2) <a href="{{ 'teaching/probprog/2022-2023/W3L5.pdf' | prepend: '/assets/pdf/' | prepend: site.baseurl | prepend: site.url }}">[Slides]</a> <br><br> **Reading guide**<br> Focus on understanding the transformations. Ignore the references to specific inference algorithms, unless the algorithm is one mentioned in W1L2. You can skip the proofs, and glance over things like ELBO (which we cover later). Do the transformations affect sample or observe statements? In which way? Give an example how the transformation improves inference.  <br/><br/> **If you want to know more**<br/> [Slicing Probabilistic Programs](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/slicing.pdf) <br/>   [A Provably Correct Sampler for Probabilistic Programs](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/final.pdf) <br> [Coarse-to-Fine Sequential Monte Carlo for Probabilistic Programs](https://arxiv.org/pdf/1509.02962.pdf) <br/> [Incremental Inference for Probabilistic Programs](https://dl.acm.org/doi/pdf/10.1145/3296979.3192399) <br/>[Conditional independence by typing](https://arxiv.org/pdf/2010.11887.pdf)  <br> [Generating Efficient MCMC Kernels from Probabilistic Programs](http://proceedings.mlr.press/v33/yang14d.pdf) <br><br> **Additional resources that can help you** <br> [Weakest precondition analysis](https://www.cs.williams.edu/~freund/cs326/ReasoningPart1.html#summary-so-far-rules-for-finding-the-weakest-precondition) | 
W3 L6 <br> September 22 <br> <br>Jord<br> Wei| **Topic**<br> Hamiltonian Monte Carlo -- better inference  through gradient estimation <br/><br/> **Required literature**<br/>  [Automatic differentiation and Machine Learning: A Survey](https://www.jmlr.org/papers/volume18/17-468/17-468.pdf). [[Review form]](#w3-l6-p1)  <a href="{{ 'teaching/probprog/2022-2023/automatic_differentiation_jord .pdf' | prepend: '/assets/pdf/' | prepend: site.baseurl | prepend: site.url }}">[Slides]</a> <br> [Pattern Recognition and Machine Learning, Chapter 11.5](https://www.microsoft.com/en-us/research/uploads/prod/2006/01/Bishop-Pattern-Recognition-and-Machine-Learning-2006.pdf) [[Review form]](#w3-l6-p2)  <br><br> **Reading guide**<br> When reading about HMC, focus on understanding the intuition of the approach and then go to the math. Make sure you understand why this is a good idea. Make sure you understand what each of the two steps brings to the table. For automated differentiation, understand the properties of each of the modes and pay attention how to implement them.    <br/><br/> **If you want to know more** <br/>[The No-U-Turn Sampler: Adaptively Setting Path Lengths in Hamiltonian Monte Carlo](http://www.stat.columbia.edu/~gelman/research/published/nuts.pdf) <br/>  [Faster Hamiltonian Monte Carlo by Learning Leapfrog Scale](https://arxiv.org/abs/1810.04449) <br> [Generating Design Suggestions under Tight Constraints with Gradient-based Probabilistic Programming](https://dritchie.github.io/pdf/hmc.pdf) <br/> [Nonparametric Hamiltonian Monte Carlo](http://proceedings.mlr.press/v139/mak21a/mak21a.pdf) <br> [MCMC using Hamiltonian dynamics](https://arxiv.org/pdf/1206.1901.pdf)  <br><br>  **Other materials that could help you better understand the topic**<br> [A  conceptual introduction to Hamiltonian Monte Carlo](https://arxiv.org/pdf/1701.02434.pdf) <br/> [Simple HMC implementation](https://github.com/ColCarroll/minimc) <br/> [Building a better Markov Chain](https://elevanth.org/blog/2017/11/28/build-a-better-markov-chain/) <br> [Probabilistic programming under the hood](https://willcrichton.net/notes/probabilistic-programming-under-the-hood/) <br> [Differentiation for Hackers](https://github.com/MikeInnes/diff-zoo) <br> [Build your own automated differentiation program](https://towardsdatascience.com/build-your-own-automatic-differentiation-program-6ecd585eec2a) <br> [Alan Maloney's HMC for Dummies](https://www.youtube.com/watch?v=ZGtezhDaSpM) | 
W4 L7 <br> September 26 <br><br> Calin <br> Mark | **Topic**<br/> Scaling up inference by surrogate distributions <br/><br/> **Required literature**<br/>[Automated Variational Inference in Probabilistic Programming](https://arxiv.org/pdf/1301.1299.pdf) [[Review form]](#w4-l7-p1) <a href="{{ 'teaching/probprog/2022-2023/W4L7p1.pdf' | prepend: '/assets/pdf/' | prepend: site.baseurl | prepend: site.url }}">[Slides]</a>  <br/>[Automatic Variational Inference in Stan](https://papers.nips.cc/paper/2015/file/352fe25daf686bdb4edca223c921acea-Paper.pdf) [[Review form]](#w4-l7-p2) <a href="{{ 'teaching/probprog/2022-2023/W4L7p2.pdf' | prepend: '/assets/pdf/' | prepend: site.baseurl | prepend: site.url }}">[Slides]</a>  <br><br> **Reading guide**<br> Variational inference is an important topics when we think about scaling probabilistic inference to large real world problems. Make sure to understand what does variational inference exactly do; if stuck, check Bishop's textbook. For the papers you are reading, focus on understanding what are they trying to achieve, how do they manage to automatically derive variational distributions from a program. Why do they do it in this way?  <br/><br/>**If you want to know more**<br/> [Variational Inference: A Review for Statisticians](https://arxiv.org/pdf/1601.00670.pdf) <br> [Stochastic Variational Inference](https://www.jmlr.org/papers/volume14/hoffman13a/hoffman13a.pdf) <br>[Automatic Differentiation Variational Inference](https://arxiv.org/pdf/1603.00788.pdf) <br/>  [Towards Verified Stochastic Variational Inference for Probabilistic Programs](https://arxiv.org/pdf/1907.08827.pdf). <br><br> **Additional materials that could help you better understand the topic**<br>  [David Blei's lecture on the foundations of variational inference](https://www.youtube.com/watch?v=ogdv_6dbvVQ) <br> [Variational inference from scratch](https://www.ritchievink.com/blog/2019/09/16/variational-inference-from-scratch/) |  
W4 L8 <br> September 29 <br><br> Siert <br>Konstantinos | **Topic**<br/> Reusing previous inferences to speed up future ones  <br/><br/> **Required literature**<br/>[Deep Amortized Inference for Probabilistic Programs](https://arxiv.org/pdf/1610.05735.pdf) [[Review form](#w4-l7-p1)] <br/> [Inference Compilation and Universal Probabilistic Programming](https://arxiv.org/pdf/1610.09900.pdf) [[Review form](#w4-l7-p2)]<br><br> **Reading guide**<br> <br><br> **If you want to know more**<br> [Amortized Rejection Sampling in Universal Probabilistic Programming](https://proceedings.mlr.press/v151/naderiparizi22a/naderiparizi22a.pdf) <br> [Accelerating Metropolis-Hastings with Lightweight Inference Compilation](http://proceedings.mlr.press/v130/liang21a/liang21a.pdf)  | 
W5 L9 <br> October 3 <br><br> Lucas <br>Matei | **Topic**<br/> Programmable inference  <br/><br>  **Required literature**<br> [Probabilistic programming with programmable inference](https://www.cantab.net/users/yutian.chen/Publications/MansinghkaEtAl_pldi18.pdf) [[Review form](#w5-l9-p1)] <br> [Using probabilistic programs as proposals](https://arxiv.org/pdf/1801.03612.pdf) [[Review form](#w5-l9-p2)] <br><br> **Reading guide**<br> So far, we have looked into monolithic inference procedures. We have also seen that we have so many of them because there is no perfect one. In this lecture, we focus on techniques that make it possible to utilise the strengths of several inference procedures for the same problem. When reading these papers, focus on the new aspects they bring and the aspects that could not be done with inference procedures we looked ata so far. Try to understand the theorems, but don't bother with proofs.   <br><br> **If you want to know more** <br> [Learning Proposals for Probabilistic Programs with Inference Combinators](https://arxiv.org/pdf/2103.00668.pdf) <br> [Gen: a general-purpose probabilistic programming system with programmable inference](https://dl.acm.org/doi/pdf/10.1145/3314221.3314642)  <br> [Venture: a higher-order probabilistic programming platform with programmable inference](https://arxiv.org/pdf/1404.0099.pdf) | 
W5 L10 <br> October 6 <br><br> Martin <br> Marije | **Topic**<br/> Simulation-based inference <br><br> **Required literature** <br> [Efficient Probabilistic Inference in the Quest for Physics Beyond the Standard Model](https://proceedings.neurips.cc/paper/2019/file/6d19c113404cee55b4036fce1a37c058-Paper.pdf) [[Review form](#w5-l10-p1)] <br> [Planning as Inference in Epidemiological Models](https://arxiv.org/pdf/2003.13221.pdf) [[Review form](#w5-l10-p2)] <br><br> **Reading guide**<br> When reading these papers focus on (1) understanding why probabilistic programming is a suitable paradigm for this task, (2) which kind of inference techniques were used, and (3) what are the challenges in applying probabilistic programming to simulators. For the second paper on epidemiological models, you don't have to read the entire paper; use your judgement to identify the important parts.  <br><br> **If you want to know more**<br> [The frontier of simulation-based inference](https://arxiv.org/pdf/1911.01429.pdf) <br> [Modeling Expectation Violation in Intuitive Physics with Coarse Probabilistic Object Representations](http://physadept.csail.mit.edu/papers/adept.pdf) <br> [Etalumis: Bringing Probabilistic Programming to Scientific Simulators at Scale](https://par.nsf.gov/servlets/purl/10169392) <br> [Simulation Intelligence: Towards a New Generation of Scientific Methods](https://arxiv.org/pdf/2112.03235.pdf) <br> [Coping With Simulators That Don’t Always Return](http://proceedings.mlr.press/v108/warrington20a/warrington20a.pdf) <br> [Probabilistic Surrogate Networks for Simulators with Unbounded Randomness](https://arxiv.org/pdf/1910.11950.pdf)  | 
W6 L11 <br> October 10 <br><br> Sneha <br> Reuben | **Topic**<br/> How to efficiently handle traces with stochastic support? <br/><br/> **Required literature**<br/>[Automating Involutive MCMC using Probabilistic and Differentiable Programming](https://arxiv.org/pdf/2007.09871.pdf) [[Review form](#w6-l11-p1)] <br/> [Divide, Conquer, and Combine: a New Inference Strategy for Probabilistic Programs with Stochastic Support](https://arxiv.org/pdf/1910.13324.pdf) [[Review form](#w6-l11-p2)] <br><br> **Reading guide**<br> Focus on the key idea how these two technqiues make it possible to easily switch between traces with different number of stochastic choices. Skip, or skim, the measure theoretic stuff in the first paper.  |  
W6 L12 <br> October 13 <br><br> Dāvis  | **Topic**<br/> Alternative paradigms of probabilistic programming -- probabilistic logic programming <br/><br/> **Required literature**<br/> [ProbLog: A Probabilistic Prolog and its Application in Link Discovery](https://dtai.cs.kuleuven.be/publications/files/42447.pdf) [[Review form](#w6-l12-p1)] <br/> [k-Optimal: A novel approximate inference algorithm for Problog](https://lirias.kuleuven.be/retrieve/190816) [[Review form](#w6-l12-p2)]<br><br> **Reading guide**<br> In the next two lectures, we will explore some alternative paradigm in probabilistic programming. You should focus on what do these new paradigm do differently than the techniques we have seen so far, what are the assumptions and deisign choices they make. Reading the [Section 3 and 3.1 from simply Logical](https://book.simply-logical.space/src/text/1_part_i/3.0.html) before will make the papers more understandable. What do these paradigm bring to the probabilistic programming scene?   <br/><br/>**If you want to know more**<br/> [Inference in Probabilistic Logic Programs using Weighted CNFs](https://arxiv.org/pdf/1202.3719.pdf) <br> [Probabilistic (Logic) Programming Concepts](https://lirias.kuleuven.be/bitstream/123456789/490338/1/deraedt_kimmig_mlj15.pdf) <br/> [MCMC Estimation of Conditional Probabilities in Probabilistic Programming Languages](https://lirias.kuleuven.be/bitstream/123456789/411248/1/mcmc.pdf) <br/> [DeepProbLog: Neural Probabilistic Logic Programming](https://lirias.kuleuven.be/retrieve/550383/) <br> [Generative modeling by PRISM](https://rjida.meijo-u.ac.jp/reference/Sato-ICLP09.pdf) <br> [Stochastic Logic Programs: Sampling, Inference and Applications](https://arxiv.org/pdf/1301.3846.pdf#:~:text=A%20stochastic%20logic%20program%20(SLP,1996%3B%20Cussens%2C%201999).) <br> [BLOG: Probabilsitic Models with Unknown Objects](https://people.eecs.berkeley.edu/~russell/papers/srlbook-blog.pdf) <br> [PSI: Exact Symbolic Inference for Probabilistic Programs](https://files.sri.inf.ethz.ch/website/papers/psi-solver.pdf) <br> [Static Analysis for Probabilistic Programs: Inferring Whole Program Properties from Finitely Many Paths](https://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.360.1462&rep=rep1&type=pdf) <br/> [Nonstandard Interpretations of Probabilistic Programs for Efficient Inference](https://stuhlmueller.org/papers/nonstandard-interpretations-nips2011.pdf) | 
W7 L13 <br> October 17<br><br> Sara <br> Raphaël  | **Topic**<br/> Alternating paradigms of probabilistic programming -- Deep generative models <br><br> **Required readings**<br> [Variational Autoencoders](https://arxiv.org/pdf/1606.05908.pdf) [[Review form](#w7-l13-p1)] <br> [Variational Inference with Normalising Flows](https://arxiv.org/pdf/1505.05770.pdf) [[Review form](#w7-l13-p2)] <br><br> **Reading guide**<br> Deep generative models are not technically probabilistic programming paradigm, but it follows some of the same idea -- they focus on modelling generative processes. When reading these papers, focus on understanding a  different perspective these approaches take towards generative modelling, how is probability interpreted, and what can they do that probabilistic programs can't (and vice versa!)..  <br><br> **If you want to know more**<br> [Deep Generative Modelling](https://link.springer.com/book/10.1007/978-3-030-93158-2) <br> [Normalizing Flows for Probabilistic Modeling and Inference](https://jmlr.org/papers/volume22/19-1028/19-1028.pdf) <br> [Simple, Distributed, and Accelerated Probabilistic Programming](https://proceedings.neurips.cc/paper/2018/file/201e5bacd665709851b77148e225b332-Paper.pdf) |
W7 L14 <br> October 20 <br><br> Guest lecture by [Steven Holtzen](https://www.khoury.northeastern.edu/home/sholtzen/) | **Topic**<br/> Discrete Probabilistic Programming <br/><br/>  **Required literature**<br/> [On probabilistic inference by weighted model counting](https://www.sciencedirect.com/science/article/pii/S0004370207001889) [[Review form](#w7-l14-p1)] <br/> **Lecture will be based on this paper:** <br> [Scaling Exact Inference for Discrete Probabilistic Programs](https://arxiv.org/pdf/2005.09089.pdf) <br><br> **Reading guide**<br>This week you will read more about weighted model counting, a technique we have already touched upon with Problog. WMC is also a technique on which today's guest lecture is heavily based on. You don't have to read the entire paper for the lecture; it is quite a long one. What you should aim to understand what the technique is and how it is used to perform probabilistic inference. you don't have to understand the construction algorithms and other things.  <br/> <br/>**If you want to know more**<br/>[Algebraic Model Counting](https://arxiv.org/pdf/1211.4475.pdf) <br/> [SPPL: Probabilistic Programming with Fast Exact Symbolic Inference](https://arxiv.org/pdf/2010.03485.pdf)  |
W8 L15 <br> October 24 <br><br> Cristian <br> Balazs <br> Farhad | **Topic**<br/> Cool applications and powerful inference procedures <br/><br/> **Required literature**<br/>[3DP3: 3D Scene Perception via Probabilistic Programming](https://arxiv.org/pdf/2111.00312.pdf) [[Review form]](#w8-l15-p1)  <br/> [Inferring Signaling Pathways with Probabilistic Programming](https://arxiv.org/pdf/2005.14062.pdf)  [[Review form]](#w8-l15-p2) <br> [A Language for Counterfactual Generative Models](http://proceedings.mlr.press/v139/tavares21a/tavares21a.pdf)  <br><br> **Reading guide**<br> When reading these papers, focus on what does every element of a probabilistic program represents (e.g., priors, likelihood, posteriors, observations). It is not necessary that you understand all the math. <br/><br/> **If you want to know more:** <br/> [Etalumis: Bringing Probabilistic Programming to Scientific Simulators at Scale](https://arxiv.org/pdf/1907.03382.pdf) <br/> [Alexandria: Unsupervised High-Precision Knowledge Base Construction using a Probabilistic Program](https://openreview.net/pdf?id=rJgHCgc6pX) <br/> [Semantic Parsing to Probabilistic Programs for Situated Question Answering](https://arxiv.org/pdf/1606.07046.pdf) <br/> [PClean: Bayesian Data Cleaning at Scale with Domain-Specific Probabilistic Programming](https://arxiv.org/pdf/2007.11838.pdf) |  
W8 L16 <br> October 27 <br><br>  Guest lecture by [Tom Rainforth](https://www.robots.ox.ac.uk/~twgr/) | **Nested Probabilistic Programs and Target Aware Inference and Expectation Programming** <br/> We formalize the notion of nesting probabilistic programming queries and investigate the resulting statistical implications. We demonstrate that while query nesting allows the definition of models which could not otherwise be expressed, such as those involving agents reasoning about other agents, existing systems take approaches which lead to inconsistent estimates. We show how to correct this by delineating possible ways one might want to nest queries and asserting the respective conditions required for convergence. We further introduce a new online nested Monte Carlo estimator that makes it substantially easier to ensure these conditions are met, thereby providing a simple framework for designing statistically correct inference engines. We prove the correctness of this online estimator and show that, when using the recommended setup, its asymptotic variance is always better than that of the equivalent fixed estimator, while its bias is always within a factor of two <br/><br/> **Target Aware Inference and Expectation Programming** <br/> Standard approaches for Bayesian inference focus solely on approximating the posterior distribution. Typically, this approximation is, in turn, used to calculate expectations for one or more target functions—a computational pipeline that is inefficient when the target function(s) are known upfront. We address this inefficiency by introducing a framework for target–aware Bayesian inference (TABI) that estimates these expectations directly. While conventional Monte Carlo estimators have a fundamental limit on the error they can achieve for a given sample size, our TABI framework is able to breach this limit; it can theoretically produce arbitrarily accurate estimators using only three samples, while we show empirically that it can also breach this limit in practice. We utilize our TABI framework by combining it with adaptive importance sampling approaches and show both theoretically and empirically that the resulting estimators are capable of converging faster than the standard (1/N) Monte Carlo rate, potentially producing rates as fast as (1/N2). We further combine our TABI framework with amortized inference methods, to produce a method for amortizing the cost of calculating expectations. Finally, we show how TABI can be used to convert any marginal likelihood estimator into a target-aware inference scheme and demonstrate the substantial benefits this can yield. | 
-----|-------------------|



## Other materials


### Additional materials 

The course does not have a required textbook, it instead relies on selected papers. Some materials that might help you better understand probabilistic programming:
  - [Probabilistic Models of Cognition](https://probmods.org/index.html): the book uses probabilistic programs to formulate models of human cognition. The book is a great introduction to using probabilistic programming and contains plenty of example to practice your modelling skills.
  - [The Design and Implementation of Probabilistic Programming Languages](http://dippl.org/): a high-level book covering the basic inference procedures.
  - [An Introduction to Probabilistic Programming](https://arxiv.org/pdf/1809.10756.pdf): a work-in-progress introductory textbook. Covers many topics of the course. Very good introduction to basic inference procedures, implementation strategies, and variational inference.
  - [Statistical Relational Artificial Intelligence: Logic, Probability, and Computation](https://www.morganclaypool.com/doi/10.2200/S00692ED1V01Y201601AIM032): a high-level introduction to various paradigms of probabilistic logic programming.
  - [Foundations of Probabilistic Logic Programming](http://mcs.unife.it/~friguzzi/plp-book.html): a deeper introduction to probabilistic logic programming.
  - [Types and programming languages](https://www.cis.upenn.edu/~bcpierce/tapl/): good introduction to foundations of programming languages.
  - [Probabilistic Programming and Bayesian Methods for Hackers](https://github.com/CamDavidsonPilon/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers): an easy to follow book, great at explaining key ideas intuitively.

### Additional topics

Probabilistic programming is rapidly developing field. There are many topics we will not be able to cover in the class. Here is a snapshot of such topics, if you want to know more:
  - Other inference tasks: The inference task we look at was the characterisation of the posterior distribution. What if we are interested in other tasks, e.g., maximising the posterior? 
    - [Bayesian Optimization for Probabilistic Programs](https://proceedings.neurips.cc/paper/2016/file/31fefc0e570cb3860f2a6d4b38c6490d-Paper.pdf)
    - [Expectation Programming: Adapting Probabilistic Programming Systems to Estimate Expectations Efficiently](https://arxiv.org/pdf/2106.04953.pdf)
  - Learning probabilsitic programs: a standard PP pipeline focuses on inference; but what if we don't know the program?
    - [Human-level concept learning through probabilistic program induction](https://www.science.org/doi/epdf/10.1126/science.aab3050)
    - [Bayesian Synthesis of Probabilistic Programs for Automatic Data Modeling](https://arxiv.org/pdf/1907.06249.pdf)
    - [Neural Sketch Learning for Conditional Program Generation](https://arxiv.org/pdf/1703.05698.pdf)
  - Semantics of probabilistic programming languages: how to define the meaning of a probabilistic program?
    - [Semantics of Probabilistic Programming: A Gentle Introduction](https://www.cambridge.org/core/books/foundations-of-probabilistic-programming/semantics-of-probabilistic-programming-a-gentle-introduction/A7964205E44B5234A78C661192E294E1)
    - [Semantics for probabilistic programming: higher-order functions, continuous distributions, and soft constraints](https://arxiv.org/pdf/1601.04943.pdf)
    - [Semantics of Probabilistic programs](https://www.cs.cornell.edu/~kozen/Papers/ProbSem.pdf)
  - Deep generative models: an alternative framework for generative modelling based on neural networks. It has less flexibility than PPL but better learning properties.
    - [Deep Generative Modelling](https://link.springer.com/book/10.1007/978-3-030-93158-2)
  - Analysis of probabilistic programs:
    - [Conditional independence by typing](https://arxiv.org/pdf/2010.11887.pdf)
    - [Probabilistic Termination: Soundness, Completeness, and Compositionality](https://dl.acm.org/doi/pdf/10.1145/2676726.2677001)
  - Nested probabilistic programs: probabilistic programs that call probabilistic programs
    - [Nesting probabilistic programs](https://arxiv.org/pdf/1803.06328.pdf)
    - [Reasoning about reasoning by nested conditioning: Modeling theory of mind with probabilistic programs](https://www.sciencedirect.com/science/article/pii/S1389041713000387)
    - [On the Pitfalls of Nested Monte Carlo](https://arxiv.org/pdf/1612.00951.pdf)
  - Stochastic conditioning: in the course, the observations always came in form of the exact value of a variable. What if we want to condition on a distribution?
    - [Probabilistic Programs with Stochastic Conditioning](https://arxiv.org/pdf/2010.00282.pdf) 
  - Deep probabilistic programming: we have touched upon various interaction between probabilistic programming and deep neural networks. Deep probabilistic programming is a paradigm that combines the two, often with murky boundaries from e.g. variational or amortised inference.
    - [Neural probabilistic logic programming](https://www.sciencedirect.com/science/article/pii/S0004370221000552)
    - [Deep Probabilistic Programming](https://arxiv.org/abs/1701.03757?context=cs.PL)

### Courses at other universities
  - [Probabilistic programming](https://www.cs.ubc.ca/~fwood/CS532W-539W/) by Frank Wood at University of British Columbia, Canada
  - [seminar course](https://www.khoury.northeastern.edu/home/sholtzen/CS7480Fall21/) by Steven Holtzen at Northeastern, USA
  - [seminar course](https://docs.google.com/document/d/1MJXs0OdUS9sVL3LjTfEFK6i-Jz06cAKG21N_auE85wM/pub) by Dan Roy at University of Toronto, Canada, which focuses on theoretical aspects of probabilistic programming
  - [Deep Probabilistic Programming course](https://github.com/aleatory-science/deep-probprog-course) by  Thomas Hamelryck and Ahmad Salim Al-Sibahi at University of Copenhagen, Denmark
  - [Probabilistic Programming Languages course](https://www.cs.tufts.edu/comp/150PP/) by Norman Ramsey at Tufts University, USA
  - [Probabilistic Programming and Relational Learning](http://web.cs.ucla.edu/~guyvdb/teaching/cs267a/2022s/) bu Guy Van den Broeck at UCLA, USA.
  - [Probabilistic Programming course](https://github.com/hongseok-yang/probprog17) by Hongseok Yang at KAIST, South Korea




## Practicalities 

### How to do well in a seminar course

A seminar course is different from a standard course in two ways: (1) "just" learning the topics covered by the materials is not enough; and (2)  you are expected to actively participate in the lectures.
The active participation includes giving a presentation (see [Preparing your presentation](#preparing-you-presentation)) and discussing the materials during the lecture. Actually, the lectures will consist only of these two activities.
The exceptions are week 1, which contain two lectures by the instructor, and week 2, in which we discuss papers but no one has to prepare the presentation.
Each student will present one paper and is expected to actively contribute in discussions.


If understanding the materials is not enough, what is?
In a seminar course, we teach you to think beyond what you have been served. 
In fact, if you only master the materials, that will get you a mere 6.
Instead, you are expected to critically analyse every paper you read. 
For every paper you read, think about the following questions:
 - What is the main idea proposed in the paper?
 - Which problem does it solve?
 - What are its strengths?
 - What are its weaknesses?
 - Which parts of the paper were/and perhaps still are confusing to you?
 - Do you have an impression that the idea works just because the authors made some particular choices?
 - What are the implicit assumption the authors are making?
 - Do you see multiple options to solve a subproblem X and are wondering why the authors chose 
 - Is the idea properly evaluated? If not, what is missing? How would you do it?
 - Are the arguments for the idea convincing?
 - How would you extend the work?

During the discussion part of the lectures, we will discuss these questions and compare your observation.
Not all questions are applicable to every paper, so don't worry if you cannot relate some of them to some papers.
The quality of the discussion will therefore depend on you.
Importantly, you have to come prepared for each lecture.





It is important that you actively participate in the discussion. 
As a rule of thumb, the more you talk, the higher your grade will be in the end. 
However, *be constructive* and avoid saying something just to say something.
I don't want you to be quiet the entire quarter, but that does not mean that you have to say something in every discussion.
Sometimes you would have something brief to say, sometimes you would have some deeper insight. 
That is fine.
As a rule of thumb, I expect you to say something at least every few lectures.
Don’t be upset if I respond to you or even correct you.
For most of you, this is the first time you are participating in a seminar. 
It is expected that you need some guidance.
Moreover, I tend to jump in when you mention something interesting without (perhaps) realising it. 







An important difference between a regular course and a seminar is that you will not be penalised for not understanding something. 
That does not mean that this is a free-pass course, but rather that it is ok to build up towards an understnading during the course.
You will be reading research papers, often in depth.  
In contrast to textbooks, research papers are concise and expect certain knowledge from a reader. 
This has two consequence. 
First,  it is likely that you will not know some of the necessary concepts and would have to fill the gap to understand the paper. 
You should go through that process. 
Second, scientists are often not great writers -- they might explain simple concepts very confusingly because they have different audience in mind (peers, not students).
For any of these reasons, you might not understand a part of the paper. 
This is normal and you should not hide it -- confusing parts of the paper are great starters for discussions!




Here are a few situations that are acceptable in a seminar course, but perhaps not in a regular course:
 1. You misunderstand something in a paper and provide a wrong answer in a review. If you realise that during the lecture, you can correct you answer after the lecture. That is fine.
 2. You misunderstand something that leads you to an interesting idea for an extension. This is perfectly fine if your reasoning taking the misunderstanding as a fact is correct and interesting.
 3. You just can't understand what the paper is trying to say. Voice it in the lecture! Try to phrase it as a detailed question; point out as specifically as possible where you lost it




### Grading scheme

The tables below lists the expected competences for passing grades.
the descriptions are cummulative; e.g., expectations for the grade 8 also include expectations for grades 6 and 7. 


**Project**

<style scoped>
table {
  font-size: 13px;
}
</style>
**Grade** | **Competences that need to be demonstrated** |
--|-----------------|
6 | Running a large number of off-the-shelf inference procedures on several problems |
7 | Composition of basic inference procedures, with minor modifications to their original form |
8 | Development of problem-specific inference procedures that leverage problem structure and domain insights in a non-trivial way <br> Basic procedure that generalises across problems <br> Contribution in terms of new problems or innovative rewrites of provided programs |
9 | Use of deep theoretical insights <br> Development of a single inference procedure that works well on different problems |
10 | Execution that  can be published as a research paper <br> Using insights beyond what was explicitly covered in the lectures |
--|----------------|

**Presentation, discussions, reviews**

**Grade** | **Competences that need to be demonstrated** |
--|-----------------|
6 | Understandable presentation, but no effort to make the topic more understandable through materials beyond the provided reading <br><br> The presentation and reviews demonstrate shallow understanding of most of the topics <br><br> Critical analysis is shallow <br><br> Active participation only in  few discussions |
7 | Presentation make extensive use of visualisations and examples <br><br>The presentation and reviews demonstrate good understanding of the topics and very good understanding of a few of them <br><br> Critical analysis is focused on the limitations outlined in a paper, but a student can elaborate in more details why  <br><br> Frequent participation in discussions, but not going too much into depth |
8 | Presentation draws connections to other topics covered in the course <br><br> The presentations and reviews demonstrate very good understanding of the topics <br><br> Provide critical analysis beyond what is outlined in the papers while also identifying solutions <br><br> Frequent participation in discussions, with a deeper insight demonstrated in few discussions |
9 | Presentation offers a very comprehensive introduction to the topic, broader than the required reading <br><br> Reviews demonstrate a very good understanding of all topics <br><br> Critical analysis goes beyond the limitations in the paper, the weaknesses are well elaborated, and the analysis contains concrete solutions <br><br> Active participation in the majority of discussions, with frequently sharing deeper insights about the topics |
10 | Demonstrable understanding of the topics beyond what was required. <br><br> The equivalent of identifying a research problem and conceiving a detailed research plan how to address it |
--|----------------|



### Preparing your presentation

You will have to present one paper to the group. Student presentation start in week 3.

Your presentation should take between 15 and 20 mins. This is an estimate, some papers might require less while other more time. If you think you have to go beyond this limit, discuss it with me.

Approach your presentation as a short lecture. You goal is to explain the topic to your colleagues so that they learn from the lecture; only half of the student in the class will have read the paper. Think about the right way to explain the topic; this might not be the way it was explained in the paper. For instance, if you found that you had to look a lot of other concepts, explain them before the topic you are covering. 
Use illustrations and animations, you can find lots of them online (if not for the exact topic, then for something very related that could help you explain the intuition). Provide a working example, especially if such an example is not present in the original paper.

Feel free to use "non-academic" materials for your preparations: blogs, videos, informal notes... I don't care what you use as long as you understand the topic.  Importantly, if you encounter materials that you found more useful than the one I proposed, share them with me. 

Your main focus in the presentation should be to convey the idea/concept to your colleagues. This usually means that you have to think about not only how to convey the idea effectively but also which parts of the paper to include or skip. There will be no correlation between the amount of content squeezed in a lecture and a grade. Often it makes sense to skip something to optimise for clarity.

**Important:** schedule a meeting with me at least 2 days before your presentation; this is to ensure that your presentation is of sufficient quality to provide a valuable learning experience to your colleagues. 







### Project rules

The project has few rules:
 - you can use any PPL you want. I would encourage you to play with multiple ones. Choose the tools based on what they can do for you rather than which language are they implemented in. I would strongly suggest to at least have a look at the PPLs that support programmable inference (such as Gen, Turing, and Pyro).  Some tools you might consider: [Gen.jl](https://www.gen.dev/), [Pyro](https://pyro.ai/), [PyMC3](https://docs.pymc.io/en/v3/index.html), [Anglican](https://probprog.github.io/anglican/), [Turing.jl](https://turing.ml/stable/), [Stan](https://mc-stan.org/), [ProbTorch](https://github.com/probtorch/probtorch), [TensorFlow probability](https://www.tensorflow.org/probability), [Bean Machine](https://beanmachine.org/).
 - Form teams of 2 or 3 
 - Your team can submit floor(N/2) inference procedures, where N is the number of problems. All submitted procedures will be run on every problem, and the best result will be kept for each problem. The idea behind limiting this is to force you to develop at least some inference procedures that work on multiple problems. You can decide how to divide the inference procedures over tasks: you can made a few submissions that specialise on a particular problem and accompany it with one general inference procedures, or vice versa. You general inference procedures can be *meta-procedures*: they can try to figure out which inference procedure to use (or their composition) heuristically.
 - You can make as many submissions as possible. We will run the evaluation once per week with the most recent submission. Every submission needs to be followed with a log entry (i.e., [project report](#project-reports)).
 - You can submit your own problems. Once I approve your problem, all teams need to consider them.
 - You have to use a common Docker image.
 - You can re-write the given programs, as long as they retain the same meaning. 
 - createa Github repository and share it with me.


### Project reports

You will not be making a standard project report that you submit once at the end of the quarter summarising your findings.
Instead, the project report will be the logs that you make with each project submission.
The logs have free form but have to answer two questions: (1) what did you change, and (2) why did you make that change.
The ansers to these questions do not have to be extensive elaborations, but should be a concise summary sufficient for me to understand your motivations. 


Don't interpret 'motivation' too strictly. It is acceptable to occasionally just try out something. You just don't want you rreport to be a collection of random tryouts.
It is also ok to have a huntch which you cannot fully ground in the theory explored during the lectures. 

Don't be shy with negative results. Sometimes you have an idea you think would be successful, but is not. This is normal. This is good progress if your motivation for trying it out makes sense. Note that 'makes sense' is different from 'correct'. You might have made a mistake in your reasoning and that is also a part of the process (this can still earn you points).

Upload your log in Brightspace (Project). The log of each submission should be a separate file.


### Course feedback

This is the first edition of the course. 
As you can imagine, this is kind of a beta version of the course.
To make sure the course offers the best learning experience to you, I would appreciate if you provide feedback throughout the course.
What works for you? What doesn't? Do you have an idea how to improve something?

You can submit the feedback anonymously [HERE](https://forms.gle/PUGRCUwsZp4HNGbC7).


### Paper reviews

#### W3 L5 P1

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - Apply the transformation to the if-then statement starting at line 9 in Figure 1

 - Why focus on weakest precondition analysis? Wouldn't it make sense to derive stronger conditions?

 - Give an example of a potential weakest precondition rule for continuous case.

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer.

 - Identify at least one limitation and, if you can, propose a solution.



#### W3 L5 P2

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - How does exactly non-centering make sampling more efficient?

 - Work out an implementation of the non-centering transformation in one of the paradigms of L4.

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer.

 - Identify at least one limitation and, if you can, propose a solution.


#### W3 L6 P2


 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - Why is Hamiltonian dynamics interesting for probabilistic inference? What does it buy us?

 - Take a closer look at equation 11.67. What does the difference in two Hamiltonians actually capture?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer.

 - Identify at least one limitation and, if you can, propose a solution.


#### W3 L6 P1

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - What is the main difference between forward and reverse mode autmamted differentiation?

 - When is forward (reverse) mode more efficient?

 - How is it possible that we can differentiate an entire program, with complex control flow and branching? 

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.



#### W4 L7 P1

 - What is the problem that the work addresses?

 - Explain the idea behind variational inference in your own words. 

 - How does this work create a variational equivalent of the provided program?

 - What are the conditions the target program needs to fulfil in order to use variational inference (of the kind described in the paper)?

 - When will variational inference fail?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.


#### W4 L7 P2

 - What is the problem that the work addresses?

 - Explain the idea behind variational inference in your own words. 

 - When will variational inference fail?

 - Does this technique works for any probabilistic program?

 - Why are the two transformations necessary?

 - Which part of the framework is variationally approximated?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.




#### W4 L8 P1

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - What is neural networks predicting exactly?

 - What is the difference compared to variational inference?

 - The paper pays special attention to gradient estimators. The variational inference paper we looked into did not do that. Why is this issue important for this paper?

 - How does the paper make discrete probabilistic choices 'differentiable'?

 - Why is the function mapData important in this work?

 - How does the paper ensure that the guide program keeps the control flow of the starting probabilistic program?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.




#### W4 L8 P2

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - What is neural networks predicting exactly?

 - What is the difference compared to variational inference?

 - Why did the authors chose the LSTM to model a program?

 - Assume you have trained a compiled inference network, but your query suddenly changes together with the observations. Can you reuse your compiled inference network?

 - Could you use this idea in other inference algorithms, beyond importance sampling? If yes, how?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.



#### W5 L9 P1

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - What is the key computational abstraction that makes programmable inference possible?

 - Can an inference procedure over a subproblem change any part of a program? 

 - How does Venture ensures that the trace remains valid after an inference step for a subproblem?

 - What is a valid trace?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.

#### W5 L9 P2

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - Give an example of a problem that could be difficult to solve with *standard* proposal but easy to do with a specific programmatic proposal? Give a sketch of such a proposal program?

 - what is the difference between *output choices* and *internal choices*?

 - Explain in your words why programs as proposal do not affect the guarantees offered by Importance sampling and Metropolis-Hastings inference algorithm?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.


#### W5 L10 P1

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - Why is the consider problem suitable for probabilistic programming?

 - Which quantities of the considered model are uncertain/probabilitic?

 - What is a big challenge in applying probabilistic inference to physics problems?

 - Do inference procedures we hve seen in the course require any modification to be applied to this problem? Why?

 - What needs to be changed in the original simulator to use it within probabilistic programming engine?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.



#### W5 L10 P2

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - Why is the consider problem suitable for probabilistic programming?

 - What are the assumptions that the paper makes?

 - What are the sources of uncertanty in epidemiological models?

 - Do inference procedures we hve seen in the course require any modification to be applied to this problem? Why?

 - What needs to be changed in the original simulator to use it within probabilistic programming engine?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.




#### W6 L11 P1

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - Involutive MCMC needs three ingredients? Which ones and why are they needed?

 - What does the auxiliary variables do? Try to relate it to other inference procedure we have seen in the class?

 - What are the key abstractions that this paper contributes in order to make involutive MCMC applicable to any problem that can be expressed in probabilistic programming?

 - What is the key part that makes it possible to easily switch between traces with different number of stochastic choices?

 - Probabilistic programming perspective makes one part of involutive MCMC easy. Which part is that?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.


#### W6 L11 P2

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - Why does the work focuses on straight-line programs?

 - Why can we so easily combine samples of individual straight-line programs?

 - What is the role of resource allocation in DCC?

 - Explain in your words why inference procedures likw Metropolis-Hastings MCMC and paricle filtering are bad at problems with stochastic support?

 - DCC draws samples from two *spaces*; which ones and why are they needed?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.


#### W6 L12 P1

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - Why is the combination of logic and probability interesting?

 - What is the role of weighted model counting in Problog?

 - What is the advantage of Problog when it comes to finding executions of a program that lead to the query?

 - Why is a disjoint sum a problem?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.


#### W6 L12 P2

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - Why is the combination of logic and probability interesting?

 - What makes a logical proof more important?

 - What is the main difference between this kind of approximation and other approximate techniques we have seen in the course?

 - How do we find the optimal proofs efficiently?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution


#### W7 L13 P1

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - What makes VAE variational?

 - What issue does the reparametrization trick solve? 

 - VAE does not make any assumption about the structure of data, unlike a probabilistic program. Explain what that means?

 - What can a probabilistic program do that VAE cannot?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.


#### W7 L13 P2

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - What makes the flows normalizing? Why can we treat the transformed function q_K as the probability density of z_K?

 - Why do we require the transformations to be invertible?

 - What do flows do better than variational inference we have seen so far?

 -  What can a probabilistic program do that VAE cannot?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.


#### W7 L14 P1

 - Explain what weighted model counting is and how is it related to probabilistic inference.

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 



#### W8 L15 P1

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - What does the prior represent in this work?

 - What is the posterior distribution representing?

 - What does the likelihood term (probability of x given y) represent?

 - what are the observations that we can observe?

 - What did the authors need to change in inference procedures to make them work on this problem?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.


#### W8 L15 P2

 - What is the problem that the work addresses?

 - Explain the main contribution of the work in your own words.

 - What does the prior represent in this work?

 - What is the posterior distribution representing?

 - What does the likelihood term (probability of x given y) represent?

 - what are the observations that we can observe?

 - What did the authors need to change in inference procedures to make them work on this problem?

 - What question(s) would you ask yourself to test your understanding? Provide the question and the answer. 

 - Identify at least one limitation and, if you can, propose a solution.

