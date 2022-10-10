# Use EDGE TPU with YOLO on Windows

## Installation

### 1. Install the Edge TPU runtime

I advise to install the last version of 13th version of the **EdgeTPU runtime**. It seems that the 14th version is not 
working well on Windows.
https://coral.ai/docs/accelerator/get-started/#runtime-on-windows

Versions of **EdgeTPU runtime**:
https://coral.ai/software/#edgetpu-runtime

### 2. Install the PyCoral library

https://coral.ai/docs/accelerator/get-started/#pycoral-on-mac-win

Versions of Pycoral API.
https://coral.ai/software/#pycoral-api


Use a 3.9 version of Python :
```
conda create -n coral_env python=3.9
conda activate coral_env
python -m pip install --extra-index-url https://github.com/google-coral/pycoral/releases/download/v2.0.0/pycoral-2.0.0-cp39-cp39-win_amd64.whl pycoral~=2.0
```

### Install tflite runtime package

```
python pip install tflite-runtime==2.5.0.post1
```

## Model conversion

Convert the model following the `edgetpu_compiler.ipynb` on Google Colab.

## Utilisation

To get started, try using **edgetpu-yolo/detect.py** code :

```
python detect.py \
  --model {model_name}edgetpu.tflite \
  --input {photo_path}.jpg
```

<hr> 

### Bibligoraphy

This repository is a fork of **edgetpu-yolo** from **jveitchmichaelis**.

[1] https://github.com/jveitchmichaelis/edgetpu-yolo    
[2] https://coral.ai/docs/accelerator/get-started
