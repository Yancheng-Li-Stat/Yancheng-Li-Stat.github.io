---
layout: archive
title: "Stat 888"
permalink: /Stat-888/
author_profile: true
line-height: 1.55
font-size: 12pt
---


The study is based on this [Paper](https://arxiv.org/pdf/2103.04472.pdf).

## Model Identification (Homework 2)

$$\psi(\bar{a}_t)=\int\cdots\int E$$

## A Causal Question to Study (Homework 1)

I want to study the relationship between social mobility and number of deaths due to Covid-19: can reduced social mobility decrease the number of deaths due to Covid-19? How many deaths would have occurred if an intervention (e.g. closing the school, quarantine, ...) had been applied? Although the Covid-19 pandemic has already ended, these questions are still important to study in order to better prepare for the next potential global pandemic in the future.

We model this problem as a stochastic process $(A_t,I_t,Y_t)(t=1,2,\cdots,T)$, where 

$A_t:\ \text{social mobility on week t}$

$I_t:\ \text{new infections in week t}$

$Y_t:\ \text{the number of deaths due to Covid-19 on week t}$

Note that we cannot simply perform a linear regression of $Y_t$ on $A_t$ (without $I_t$), because $Y_t$ are both confounding and mediating variables: 
$Y_{t-1}$ can have an effect on both $A_t$ and $Y_t$, while also being affected by $A_{t-1}$. As a result, we introduce a new unobserved random variable $I_t$ as a  mediator. The causal effect of social mobility we wish to study can be defined as

$\varphi_t(a_1,\cdots,a_T)=E[Y_t(a_1,\cdots,a_T)]$

The relationship (or the working hypotheses) of $(A_t,I_t,Y_t)$ is given by the following directed acyclic graph:
![plot](./Graph.png)
