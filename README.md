# RNNs
This is the code written as part of my Assignment in the course Deep Learning.

Here, Elman Network, LSTM and GRU models are trained.

In this task, each data sample consists of a sequence of variable length, but a constant depth of 2. All values of the first dimension (randomly) lie in [0, 1], and the second dimension being all zeros except for two elements that are marked by 1. Objective of the task is to sum the random values whose second dimensions are marked by 1. Here different RNNs (Elmon network, LSTM, and GRU) are trained.<br>
The following table presents two data samples (x) along with their labels (y).The samples in this case are of different lengths (n), so the dimensions of each sample can be represented as
n × 2. Below example have lengths of 5 and 8 respectively.

<img width="682" alt="Screenshot 2023-06-10 213514" src="https://github.com/JBA-12/RNNs/assets/102513876/852ca8d8-7ec7-43fe-abc0-534bf0073f9d">

A dataset (of size ≥ 5000) is first generated and then the RNN models are trained, tested and compared.
Using the inbuilt numpy random functions the dataset of size 7521 is generated and then the data is split into train data and test data.

*Elman Network*: In the forward pass of Elman we have,<br>
         i) Start with h<sub>0</sub> = 0<br>
         ii) h<sub>t</sub> = tanh(W<sub>xh</sub>.x<sub>t</sub> + W<sub>hh</sub>.h<sub>t-1</sub> + b<sub>h</sub>)<br>
         iii) y<sub>t</sub> = softmax(W<sub>hy</sub>.h<sub> + b<sub>y</sub><br>

 *GRU*: In the forward pass of GRU we have,
         i) Start with h<sub>0</sub> = 0<br>
         ii) z = σ(W<sub>z</sub>.[h<sub>t-1</sub>, x<sub>t</sub><br>
