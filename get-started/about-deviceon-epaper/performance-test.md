---
icon: chart-line-up
---

# Performance Test

## Test Machine

<table><thead><tr><th width="348">Name</th><th width="166">DeviceOn/ePaper</th><th width="80">vCPU</th><th>Memory (GB)</th></tr></thead><tbody><tr><td>Azure Virtual Machine Standard D2s v5</td><td>v3.2.0</td><td>2</td><td>8</td></tr><tr><td>Azure Virtual Machine Standard D4s v5</td><td>v3.2.0</td><td>4</td><td>16</td></tr></tbody></table>

## Connection & Auto-report Test

#### Test Condition

We performed stress tests utilizing Azure virtual machines (**Standard D2s v5 and Standard D4s v5**) with different quantities of EPD devices, connecting them to the server within **a one-hour window**. During the test, each device continuously transmitted **report data** at **one-minute intervals**, assessing the system's capacity to handle ongoing data reporting under varying loads.

#### Summary

The **Standard D2s v5** and **Standard** **D4s v5** virtual machines are capable of supporting up to **2,500 and 7,000 devices** per hour, respectively, providing scalable performance to meet varying operational demands.

#### Results

* **Standard D2s v5**

<table><thead><tr><th width="204">Connected Devices</th><th width="123">Auto-report</th><th width="82">Time</th><th width="99">Result</th><th>Note</th></tr></thead><tbody><tr><td><mark style="color:blue;">2500</mark></td><td><mark style="color:blue;">1 min</mark></td><td><mark style="color:blue;">1 hr</mark></td><td><mark style="color:blue;">Success</mark></td><td></td></tr><tr><td>3000</td><td>1 min</td><td>1 hr</td><td>Failed</td><td>Packet loss in MongoDB, receiving 98.5% of the data.</td></tr></tbody></table>

* **Standard** **D4s v5**

<table><thead><tr><th width="201">Connected Devices</th><th width="123">Auto-report</th><th width="80">Time</th><th width="99">Result</th><th>Note</th></tr></thead><tbody><tr><td>5000</td><td>1 min</td><td>1 hr</td><td>Success</td><td></td></tr><tr><td><mark style="color:blue;">7000</mark></td><td><mark style="color:blue;">1 min</mark></td><td><mark style="color:blue;">1 hr</mark></td><td><mark style="color:blue;">Success</mark></td><td></td></tr><tr><td>8000</td><td>1 min</td><td>1 hr</td><td>Failed</td><td>Packet loss in MongoDB, receiving 98.9% of the data.</td></tr><tr><td>10000</td><td>1 min</td><td>1 hr</td><td>Failed</td><td></td></tr></tbody></table>

## Transmit Image Schedule Test

#### Test Condition

We performed tests using Azure virtual machines with different quantities of EPD devices, transmitting **2MB images** over intervals of **10 minutes**, **30 minutes**, and **1 hour**. These tests aimed to evaluate the system's performance under varying transfer loads and to determine the maximum number of EPD devices that could be supported efficiently during image transmission.

#### Summary

* **D2s v5:**
  * Maximum supported devices for the 10-minute image transfer schedule: **500**
  * Maximum supported devices for the 30-minute image transfer schedule: **1,400**
* **D4s v5:**
  * Maximum supported devices for the 10-minute image transfer schedule: **800**
  * Maximum supported devices for the 30-minute image transfer schedule: **2,000**
  * Maximum supported devices for the 1-hour image transfer schedule: **3,500**

#### Results

* **Standard D2s v5 for the 10-minutes schedule**

<table><thead><tr><th width="194">Connected Devices</th><th width="153">Time per batch</th><th width="82">Batch</th><th width="101">Result</th><th>Note</th></tr></thead><tbody><tr><td>200</td><td>3 min</td><td>104</td><td>Success</td><td></td></tr><tr><td><mark style="color:blue;">500</mark></td><td><mark style="color:blue;">7 min</mark></td><td><mark style="color:blue;">30</mark></td><td><mark style="color:blue;">Success</mark></td><td></td></tr><tr><td>700</td><td>9 min</td><td>18</td><td>Failed</td><td>Packet loss in MongoDB, receiving 98.16% of the data.</td></tr></tbody></table>

* **Standard D2s v5 for the 30-minutes schedule**

<table><thead><tr><th width="193">Connected Devices</th><th width="153">Time per batch</th><th width="82">Batch</th><th width="101">Result</th><th>Note</th></tr></thead><tbody><tr><td><mark style="color:blue;">1400</mark></td><td><mark style="color:blue;">21 min</mark></td><td><mark style="color:blue;">15</mark></td><td><mark style="color:blue;">Success</mark></td><td></td></tr><tr><td>1600</td><td>21 min</td><td>16</td><td>Failed</td><td>Packet loss in MongoDB, receiving 99.15% of the data.</td></tr><tr><td>1800</td><td>24 min</td><td>9</td><td>Failed</td><td></td></tr><tr><td>2000</td><td>27 min</td><td>4</td><td>Failed</td><td>Packet loss in MongoDB, receiving 97.52% of the data.</td></tr></tbody></table>

* **Standard D4s v5 for the 10-minutes schedule**

<table><thead><tr><th width="194">Connected Devices</th><th width="153">Time per batch</th><th width="82">Batch</th><th width="101">Result</th><th>Note</th></tr></thead><tbody><tr><td><mark style="color:blue;">800</mark></td><td><mark style="color:blue;">9 min</mark></td><td><mark style="color:blue;">24</mark></td><td><mark style="color:blue;">Success</mark></td><td></td></tr><tr><td>900</td><td>11 min</td><td>4</td><td>Failed</td><td>Time per batch exceeds 10-minutes schedule</td></tr></tbody></table>

* **Standard D2s v5 for the 30-minutes schedule**

<table><thead><tr><th width="188">Connected Devices</th><th width="153">Time per batch</th><th width="82">Batch</th><th width="101">Result</th><th>Note</th></tr></thead><tbody><tr><td><mark style="color:blue;">2000</mark></td><td><mark style="color:blue;">22 min</mark></td><td><mark style="color:blue;">28</mark></td><td><mark style="color:blue;">Success</mark></td><td></td></tr><tr><td>2500</td><td>37 min</td><td>1</td><td>Failed</td><td>Time per batch exceeds 30-minutes schedule</td></tr></tbody></table>

* **Standard D4s v5 for the 1-hr schedule**

<table><thead><tr><th width="188">Connected Devices</th><th width="153">Time per batch</th><th width="82">Batch</th><th width="101">Result</th><th>Note</th></tr></thead><tbody><tr><td><mark style="color:blue;">3500</mark></td><td><mark style="color:blue;">41 min</mark></td><td><mark style="color:blue;">12</mark></td><td><mark style="color:blue;">Success</mark></td><td></td></tr><tr><td>4000</td><td>47 min</td><td>3</td><td>Failed</td><td>Packet loss in MongoDB after 3 hours</td></tr><tr><td>5000</td><td>-</td><td>1</td><td>Failed</td><td></td></tr></tbody></table>

