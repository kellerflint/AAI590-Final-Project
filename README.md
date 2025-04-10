# AAI590-Final-Project


### GPU Steps

From Anaconda Prompt:

```bash
conda create -n tf-gpu python=3.10
```

```bash
conda activate tf-gpu
```

```bash
conda install -c conda-forge cudatoolkit=11.2 cudnn=8.1
```

```bash
python -m pip install "tensorflow<2.11"
```

```bash
pip uninstall numpy
pip install numpy==1.26.4
```

From the activated conda env, run python. Then run each of these lines.
```python
import tensorflow as tf
print("Available GPUs:", tf.config.list_physical_devices('GPU'))
```

Then to get it to work for VS Code (from the env still):
```bash
conda install jupyter ipykernel
```

```bash
python -m ipykernel install --user --name=tf-gpu --display-name "Python (tf-gpu)"
```

Then you have to launch code/cursor from the activated anaconda enviornemnt
```bash
conda activate tf-gpu
code
```

Then when you go to select the kernel you should have a "Jupyter Kernel" option and in there will be the "Python (tf-gpu)". Select that.

Then you can run these in the notebook
```python
import tensorflow as tf
print("Available GPUs:", tf.config.list_physical_devices('GPU'))
```
And it should list a device.


### Requirements
```bash
pip install tensorflow-datasets
pip install matplotlib
pip install scikit-learn
pip install seaborn
```