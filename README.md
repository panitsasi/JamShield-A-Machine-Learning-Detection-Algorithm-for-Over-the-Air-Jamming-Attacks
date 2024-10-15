# JamShield: A Machine Learning Detection Algorithm for Over-the-Air Jamming Attacks

This repository contains the dataset used in the research paper "**JamShield: A Machine Learning Detection Algorithm for Over-the-Air Jamming Attacks**." The research was conducted by Ioannis Panitsas, Yagmur Yigit, Leandros Tassiulas, and Leandros Maglaras from Yale University and Edinburgh Napier University.

For any inquiries, please contact Ioannis Panitsas at [ioannis.panitsas@yale.edu](mailto:ioannis.panitsas@yale.edu).

## Dataset

Each dataset corresponds to a specific jamming type. You can access the raw files in the `data` folder:

- [Normal Channel](data/normal_channel.csv)
- [Constant Jammer](data/constant_jammer.csv)
- [Random Jammer](data/random_jammer.csv)

Each dataset file contains the following columns:

- Received Signal Strength (RSS)
- Jamming Signals

For more information on how the data was collected, please refer to the published paper.

## Implementation

The code was initially implemented in GNURadio and later converted to Python. Below is the flow graph used for the implementation.

**Flow Graph**
![Flow Graph](path/to/your/flow_graph_image.png) <!-- Add your flow graph image here -->

Please refer to the published paper for more details about the setup and the parameters used in the flow graph and code.

## Testbed Setup and Reference Scenarios

The testbed setup for the experiments is illustrated below:

![Testbed Setup](testbed_setup.png) <!-- Your testbed setup image -->

### Reference Scenarios

The following images demonstrate the scenarios used during the experiments:

#### Line of Sight (LOS) Scenario
![LOS Scenario](LOS_scenario.png)

#### Non-Line of Sight (NLOS) Scenario
![NLOS Scenario](NLOS_scenario.png)

### Additional Scenarios
![Channels](channels.png)
![Edge Server](edge_server.png)
![Noise](noise.png)

## Citing This Work

When using this dataset, please cite the paper as follows:

