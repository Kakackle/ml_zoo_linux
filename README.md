# ML zoo projects with TensorFlow on GPU
Existant as a separate repository from the main [ml_zoo repo](github.com/Kakackle/ml_zoo) because of the need to use WSL2 / linux for GPU support to work on tensorflow versions above 2.10 (quite outdated at this point)

In case of any errors detecting the GPU, you can use: [this answer](https://stackoverflow.com/questions/69917132/could-not-load-dynamic-library-libcudart-so-11-0-in-conda-enviroment)

Otherwise it might be necessary to activate the conda environment (altough it shouldn't as the kernel is installed in jupyter)

Then to check whether a GPU device is indeed available:

```python
print(tf.config.list_physical_devices('GPU'))
```

To install dependencies with conda:

```
    conda env create -f environment.yaml
```