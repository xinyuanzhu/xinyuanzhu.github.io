---
layout: post
title: Hidden Confounder Removal 
subtitle: Causal inference in Recommender System
thumbnail-img: assets/img/blogs/lcdr_cg_00.jpg
tags: [research, recsys]
---
Recommender systems suffer from confounding biases when there exist confounders affecting both item features and user feedback (e.g., like or not). Existing causal recommendation methods typically assume confounders are fully observed and measured, forgoing the possible existence of hidden confounders in real applications. For instance, product quality is a confounder since affecting both item prices and user ratings, but is hidden for the third-party e-commerce platform due to the difficulty of large-scale quality inspection; ignoring it could result in the bias effect of over-recommending high-price items. This work analyzes and addresses the problem from a causal perspective. The key lies in modeling the causal effect of item features on a user's feedback. To mitigate hidden confounding effects, it is compulsory but challenging to estimate the causal effect without measuring the confounder. Towards this goal, we propose a Hidden Confounder Removal (HCR) framework that leverages front-door adjustment to decompose the causal effect into two partial effects, according to the mediators between item features and user feedback. The partial effects are independent from the hidden confounder and identifiable. During training, HCR performs multi-task learning to infer the partial effects from historical interactions.
