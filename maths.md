# Core Formulas


### 1. Single neuron

For one neuron:
<h3 align = 'center'>
𝑧 = 𝑋𝑊 + 𝑏 <br>
𝑎 = 𝑓(𝑧)
</h3>

Where:
- 𝑋 = input
- 𝑊 = weights
- 𝑏 = bias
- 𝑓 = activation
- 𝑎 = output

--- 

### 2. Hidden layer network

For a 2-layer network:

#### Hidden layer
<h3 align = 'center', size = '42'>
𝑍<sub>1</sub> = 𝑋𝑊<sub>1</sub> + 𝑏<sub>1</sub> <br>
𝐴<sub>1</sub> = 𝑓(𝑍<sub>1</sub>)
</h3>

#### Output layer
<h3 align = 'center'>
𝑍<sub>2</sub> = 𝐴<sub>1</sub>𝑊<sub>2</sub> + 𝑏<sub>2</sub> <br>  
ŷ = 𝑔(𝑍<sub>2</sub>)
</h3>

Where:
* 𝑓 can be sigmoid or ReLU
* 𝑔 can be sigmoid for binary classification

---
