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

The course consists of several learning activities, alongside lectures by the intrstructor, with the points distributed as follows:
 - 0%: Paper reviews 
 - 25%: Presentation
 - 65%: Research report
 - 10%: Participation  
 

**Paper reviews.** 
The course will take the format of a research seminar. 
This means that there will be no textbook and blackboard lectures; instead, we will be reading and discussing state of the art papers in the field. 
Consequently, you are expected to come prepared for the class by reading one of the papers covered in the lecture.
As a preparation for the class, you have to write a review of that paper. 
The reviews consist of a few questions that help you understand the paper to sufficient extend; they will point out important points, what you should pay attention to, and which part you can avoid.
Scientific articles are not always easy to read as they are typically written for people that already know a lot about the field; the review questions help you navigate that.
The reviews are not graded, but are essential preparation for the classes.
After the lectures, you will receive prototypical answer that help you to track your progress.



**Paper presentation.** 
You are expected to present one of the assigned papers. 
You will understand the paper in details, including searching for additional literature that helps you to understand the paper and why it works, and present it to your colleagues. 
Your objective for the presentation: explain the core idea behind the assigned paper in clearest terms possible. Don't try to cover everything in the paper, identify important and essential parts. 
Convey the intuitions before the math.



**Research report.**
The largest part of your grade and efforts goes to a research report. 
In contrast to standard courses, the goal of this course is not for you to just learn what you have been thought; instead, the goal is to go beyond the materials and think about strengths and weaknesses, and how to overcome them.
Your task is to do that for your assigned topic: you will start from your paper, relate it to other content of the course, explore the current status of the topic, analyse its strength and weaknesses, and propose new research directions.
You don't have to execute that research, but you have to develop a proposal.
You are also expected to stress-test the method experimentally, either starting from an existing implementation or producing a simplified implementation yourself.





**Class participation.** 
As this is a seminar course, you are expected to *actively participate* in class. 
During the lectures, we will be clarifying the details from the papers, analysing their strengths, weaknesses, and evaluation; in other words, exactly what you are supposed to do in your reports.
Your participation will be graded in two ways:
 - Sending questions in advance. To start up discussion, I ask you to think about the papers in advance and post questions you have about it. What is a good question? Anything that helps you to understand the paper and is not of the form "What is X?" where X is something explained in the paper.
 - Helping others. Our shared goal is to understand the papers, and the field of probabilistic programming itself, together. We will maintain a shared PDF in which you can post and answer questions about papers. 

