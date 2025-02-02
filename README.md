# A Study on the Effectiveness of the Class Imbalance of Training Data on Convolutional Networks(CNNs)
Experiment about class imbalance problems inside the CNNs

# Prerequistes
1. pytorch, python : pytorch 1.0 ↑, python 3.7 ↑
2. package : numpy, os

# Measures Definition
1. Neuron Membership
<table align='center'>
<tr align='center'>
</tr>
<tr>
<td><img src = 'images/neuron membership.png' height = '400px'></td>
</tr>
</table>
2. Major class actvation - Minor class activation
3. Class Selectivity
<table align='center'>
<tr align='center'>
</tr>
<tr>
<td><img src = 'images/class_selectivity.png' height = '400px'></td>
</tr>
</table>

# Dataset / Model
1. Data : Cifar10 with different imbalance ratio
  <table> 
    <thead> 
     <tr> 
      <th rowspan=2>Dataset</th>
      <th colspan=4>Cifar10</th>
     </tr>
     <tr> 
      <th>Major / Minor</th>
      <th>Major class images per group</th>
      <th>Minor class images per group</th>
      <th>Accuracy</th>
     </tr>
    </thead> 
    <tbody align='center'> 
     <tr> 
      <td>Balanced</td>
      <td rowspan=4>[0~4] / [5~9]</td>
      <td rowspan=4>5000</td>
      <td>5000</td>
      <td>91.29</td>
     </tr>
     <tr> 
      <td>Imbalance 20</td>
      <td>250</td>
      <td>68.93</td>
     </tr>
     <tr> 
      <td>Imbalance 50</td>
      <td>100</td>
      <td>58.51</td>
     </tr>
     <tr> 
      <td>Imbalance 100</td>
      <td>50</td>
      <td>52.45</td>
     </tr>
    </tbody> 
</table>


2. Model : Vgg11 with batch normalization

# Experiment Result
1. Neuron Membership 
<table align='center'>
<tr align='center'>
</tr>
<tr>
<td><img src = 'images/neuron_membership_result.png' height = '400px'></td>
</tr>
</table>

2. Major class actvation - Minor class activation 
<table align='center'>
<tr align='center'>
</tr>
<tr>
<td><img src = 'images/ma-mi_result.png' height = '400px'></td>
</tr>
</table>

3. Class Selectivity
<table align='center'>
<tr align='center'>
</tr>
<tr>
<td><img src = 'images/class_selectivity_result.png' height = '400px'></td>
</tr>
</table>
