---
title: Home
---

# Bridging the Gap between Neural and Symbolic World Models for Robot Planning, Reasoning, and Action

{% include figure.html img="workshop_banner.png" alt="banner image here" caption="" width="75%" %}


## Abstract
World models have emerged as a central paradigm in robot learning, planning, and reasoning. Yet, the term spans different meanings across communities. Specifically, high-dimensional neural models that predict future latent states (e.g., DreamerV3 [1], World Models [45]) and symbolic state transition systems (e.g. PDDL-style models) [2], [24], [46]. Each has distinct limitations: neural models often suffer from data inefficiency, while symbolic systems require extensive domain engineering. Integrating high-dimensional neural state representations with symbolic state abstractions may mitigate these limitations by leveraging the strengths of both frameworks. However, it is unclear how to combine them, as shown in recent world model-related [4–21] workshops, including at IROS 2024–2025 [17–21]. These workshops have highlighted neural approaches or the use of neural methods to induce symbolic models [24]. Moreover, we must look past overemphasized policy-centric frameworks, such as Vision-Language-Action models [3], and investigate the limits of state estimation in world models. Consequently, this workshop focuses on the intersection between neural and symbolic world models for robot planning and decision-making.

We aim to bring together researchers across neural, symbolic, and hybrid communities to clarify terminology, align assumptions, and identify shared challenges. Ideally, this will elicit methods with improved data efficiency, generalization, interpretability, and long-horizon reasoning. These attributes will help tackle complex, high-precision domains, where structured task knowledge and state prediction are critical. By positioning world models as explicit components of robotic systems, alongside planning and policy learning, this workshop seeks to articulate new principles for hybrid world modeling in robotics.


## Objectives
The following non-exhaustive list of questions is intended to stimulate dialogue and outline the workshop's core objectives. They provide a thematic framework for potential contributors. While comprehensive solutions are encouraged, these prompts serve primarily to define the scope and inspire diverse research directions.

* How can neural and symbolic perspectives be formally related or unified into world models for robotics? 
  * How can neural world model architectures be integrated with symbolic priors and planning tools for improved, long-horizon reasoning, data-efficiency, and generalization?
  * How can symbolic world models be enhanced by high-dimensional latent world models for symbol and predicate extraction and improved interpretability of latent embeddings?
  * How can symbolic planners be used for data collection to train neural world models for trajectory generation, data collection, and safe exploration?
* How can different types of world models interact with each other?
  * What are the benefits and drawbacks of combining neural and symbolic models? Is there a principled way to do so?
* How does the task application dictate the type of world model used?
  * How do we differentiate between classes of tasks for world models? How do we transition world models from simple tasks to complex tasks, such as those present in manufacturing domains?
  * What hybrid architectures (e.g., latent dynamics + symbolic constraint module, neuro-symbolic graph networks, neuro-symbolic program induction) are most effective across robotics tasks, especially those requiring high precision?
* How do world models differ in terms of their horizon limit and coarseness level? 
* What benchmarks and metrics define a 'sufficient' world model, and how can we rigorously evaluate hybrid architectures across the axes of modeling fidelity, diverse task success, and deployment readiness?


## Speakers

<div class="people-grid-container">
  {% for person in site.data.speakers %}
    <div class="person">
      <div class="circle-crop-wrapper">
        <img src="{{ person.image | relative_url }}" alt="{{ person.name }}"
          {% if person.position %}
            style="object-position: {{ person.position }};"
          {% endif %}>
      </div>
      <h3>{{ person.name }}</h3>
      <p>{{ person.role }}</p>
      <p>{{ person.affiliation }}</p>
    </div>
  {% endfor %}
</div>