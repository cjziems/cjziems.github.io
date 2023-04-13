---
layout: page
permalink: /datasets/
title: datasets
description:
nav: false
nav_order:
---


## 🤗 [Implicit Hate](https://huggingface.co/datasets/SALT-NLP/ImplicitHate)
##### *Why Implicit Hate?* 

It is important to consider the subtle tricks that many extremists use to mask their threats and abuse. These more implicit forms of hate speech may easily go undetected by keyword detection systems, and even the most advanced architectures can fail if they have not been trained on implicit hate speech ([Caselli et al. 2020](https://aclanthology.org/2020.lrec-1.760/)).

##### *What's 'in the box?'* 

This dataset contains **22,056** tweets from the most prominent extremist groups in the United States; **6,346** of these tweets contain *implicit hate speech.* We decompose the implicit hate class using the following taxonomy (distribution shown on the left).

* ![24.2%](https://progress-bar.dev/24) **Grievance:** frustration over a minority group's perceived privilege.
* ![20.0%](https://progress-bar.dev/20) **Incitement:** implicitly promoting known hate groups and ideologies (e.g. by flaunting in-group power).
* ![13.6%](https://progress-bar.dev/14) **Inferiority:** implying some group or person is of lesser value than another.
* ![12.6%](https://progress-bar.dev/23) **Irony:** using sarcasm, humor, and satire to demean someone.
* ![17.9%](https://progress-bar.dev/18) **Stereotypes:** associating a group with negative attribute using euphemisms, circumlocution, or metaphorical language.
* ![10.5%](https://progress-bar.dev/11) **Threats:** making an indirect commitment to attack someone's body, well-being, reputation, liberty, etc.
* ![1.2%](https://progress-bar.dev/1) **Other**

Each of the 6,346 implicit hate tweets also has free-text annotations for *target demographic group* and an *implied statement* to describe the underlying message (see banner image above).

##### *What can I do with this data?* 

State-of-the-art neural models may be able to learn from our data how to (1) classify this more difficult class of hate speech and (3) explain implicit hate by generating descriptions of both the *target* and the *implied message.* As our paper baselines show, neural models still have a ways to go, especially with classifying *implicit hate categories*, but overall, the results are promising, especially with *implied statement generation,* an admittedly challenging task. 

We hope you can extend our baselines and further our efforts to understand and address some of these most pernicious forms of language that plague the web, especially among extremist groups.

## 🤗 [MIC](https://huggingface.co/datasets/SALT-NLP/MIC)

##### *Why MIC?* 

Open-domain or "chit-chat" conversational agents often reflect insensitive, hurtful, or contradictory viewpoints that erode a user’s trust in the integrity of the system. Moral integrity is one important pillar for building trust. 

`MIC` is a dataset that can help us understand chatbot behaviors through their latent values and moral statements. 

##### *What's 'in the box?'* 

`MIC` contains 114k annotations, with 99k distinct "Rules of Thumb" (RoTs) that capture the moral assumptions of 38k chatbot replies to open-ended prompts. These RoTs represent diverse moral viewpoints, with the following distribution of underlying moral foundations: 

* ![51%](https://progress-bar.dev/51) **Care:** wanting someone or something to be safe, healthy, and happy. (58k chatbot replies)
* ![21%](https://progress-bar.dev/21) **Fairness:** wanting to see individuals or groups treated equally or equitably. (24k)
* ![19%](https://progress-bar.dev/19) **Liberty:** wanting people to be free to make their own decisions. (22k)
* ![19%](https://progress-bar.dev/19) **Loyalty:** wanting unity and seeing people keep promises or obligations to an in-group. (22k)
* ![18%](https://progress-bar.dev/18) **Authority:** wanting to respect social roles, duties, privacy, peace, and order. (20k)
* ![11%](https://progress-bar.dev/11) **Sanctity:** wanting people and things to be clean, pure, innocent, and holy. (13k)


##### *What can I do with this data?* 

We can train encoder-decoder models to automatically generate RoT explanations for chatbot behaviors. This could facilitate explainable downstream applications. For example, we could train RL systems that demote chatbot replies which fall into certain moral classes or train safety classifiers that guide systems towards the desired behaviors, with sensitivity towards ideological and political difference.

In the RoT generation task, we find our best models match the quality, fluency, and relevance of human annotations, but they still generate irrelevant RoTs nearly 28% of the time. This suggests that the proposed generation task is not yet solved and that `MIC` can continue to serve as resource for ongoing work in developing morally-consistent conversational agents.

## 🤗 [Positive Reframing](https://huggingface.co/datasets/SALT-NLP/positive_reframing)

##### *Why Positive Frames?* 

This work was inspired by the need to escape the negative patterns of thinking that began to overwhelm the authors during the COVID-19 pandemic. We realized that what we needed was not some naive belief that everything would be okay if we ignored our problems. Instead, we needed _reframing_, or a shift in focus, with less weight on the negative things we can't control, and more weight on the positive things about ourselves and our situation which we can control.

_Positive reframing_ induces a complementary positive viewpoint (e.g. glass-half-full), which nevertheless supports the underlying content of the original sentence (see diagram above). The reframe implicates rather than contradicts the source, and the transformation is motivated by theoretically justified strategies from positive psychology (see _What's 'in the box?'_).

Our work shows how NLP can help lead the way by automatically reframing overly negative text using strategies from positive psychology.

##### *What's 'in the box?'* 

The `Positive Psychology Frames` dataset contains **8,349** reframed sentence pairs, where the original sentence is drawn from a negative tweet (\#stressed), and a reframed copy is provided by a crowdworker who was trained in the methods of positive psychology. Our positive psychology frames taxonomy is defined below (with the distribution of labels shown on the left).

* ![25.4%](https://progress-bar.dev/25) **Growth Mindset:** Viewing a challenging event as an opportunity for the author specifically to grow or improve themselves.
* ![19.5%](https://progress-bar.dev/20) **Impermanence:** Saying bad things don't last forever, will get better soon, and/or that others have experienced similar struggles.
* ![36.1%](https://progress-bar.dev/36) **Neutralizing:** Replacing a negative word with a neutral word.
* ![48.7%](https://progress-bar.dev/49) **Optimism:** Focusing on things about the situation itself, in that moment, that are good (not just forecasting a better future).
* ![10.1%](https://progress-bar.dev/10) **Self-Affirmation:** Talking about what strengths the author already has, or the values they admire, like love, courage, perseverance, etc.
* ![13.0%](https://progress-bar.dev/13) **Thankfulness:** Expressing thankfulness or gratitude with key words like appreciate, glad that, thankful for, good thing, etc.


##### *What can I do with this data?* 

State-of-the-art neural models can learn from our data how to (1) shift a negatively distorted text into a more positive perspective using a combination of strategies from positive psychology; and (2) recognize or classify the psychological strategies that are used to reframe a given source. 

As our paper baselines show, neural models still have a long ways to go before they can reliably generate positive perspectives. We see particular errors from _insubstantial changes, contradictions to the premise, self-contradictions, and hallucinations_. Overall, our suggests that our dataset can serve as a useful benchmark for building natural language generation systems with positive perspectives.
