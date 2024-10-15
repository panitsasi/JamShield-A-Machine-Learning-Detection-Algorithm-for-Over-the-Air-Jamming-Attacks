# JamShield: A Machine Learning Detection Algorithm for Over-the-Air Jamming Attacks

This repository contains the dataset used in the research paper "**JamShield: A Machine Learning Detection Algorithm for Over-the-Air Jamming Attacks**." The research was conducted by Ioannis Panitsas, Yagmur Yigit, Leandros Tassiulas, and Leandros Maglaras from Yale University and Edinburgh Napier University.

For any inquiries, please contact Ioannis Panitsas at [ioannis.panitsas@yale.edu](mailto:ioannis.panitsas@yale.edu).

## Dataset

Each dataset corresponds to a specific jamming type. We have implemented three types of jammers: constant, random, and reactive, each with varying output power and different jamming signals. You can access the raw files in the `data` folder:

- [Constant Jammer](data/)
- [Random Jammer](data/)
- [Reactive Jammer](data/)


Each dataset file contains the following features:

| Feature Name                                             | Description                                                                                           |
|---------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| sample                                                  | Unique identifier for each data sample.                                                              |
| station                                                 | MAC Address for the station transmitting the data.                                                   |
| tx_total_pkts                                           | Total number of packets transmitted.                                                                  |
| tx_total_bytes                                          | Total number of bytes transmitted.                                                                     |
| tx_ucast_pkts                                           | Number of unicast packets transmitted.                                                                |
| tx_ucast_bytes                                          | Total bytes of unicast packets transmitted.                                                           |
| tx_mcast_bcast_pkts                                     | Number of multicast and broadcast packets transmitted.                                               |
| tx_mcast_bcast_bytes                                    | Total bytes of multicast and broadcast packets transmitted.                                           |
| tx_failures                                             | Number of transmission failures.                                                                      |
| rx_data_pkts                                            | Number of received data packets.                                                                       |
| rx_data_bytes                                           | Total number of bytes received in data packets.                                                      |
| rx_ucast_pkts                                           | Number of unicast packets received.                                                                    |
| rx_ucast_bytes                                          | Total bytes of unicast packets received.                                                               |
| rx_mcast_bcast_pkts                                     | Number of multicast and broadcast packets received.                                                   |
| rx_mcast_bcast_bytes                                    | Total bytes of multicast and broadcast packets received.                                              |
| rx_decrypt_succeeds                                     | Number of successful decryption attempts for received packets.                                        |
| tx_data_pkts_retried                                    | Number of data packets that were retried for transmission.                                           |
| tx_total_pkts_sent                                      | Total number of packets sent, including retransmissions.                                             |
| tx_pkts_retries                                         | Total number of packet retries during transmission.                                                  |
| tx_pkts_retry_exhausted                                 | Number of packets that reached their retry limit without successful transmission.                     |
| rx_total_pkts_retried                                   | Number of received packets that were retried during reception.                                        |
| rate_last_tx_pkt_min                                    | Minimum transmission rate for the last transmitted packet (in kbps).                                 |
| rate_last_tx_pkt_max                                    | Maximum transmission rate for the last transmitted packet (in kbps).                                 |
| per_antenna_rssi_last_rx_data_frame_1-4                 | RSSI for the last received data frame per antenna.                                                   |
| per_antenna_avg_rssi_rx_data_frames_1-4                 | Average RSSI for received data frames per antenna.                                                  |
| per_antenna_noise_floor_1-4                             | Noise floor measurements for each antenna.                                                            |
| sinr_per_antenna_1-4                                    | Signal-to-Interference-plus-Noise Ratio (SINR) per antenna
| attack                                                  | Indicator of whether an attack is present (1 for attack, 0 for normal operation).                    |


## Implementation
The jammers were implemented using GNURadio. Below is the flow graph used for this implementation.

**Flow Graph**
![Flow Graph](/flow_graph.jpg) 

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