See [how to do well in a seminar course.](#how-to-do-well-in-a-seminar-course) 



## Schedule


You do not have to read every paper from the required literature. 
You will be divided in groups (group split is on Brightspace) and each group reads only one paper for the class. 
You will learn about the other paper from the presentation of your colleagues.

Use review questions to focus on the important parts.
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
    <tr valign="top" >
      <td></td>
      <td markdown="span">
        **Paper 1** <br>
        [Chapter 8](https://probmods.org/chapters/inference-algorithms.html) from [Probabilistic models of cognition](Probabilistic models of cognition) <br>
        Noah D. Goodman, Joshua B. Tenenbaum<br>
        
        **Paper 2** <br>
        Sections 4.1-4.3 from [An introduction to probabilistic programming](https://arxiv.org/pdf/1809.10756.pdf) <br>
        Jan-Willem van de Meent, Brooks Paige, Hongseok Yang, Frank Wood<br>
        
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
    <tr valign="top" >
      <td></td>
      <td markdown="span">
        **Paper 1** <br>
        [Lightweight Implementations of Probabilistic Programming Languages Via Transformational Compilation](http://proceedings.mlr.press/v15/wingate11a/wingate11a.pdf) <br>
        David Wingate, Andreas Stuhlmüller, Noah D. Goodman<br>
        [[Miro board]](https://miro.com/app/board/uXjVMtjPqNo=/?share_link_id=350930972822)
        
        **Paper 2** <br>
        [C3: Lightweight Incrementalized MCMC for Probabilistic Programs using Continuations and Callsite Caching](https://arxiv.org/pdf/1509.02151.pdf) <br>
        Daniel Ritchie, Andreas Stuhlmuller, Noah D. Goodman<br>
        [[Miro board]](https://miro.com/app/board/uXjVMtiBzTw=/?share_link_id=827175051942)

        **Paper 3** <br>
        Sections 6.1, 6.4-6.7 from [An introduction to probabilistic programming](https://arxiv.org/pdf/1809.10756.pdf) <br>
        Jan-Willem van de Meent, Brooks Paige, Hongseok Yang, Frank Wood<br><br>
        
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
        [[Miro board]](https://miro.com/app/board/uXjVMtiBw3s=/?share_link_id=462517837474) <br>
        *Code starter:* [HMC implementation in Gen.jl](https://docs.juliahub.com/Gen/OEZG1/0.4.1/ref/mcmc/#Built-in-Stationary-Kernels-1) or implement it from scratch
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span">
        **Paper 2** <br>
        [Automated Variational Inference in Probabilistic Programming](https://arxiv.org/pdf/1301.1299.pdf) <br>
        David Wingate, Theo Weber<br>
        [[Miro board]](https://miro.com/app/board/uXjVMtiBw8c=/?share_link_id=80775884375) <br>
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
        [[Miro board]](https://miro.com/app/board/uXjVMtiBw7M=/?share_link_id=994773568352) <br>
        *Code starter:* start from Gen.jl and implement a machine learning part
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Inference Compilation and Universal Probabilistic Programming](https://arxiv.org/pdf/1610.09900.pdf) <br>
        Tuan Anh Le, Atılım Güneş Baydin, Frank Wood<br>
        [[Miro board]](https://miro.com/app/board/uXjVMthiiP4=/?share_link_id=191320299251) <br>
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
        [[Miro board]](https://miro.com/app/board/uXjVMthiiLI=/?share_link_id=251466589215) <br>
        *Code starter:* [Gen.jl](https://www.gen.dev/) provides you with everything you need to implement a simplified version of this. You are allowed to collaborate wiht the colleague from the same session
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Rethinking Variational Inference for Probabilistic Programs with Stochastic Support](https://openreview.net/pdf?id=wjClgX-muzB) <br>
        Tim Reichelt, Luke Ong, Tom Rainforth<br>
        [[Miro board]](https://miro.com/app/board/uXjVMthiid8=/?share_link_id=510934592885) <br>
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
        [[Miro board]](https://miro.com/app/board/uXjVMthijg8=/?share_link_id=16520920058) <br>
        *Code starter:* [Gen.jl](https://www.gen.dev/)
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [SMCP3: Sequential Monte Carlo with probabilistic program proposals](https://proceedings.mlr.press/v206/lew23a.html)<br>
        Alexander K Lew, George Matheos, Tan Zhi-Xuan, Matin Ghavamizadeh, Nishad Gothoskar, Stuart Russell, Vikash K Mansinghka<br>
        [[Miro board]](https://miro.com/app/board/uXjVMthiju8=/?share_link_id=160364427270) <br>
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
        [[Miro board]](https://miro.com/app/board/uXjVMthijqI=/?share_link_id=265343576932)
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Scaling Exact Inference for Discrete Probabilistic Programs](https://arxiv.org/abs/2005.09089)<br>
        Steven Holtzen, Guy van den Broeck, Todd Millsten<br>
        [[Miro board]](https://miro.com/app/board/uXjVMthij2Q=/?share_link_id=681684492218) <br>
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
        [[Miro board]](https://miro.com/app/board/uXjVMtGYRCQ=/?share_link_id=975966924368) <br>
        *Code starter:* [Problog website](https://dtai.cs.kuleuven.be/problog/)
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [k-Optimal: A novel approximate inference algorithm for Problog](k-Optimal: A novel approximate inference algorithm for Problog)<br>
        Joris Renkens, Guy Van den Broeck, Siegfried Nijssen<br>
        [[Miro board]](https://miro.com/app/board/uXjVMtGYRN8=/?share_link_id=449278371126)
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
        [[Miro board]](https://miro.com/app/board/uXjVMtGYRJE=/?share_link_id=352713619226)
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Anytime Inference in Probabilistic Logic Programs with TP-Compilation](https://www.ijcai.org/Proceedings/15/Papers/263.pdf)<br>
        Jonas Vlasselaer, Guy Van den Broeck, Angelika Kimmig, Wannes Meert, Luc De Raedt<br>
        [[Miro board]](https://miro.com/app/board/uXjVMtGYRSI=/?share_link_id=394484032419)
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
        [Miro board]
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [DeepStochLog: Neural Stochastic Logic Programming](https://arxiv.org/abs/2106.12574)<br>
        Thomas Winters, Giuseppe Marra, Robin Manhaeve, Luc De Raedt<br>
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
        [Variational Inference with Normalizing Flows](https://arxiv.org/pdf/1505.05770.pdf)<br>
        Danilo Jimenez Rezende, Shakir Mohamed<br>
        [[Miro board]](https://miro.com/app/board/uXjVMtGYRdo=/?share_link_id=106069796777)<br>
        *Code starter:* any implementation of normalising flows like [normalizing flows in Pytorch](https://github.com/VincentStimper/normalizing-flows), [FlowTorch](https://flowtorch.ai/), or [Pyro](https://pyro.ai/examples/normalizing_flows_i.html)

      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Denoising Diffusion Probabilistic Models](https://arxiv.org/abs/2006.11239)<br>
        Jonathan Ho, Ajay Jain, Pieter Abbeel<br>
        [[Miro board]](https://miro.com/app/board/uXjVMtVcDos=/?share_link_id=635867473828) <br>
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
        [[Miro board]](https://miro.com/app/board/uXjVMtFCwcM=/?share_link_id=313897442346) <br>
        *Code starter:* Problog allows you to [play with various semirings](https://dtai.cs.kuleuven.be/problog/wasp2017/session5.html)
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Automating Involutive MCMC using Probabilistic and Differentiable Programming](https://arxiv.org/abs/2007.09871)<br>
        Marco Cusumano-Towner, Alexander K. Lew, Vikash K. Mansinghka<br> 
        [[Miro board]](https://miro.com/app/board/uXjVMtPZaUs=/?share_link_id=264639656648) <br>
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
        [[Miro board]](https://miro.com/app/board/uXjVMtPZad0=/?share_link_id=159807287985) <br>
        *Code starter:* [SBI library](https://www.mackelab.org/sbi/) or implement it from scratch in [Gen.jl](https://www.gen.dev/)
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Efficient Probabilistic Inference in the Quest for Physics Beyond the Standard Model](https://arxiv.org/pdf/1807.07706.pdf)<br>
        Atılım Günes Baydin et al<br>
        [[Miro board]](https://miro.com/app/board/uXjVMtPZabs=/?share_link_id=841848106028) <br>
        *Code starter:* take a much simpler simulators and work with it
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
        [[Miro board]](https://miro.com/app/board/uXjVMtPZbnk=/?share_link_id=5429881514§) <br>
        *Code starter:* I recommend a fresh implementation in Gen.jl, but [the original code repository](https://github.com/schasins/PPL-synthesis) might have useful information
      </td>
    </tr>
    <tr valign="top" >
      <td></td>
      <td markdown="span" >
        **Paper 2** <br>
        [Bayesian Synthesis of Probabilistic Programs for Automatic Data Modeling](https://arxiv.org/abs/1907.06249)<br>
        Feras Saad, Marco Cusumano-Towner, Ulrich Schaechtle, Martin Rinard, and Vikash Mansinghka<br>
        [[Miro board]](https://miro.com/app/board/uXjVMtV-GeE=/?share_link_id=847628046927) <br>
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




### Preparing your presentation

You will have to present one paper to the group. Student presentation start in week 3.

Your presentation should take 15 mins. This is an estimate, some papers might require less while other more time. If you think you have to go beyond this limit, discuss it with me.

Approach your presentation as a short lecture. You goal is to explain the topic to your colleagues so that they learn from the lecture; only half of the student in the class will have read the paper. Think about the right way to explain the topic; this might not be the way it was explained in the paper. For instance, if you found that you had to look a lot of other concepts, explain them before the topic you are covering. 
Use illustrations and animations, you can find lots of them online (if not for the exact topic, then for something very related that could help you explain the intuition). Provide a working example, especially if such an example is not present in the original paper.

Feel free to use "non-academic" materials for your preparations: blogs, videos, informal notes... I don't care what you use as long as you understand the topic.  Importantly, if you encounter materials that you found more useful than the one I proposed, share them with me. 

Your main focus in the presentation should be to convey the idea/concept to your colleagues. This usually means that you have to think about not only how to convey the idea effectively but also which parts of the paper to include or skip. There will be no correlation between the amount of content squeezed in a lecture and a grade. Often it makes sense to skip something to optimise for clarity.

**Important:** schedule a meeting with me at least 2 days before your presentation; this is to ensure that your presentation is of sufficient quality to provide a valuable learning experience to your colleagues. 







### Project - implementation



### Project - report



### Course feedback

This is the first edition of the course. 
As you can imagine, this is kind of a beta version of the course.
To make sure the course offers the best learning experience to you, I would appreciate if you provide feedback throughout the course.
What works for you? What doesn't? Do you have an idea how to improve something?

You can submit the feedback anonymously [HERE](https://forms.gle/PUGRCUwsZp4HNGbC7).



