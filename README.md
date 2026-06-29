## Introduction
This repository contains the official implementation of our **physics-informed semi-supervised learning (PISL) framework** for bearing degradation modeling and remaining useful life (RUL) prediction. 

## Dataset

**The XJTU-SY dataset** is utilized to validate the effectiveness and superiority of the proposed PISL framework. 

Given that the proposed framework is designed to extract a unified degradation pattern and estimate a shared physical failure threshold for similar components, it is imperative to utilize bearings that share a common degradation behavior. Consequently, **six specific bearings (namely 1-2, 2-2, 1-3, 3-5, 2-5, and 3-1)** exclusively exhibiting outer race faults are selected from the dataset for the subsequent experiments. To establish a rigorous standard for data annotation, a relative failure criterion consistent with the original data collection protocol is adopted. A bearing is deemed to have failed when its maximum vibration amplitude in either direction exceeds seven times the historical maximum amplitude recorded during its normal operating phase. Any data collected subsequent to this point is labeled as fault data. Consequently, the specific amplitude failure thresholds for the six selected sequences are definitively determined as 25.9, 18.9, 17.5, 31.5, 21.0, and 31.5. The dataset is strategically partitioned based on these thresholds as shown in the table below.

**Training set:** Three bearings (1-2, 2-2, and 3-1) are designated as historically failed bearings, providing full run-to-failure data. For these bearings, the initial stable segment is labeled as normal data, data after the threshold is labeled as fault data, and the intermediate segment is treated as unlabeled data.

**Testing Set:** The remaining three bearings are treated as in-service (non-failed) bearings to evaluate degradation modeling and RUL prediction capabilities, with their health states completely hidden during training.

<table border="1" align="center" style="margin: auto; text-align: center;">
    <thead>
        <tr style="text-align: center;">
            <th rowspan="2" style="text-align: center; padding: 10px;">Dataset</th>
            <th rowspan="2" style="text-align: center; padding: 10px;">NO.</th>
            <th rowspan="2" style="text-align: center; padding: 10px;">Bearing</th>
            <th rowspan="2" style="text-align: center; padding: 10px;">Total samples</th>
            <th colspan="3" style="text-align: center; padding: 10px;">Time range (min)</th>
            <th rowspan="2" style="text-align: center; padding: 10px;">EOL</th>
        </tr>
        <tr style="text-align: center;">
            <th style="text-align: center; padding: 5px;">Normal</th>
            <th style="text-align: center; padding: 5px;">Unknown</th>
            <th style="text-align: center; padding: 5px;">Fault</th>
        </tr>
    </thead>
    <tbody>
        <!-- Train Set -->
        <tr style="text-align: center;">
            <td rowspan="3" style="text-align: center; font-weight: bold;">Train</td>
            <td style="text-align: center;">0</td>
            <td style="text-align: center;">Bearing 1_2</td>
            <td style="text-align: center;">161</td>
            <td style="text-align: center;">1-20</td>
            <td style="text-align: center;">21-124</td>
            <td style="text-align: center;">125-161</td>
            <td style="text-align: center;">125</td>
        </tr>
        <tr style="text-align: center;">
            <td style="text-align: center;">1</td>
            <td style="text-align: center;">Bearing 2_2</td>
            <td style="text-align: center;">161</td>
            <td style="text-align: center;">1-30</td>
            <td style="text-align: center;">31-115</td>
            <td style="text-align: center;">116-161</td>
            <td style="text-align: center;">116</td>
        </tr>
        <tr style="text-align: center;">
            <td style="text-align: center;">2</td>
            <td style="text-align: center;">Bearing 1_3</td>
            <td style="text-align: center;">158</td>
            <td style="text-align: center;">1-40</td>
            <td style="text-align: center;">41-147</td>
            <td style="text-align: center;">148-158</td>
            <td style="text-align: center;">148</td>
        </tr>
        <!-- Test Set -->
        <tr style="text-align: center;">
            <td rowspan="3" style="text-align: center; font-weight: bold;">Test</td>
            <td style="text-align: center;">3</td>
            <td style="text-align: center;">Bearing 3_5</td>
            <td style="text-align: center;">70</td>
            <td colspan="3" style="text-align: center;">1-70</td>
            <td style="text-align: center;">74</td>
        </tr>
        <tr style="text-align: center;">
            <td style="text-align: center;">4</td>
            <td style="text-align: center;">Bearing 2_5</td>
            <td style="text-align: center;">260</td>
            <td colspan="3" style="text-align: center;">1-260</td>
            <td style="text-align: center;">262</td>
        </tr>
        <tr style="text-align: center;">
            <td style="text-align: center;">5</td>
            <td style="text-align: center;">Bearing 3_1</td>
            <td style="text-align: center;">170</td>
            <td colspan="3" style="text-align: center;">2350-2520</td>
            <td style="text-align: center;">2524</td>
        </tr>
    </tbody>
</table>

## Demostration
A demonstration video which illustrates the reconstruction process can be viewed at: https://pisl-for-rul-prediction.oss-cn-hangzhou.aliyuncs.com/demo_PISL_RUL_6.0.mp4

<img width="2238" height="1048" alt="image" src="https://github.com/user-attachments/assets/4f4ef2a3-69fb-4e68-a035-3ee3ff733c94" />


## Future Updates
The code will be made available in this repository.
