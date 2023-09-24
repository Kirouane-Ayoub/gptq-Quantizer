# Project Name: gptq-Quantizer

## Description:
**GPTQ-Quantizer** is a Python package that simplifies the process of post-training quantization for Generative Pre-trained Transformer (GPT) models. It automates the GPTQ quantization algorithm, allowing you to quantize GPT models quickly and efficiently.

## Key Features:

+ **Automated GPTQ quantization**: Quantize GPT models effortlessly with just a few lines of code.
+ **Easy model loading**: Load the quantized GPT model with minimal code complexity.
+ **State-of-the-art results**: Benefit from the accuracy improvements of GPTQ quantization.
+ **Reduced model size**: Deploy smaller GPT models for resource-constrained environments.
+ **Faster inference**: Enjoy faster model inference with reduced arithmetic operations.
+ **Lower power consumption**: Ideal for battery-powered devices.


## Get started with gptq-Quantizer

### Installation:
```
pip install gptq-Quantizer==1.0
```

### Usage

**Quantization :**


```python
from gptq_Quantizer import gptq_Quantizer
llm_quantizer = gptq_Quantizer.Quantizer("facebook/opt-125m" )
llm_quantizer.run(
    bits=4,  # Number of bits for quantization (e.g., 4 bits)
    block_name_to_quantize="model.decoder.layers",  # Name of the block to be quantized
    model_seqlen=2048,  # Maximum sequence length of the model (e.g., 2048)
    save_folder="new_model/"  # Folder where the quantized model will be saved
)
```

**Load the Quantized Model :** 

```python
from gptq_Quantizer.utils import Load
quantized_model = Load(
    model_name="facebook/opt-125m",  # Name of the quantized model to load (e.g., "facebook/opt-125m")
    save_folder="/content/new_model"  # Folder where the quantized model is located
)
```
