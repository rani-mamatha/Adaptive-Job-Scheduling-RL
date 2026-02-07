# RLbDS – Reinforcement Learning Based Dynamic Job Scheduling

## Overview

This repository contains an implementation of a **Reinforcement Learning based Dynamic Scheduling (RLbDS)** framework for large-scale job scheduling. The system formulates job scheduling as a Markov Decision Process and applies a **Deep Q-Network (DQN)** agent to learn optimal scheduling policies under dynamic workloads.

The implementation evaluates the proposed RL-based scheduler against classical baseline strategies using **2000-job** and **5000-job** workloads.

---

## Key Contributions

The project demonstrates how deep reinforcement learning can be used to dynamically allocate jobs to resources in a scheduling environment. It provides:

- A custom scheduling environment modeling job queues and system states
- A DQN-based agent for adaptive scheduling decisions
- Baseline scheduling policies for comparison
- Scalability experiments on different workload sizes
- Visualization of scheduling performance

---

## Project Structure

```
Mamatha Rani/
└── Implementation/
    ├── 2000 Jobs/
    │   ├── Agent.py
    │   ├── AgentOthers.py
    │   ├── MyEnv1.py
    │   ├── Main.py
    │   └── JOB_Scheduling_2000_jobs.ipynb
    └── 5000 Jobs/
        ├── Agent.py
        ├── AgentOthers.py
        ├── MyEnv1.py
        ├── Main.py
        └── JOB_Scheduling_5000_jobs.ipynb
```

---

## Core Components

### Scheduling Environment

- `MyEnv1.py` defines the custom scheduling environment.
- It models system states, available actions, reward computation, and job transitions.
- The environment exposes the state space and action space required by the RL agent.

---

### Reinforcement Learning Agent

- `Agent.py` implements a **Deep Q-Network (DQN)** agent.
- The agent learns an optimal scheduling policy by interacting with the environment and maximizing cumulative reward.
- Key elements include experience replay, Q-value approximation, and action selection.

---

### Baseline Scheduling Policies

`AgentOthers.py` implements traditional scheduling strategies used for comparison:

- Random scheduling
- Round-robin scheduling
- Earliest job scheduling

These baselines help quantify the improvement achieved by the RL-based approach.

---

### Execution Script

- `Main.py` acts as the entry point for experiments.
- It initializes the environment, selects the scheduling policy, runs simulations, and collects performance metrics.

---

### Jupyter Notebooks

- `JOB_Scheduling_2000_jobs.ipynb`
- `JOB_Scheduling_5000_jobs.ipynb`

These notebooks provide an interactive way to run experiments, visualize results, and analyze scheduler performance for different workload sizes.

---

## Experimental Setup

Two workload configurations are evaluated:

- **2000 Jobs** scenario for moderate-scale testing
- **5000 Jobs** scenario for scalability analysis

Each configuration compares DQN-based scheduling with baseline policies under identical conditions.

---

## How to Run

### Requirements

- Python 3.8 or later
- NumPy
- Matplotlib
- Jupyter Notebook

Install dependencies using:

```bash
pip install numpy matplotlib notebook
```

---

### Running from Script

Navigate to the desired workload directory and run:

```bash
python Main.py
```

---

### Running from Notebook

Open the corresponding notebook and run all cells:

```bash
jupyter notebook JOB_Scheduling_2000_jobs.ipynb
```

or

```bash
jupyter notebook JOB_Scheduling_5000_jobs.ipynb
```

---

## Results and Observations

The DQN-based scheduler consistently adapts to dynamic workloads and demonstrates improved scheduling efficiency compared to static baseline strategies. Performance gains become more evident as the number of jobs increases, highlighting the scalability of reinforcement learning for scheduling problems.

---

## Applications

- Cloud and edge computing job scheduling
- Data center resource management
- Real-time task allocation systems
- Research on adaptive scheduling using reinforcement learning

---

## License

This project is intended for academic and research use.

---

## Future Enhancements

Potential areas for further development:

- Integration with real-world cloud platforms
- Multi-objective optimization (energy efficiency, fairness)
- Advanced RL algorithms (A3C, PPO, Rainbow DQN)
- Larger-scale experiments with 10,000+ jobs
- Comparative analysis with other ML approaches

---

## Contact

For questions or collaboration opportunities, please open an issue in this repository.
