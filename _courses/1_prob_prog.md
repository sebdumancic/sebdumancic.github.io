---
layout: page
title: Probabilistic Programming Seminar 2023-2024
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

The course will consist of lectures by the instructors, paper reviews, student presentations on research papers, and a project. The points are distributed as follows:
 - 65%: Research report
 - 25%: Presentation
 - 10%: Participation  
 - 0%: Paper reviews

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
  font-size: 11px;
}
</style>
<font size="11">
<table>
  <colgroup>
    <col width="30%" />
    <col width="70%" />
  </colgroup>
  <thead>
    <tr class="header" style="border-bottom:1px solid black">
      <th>Date</th>
      <th>Topic</th>
    </tr>
  </thead>
  <tbody>
    <tr valign="top">
      <td markdown="span" >
        September 4, 2023 <br>
        (W1 L1)
      </td>
      <td markdown="span" >
        **What is probabilistic programming?** <br> What is model-based reasoning? The anatomy of a probabilistic program. Course structure.
      </td>
    </tr>
    <tr><td><br></td></tr>

    <tr valign="top">
      <td markdown="span" >
        September 7, 2023 <br>
        (W1 L2)
      </td>
      <td markdown="span" >
        **Generative thinking.** <br> How to write probabilistic programs? What is the distribution probabilistic program captures?
      </td>
    </tr>
    <tr><td><br></td></tr>

    <tr valign="top">
      <td markdown="span" >
        September 11, 2023 <br>
        (W2 L1)
      </td>
      <td markdown="span" >
        **Basic inference procedures:** <br> Enumeration, Rejection sampling, Importance Sampling, Metropolis-Hastings MCMC, Sequential Monte Carlo (Particle filtering). Why do they work? 
      </td>
    </tr>
    <tr><td><br></td></tr>


    <tr valign="top">
      <td markdown="span" >
        September 14, 2023 <br>
        (W2 L2)
      </td>
      <td markdown="span" >
        **Implementation strategies.** <br> Database view. Continuations. Message passing. 
      </td>
    </tr>
    <tr><td><br></td></tr>


    <tr valign="top">
      <td markdown="span" >
        September 18, 2023 <br>
        (W3 L1)
      </td>
      <td markdown="span">
        **Gradient-directed probabilistic inference** 
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span">
        **Paper 1** <br>
        [MCMC using Hamiltonian dynamics](https://arxiv.org/pdf/1206.1901.pdf) <br>
        Radford M. Neal<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:* [HMC implementation in Gen.jl](https://docs.juliahub.com/Gen/OEZG1/0.4.1/ref/mcmc/#Built-in-Stationary-Kernels-1) or implement it from scratch
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span">
        **Paper 2** <br>
        [Automated Variational Inference in Probabilistic Programming](https://arxiv.org/pdf/1301.1299.pdf) <br>
        David Wingate, Theo Weber<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:* [Implementation in Gen.jl](https://docs.juliahub.com/Gen/OEZG1/0.4.1/ref/vi/) or [Pyro](https://pyro.ai/), or implemented a macro in Gen.jl to transform an arbitrary program into a variational one
      </td>
    </tr>
    <tr><td><br></td></tr>


    <tr valign="top">
      <td markdown="span" >
        September 21, 2023 <br>
        (W3 L2)
      </td>
      <td markdown="span">
        **Learning for inference** 
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 1** <br>
        [Deep Amortized Inference for Probabilistic Programs](https://arxiv.org/pdf/1610.05735.pdf) <br>
        Daniel Ritchie, Paul Horsfall, Noah D. Goodman<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:* start from Gen.jl and implement a machine learning part
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Inference Compilation and Universal Probabilistic Programming](https://arxiv.org/pdf/1610.09900.pdf) <br>
        Tuan Anh Le, Atılım Güneş Baydin, Frank Wood<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:* implement a piple over Gen.jl or start from [this code](https://github.com/facebookresearch/lightweight-inference-compilation)
      </td>
    </tr>
    <tr><td><br></td></tr>



    <tr valign="top">
      <td markdown="span" >
        September 24 2023 <br>
        (W4 L1)
      </td>
      <td markdown="span" >
        **Programs with stochastic support** 
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 1** <br>
        [Divide, Conquer, and Combine: a New Inference Strategy for Probabilistic Programs with Stochastic Support](https://arxiv.org/pdf/1910.13324.pdf) <br>
        Yuan Zhou, Hongseok Yang, Yee Whye Teh, Tom Rainforth <br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:* [Gen.jl](https://www.gen.dev/) provides you with everything you need to implement a simplified version of this. You are allowed to collaborate wiht the colleague from the same session
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Rethinking Variational Inference for Probabilistic Programs with Stochastic Support](https://openreview.net/pdf?id=wjClgX-muzB) <br>
        Tim Reichelt, Luke Ong, Tom Rainforth<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:* [Gen.jl](https://www.gen.dev/) provides you with everything you need to implement a simplified version of this. You are allowed to collaborate wiht the colleague from the same session
      </td>
    </tr>
    <tr><td><br></td></tr>


    <tr valign="top">
      <td markdown="span" >
        September 28 2023 <br>
        (W4 L2)
      </td>
      <td markdown="span" >
        **Programmable inference** 
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 1** <br>
         [Gen: A General-Purpose Probabilistic Programming System with Programmable Inference](https://dl.acm.org/doi/pdf/10.1145/3314221.3314642)<br>
        Marco F. Cusumano-Towner, Feras A. Saad, Alexander K. Lew, Vikash K. Mansinghka<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:* [Gen.jl](https://www.gen.dev/)
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [SMCP3: Sequential Monte Carlo with probabilistic program proposals](https://proceedings.mlr.press/v206/lew23a.html)<br>
        Alexander K Lew, George Matheos, Tan Zhi-Xuan, Matin Ghavamizadeh, Nishad Gothoskar, Stuart Russell, Vikash K Mansinghka<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter: [Gen.jl library](https://github.com/probcomp/GenSMCP3.jl) implementing the functionality in Gen.jl, or build a simplified version from scratch
      </td>
    </tr>
    <tr><td><br></td></tr>



    <tr valign="top">
      <td markdown="span" >
        October 2, 2023 <br>
        (W5 L1)
      </td>
      <td markdown="span" >
        **Connection between probabilistic and logical reasoning** 
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 1** <br>
        [On probabilistic inference by weighted model counting](https://www.sciencedirect.com/science/article/pii/S0004370207001889)<br>
        Mark Chavira, Adnan Darwiche<br>
        [Review questions] 
        [Miro board]
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Scaling Exact Inference for Discrete Probabilistic Programs](https://arxiv.org/abs/2005.09089)<br>
        Steven Holtzen, Guy van den Broeck, Todd Millsten<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:* [Dice repository](http://dicelang.cs.ucla.edu/)
      </td>
    </tr>
    <tr><td><br></td></tr>


    <tr valign="top">
      <td markdown="span" >
        October 5, 2023 <br>
        (W5 L2)
      </td>
      <td markdown="span" >
        **Probabilistic logic programming** 
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 1** <br>
        [ProbLog: A Probabilistic Prolog and its Application in Link Discovery](https://dtai.cs.kuleuven.be/publications/files/42447.pdf)<br>
        Luc De Raedt, Angelika Kimmig, Hannu Toivonen<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:* [Problog website](https://dtai.cs.kuleuven.be/problog/)
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [k-Optimal: A novel approximate inference algorithm for Problog](k-Optimal: A novel approximate inference algorithm for Problog)<br>
        Joris Renkens, Guy Van den Broeck, Siegfried Nijssen<br>
        [Review questions] 
        [Miro board]
      </td>
    </tr>
    <tr><td><br></td></tr>



    <tr valign="top">
      <td markdown="span" >
        October 9, 2023 <br>
        (W6 L1)
      </td>
      <td markdown="span" >
        **Incremental and anytime inference** 
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 1** <br>
        [Incremental inference for probabilistic programs](https://dl.acm.org/doi/pdf/10.1145/3296979.3192399)<br>
        Marco Cusumano-Towner, Benjamin Bichsel, Timon Gehr, Martin Vechev, Vikash K. Mansinghka<br>
        [Review questions] 
        [Miro board]
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Anytime Inference in Probabilistic Logic Programs with TP-Compilation](https://www.ijcai.org/Proceedings/15/Papers/263.pdf)<br>
        Jonas Vlasselaer, Guy Van den Broeck, Angelika Kimmig, Wannes Meert, Luc De Raedt<br>
        [Review questions] 
        [Miro board]
      </td>
    </tr>
    <tr><td><br></td></tr>



    <tr valign="top">
      <td markdown="span" >
        October 12, 2023 <br>
        (W6 L2)
      </td>
      <td markdown="span" >
        **Deep probabilistic programming** 
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 1** <br>
        [DeepProbLog: Neural Probabilistic Logic Programming](https://arxiv.org/pdf/1805.10872.pdf)<br>
        Robin Manhaeve, Sebastijan Dumančić, Angelika Kimmig, Thomas Demeester, Luc De Raedt<br>
        [Review questions] 
        [Miro board]
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [DeepStochLog: Neural Stochastic Logic Programming](https://arxiv.org/abs/2106.12574)<br>
        Thomas Winters, Giuseppe Marra, Robin Manhaeve, Luc De Raedt<br>
        [Review questions] 
        [Miro board]
      </td>
    </tr>
    <tr><td><br></td></tr>

    <tr valign="top">
      <td markdown="span" >
        October 16, 2023 <br>
        (W7 L1)
      </td>
      <td markdown="span" >
        **Deep generative models** 
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 1** <br>
        [Normalizing Flows for Probabilistic Modeling and Inference](https://arxiv.org/abs/1912.02762)<br>
        George Papamakarios, Eric Nalisnick, Danilo Jimenez Rezende, Shakir Mohamed, Balaji Lakshminarayanan<br>
        [Review questions] 
        [Miro board]<br>
        *Code starter:* any implementation of normalising flows like [normalizing flows in Pytorch](https://github.com/VincentStimper/normalizing-flows), [FlowTorch](https://flowtorch.ai/), or [Pyro](https://pyro.ai/examples/normalizing_flows_i.html)

      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Denoising Diffusion Probabilistic Models](https://arxiv.org/abs/2006.11239)<br>
        Jonathan Ho, Ajay Jain, Pieter Abbeel<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:* any implementation such as [this one](https://github.com/lucidrains/denoising-diffusion-pytorch)
      </td>
    </tr>
    <tr><td><br></td></tr>



    <tr valign="top">
      <td markdown="span" >
        October 19, 2023 <br>
        (W7 L2)
      </td>
      <td markdown="span" >
        **Generalised paradigms for probabilistic programming** 
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 1** <br>
        [Algebraic Model Counting](https://www.sciencedirect.com/science/article/pii/S157086831630088X)<br>
        Angelika Kimmig, Guy Van den Broeck, Luc De Raedt<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:* Problog allows you to [play with various semirings](https://dtai.cs.kuleuven.be/problog/wasp2017/session5.html)
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Automating Involutive MCMC using Probabilistic and Differentiable Programming](https://arxiv.org/abs/2007.09871)<br>
        Marco Cusumano-Towner, Alexander K. Lew, Vikash K. Mansinghka<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:* [Gen.jl's implementation](https://www.gen.dev/docs/stable/ref/mcmc/#Involutive-MCMC-1) of Involutive MCMC
      </td>
    </tr>
    <tr><td><br></td></tr>




    <tr valign="top">
      <td markdown="span" >
        October 23, 2023 <br>
        (W8 L1)
      </td>
      <td markdown="span" >
        **No probability? No problem! Alternative sources of probabilities.** 
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 1** <br>
        [Approximate Bayesian computation scheme for parameter inference and model selection in dynamical systems](https://pubmed.ncbi.nlm.nih.gov/19205079/)<br>
        Tina Toni, David Welch, Natalja Strelkowa, Andreas Ipsen and Michael P.H Stumpf<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:* [SBI library](https://www.mackelab.org/sbi/) or implement it from scratch in [Gen.jl](https://www.gen.dev/)
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Sequential Monte Carlo Steering of Large Language Models using Probabilistic Programs](https://arxiv.org/abs/2306.03081)<br>
        Alexander K. Lew, Tan Zhi-Xuan, Gabriel Grand, Vikash K. Mansinghka<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:* [official implementation](https://github.com/probcomp/LLaMPPL)
      </td>
    </tr>
    <tr><td><br></td></tr>




    <tr valign="top">
      <td markdown="span" >
        October 26, 2023 <br>
        (W8 L1)
      </td>
      <td markdown="span" >
        **Learning probabilistic programs** 
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 1** <br>
        [Data-Driven Synthesis of Full Probabilistic Programs](https://schasins.com/assets/papers/dataDrivenSynthesisOfFullProbabilisticPrograms.pdf)<br>
        Sarah Chasins, Phitchaya Mangpo Phothilimthana<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:* I recommend a fresh implementation in Gen.jl, but [the original code repository](https://github.com/schasins/PPL-synthesis) might have useful information
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Bayesian Synthesis of Probabilistic Programs for Automatic Data Modeling](https://arxiv.org/abs/1907.06249)<br>
        Feras Saad, Marco Cusumano-Towner, Ulrich Schaechtle, Martin Rinard, and Vikash Mansinghka<br>
        [Review questions] 
        [Miro board] <br>
        *Code starter:*  Implement a simplified version in Gen.jl
      </td>
    </tr>
    <tr><td><br></td></tr>


  </tbody>
</table>
</font>






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

