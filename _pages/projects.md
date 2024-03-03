---
permalink: /projects/
title: "Projects"
---

As part of my research agenda, one key focus is conducting applied research in domains like Software Engineering 
for Artificial Intelligence (SE4AI). This endeavor often necessitates coding and the development of libraries. Below, 
I present a selection of my works—projects I've undertaken during my studies or tools I've created to streamline 
repetitive tasks.

# DRLDebugger

{% include gallery %}

[<img src="https://img.shields.io/badge/license-Apache 2.0-blue">](https://github.com/rached1997/RLDebugger)
[![Code style: black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)

This package provides a debugging tool for Deep Reinforcement Learning (DRL) frameworks,
designed to detect and address DNN and RL issues that may arise during training.
The tool allows you to monitor your training process in real-time, identifying any
potential flaws and making it easier to improve the performance of your DRL models.

The implementation is clean and simple, with research-friendly features. The highlight features of DRLDebugger are:

* 📜 Straightforward integration
  * DRLDebugger can be integrated into your project with a few lines of code.
* 🗳️ DNN + RL checks
* 🛃 Custom checks
* 🖥️ Real-time warnings
* 📈 Monitoring using [Weights and Biases](https://wandb.ai/site)

## Get started

Prerequisites:
* Python >=3.7.7,<3.10 (not yet tested on 3.10)

Step 1. Install the debugger in your python environment:
```bash
git clone https://github.com/rached1997/RLDebugger.git && cd RLDebugger
pip install -e .
```

Step 2. Create a .yml config file and copy the following lines:
```yml
debugger:
  name: 'Debugger'
  kwargs:
    observed_params:
      constant: []
      variable: []
    check_type:
      - name: #Checker_Name_1
      - name: #Checker_Name_2
```

Step 3. Set up the config and run the debugger:

```python
from debugger import rl_debugger

rl_debugger.set_config(config_path="the path to your debugger config.yml file")

...

rl_debugger.debug(model=...,
                  max_total_steps=...,
                  targets=...,
                  action_probs=....
                  )
```

For detailed steps on how to use the debugger, please refer to [GitHub](https://github.com/rached1997/RLDebugger).