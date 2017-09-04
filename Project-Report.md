# Extended Kalman Filter Project
Self-Driving Car Engineer Nanodegree Program

In this project I will utilize a kalman filter to estimate the state of a moving object of interest with noisy lidar and radar measurements. 

## Results Compared
#### Dateset 1
| RMSM  | Fusion with Radar and Lidar | Only Lidar | Only Radar |
|:-------:|:-------:|:-------:|:-------:|
| X | 0.0974 | 0.1474 | 0.2250 |
| Y | 0.0855 | 0.1154 | 0.3464 |
| Vx | 0.4517 | 0.6390 | 0.5781 |
| Vy | 0.4404 | 0.5351 | 0.8227 |

#### Dateset 2
| RMSM  | Fusion with Radar and Lidar | Only Lidar | Only Radar |
|:-------:|:-------:|:-------:|:-------:|
| X | 0.0726 | 0.1210 | 0.2684 |
| Y | 0.0963 | 0.1268 | 0.3844 |
| Vx | 0.3978 | 0.6639 | 0.5640 |
| Vy | 0.4840 | 0.5496 | 0.8264 |

The results  show that using lidar only has a better performance than using radar only at estimating position, since lidar has less noisy measurements. But at estimating velocity, they both are comparable. Radar can measure the speed information directly which make up for the larger measurement noise.
Through fusing lidar and radar data, the algorithm can not only have a relative lower noisy measurements, but also have the speed information directly. Therefore, the fusion algorithm is able to make better predictions.