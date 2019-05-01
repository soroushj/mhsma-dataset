# MHSMA: The Modified Human Sperm Morphology Analysis Dataset

The MHSMA dataset is a collection of human sperm images from 235 patients with male factor infertility.
Each image is labeled by experts for normal or abnormal sperm acrosome, head, vacuole, and tail.

The training, validation, and test sets contain 1000, 240, and 300 images, respectively.

Images are available in two different crop sizes: 128x128- and 64x64-pixel.
The following figure shows two versions of the same sample.

| 128x128-pixel                                         | 64x64-pixel                                         |
| :---------------------------------------------------: | :-------------------------------------------------: |
| ![Sample from MHSMA-128](sample/mhsma-128-sample.png) | ![Sample from MHSMA-64](sample/mhsma-64-sample.png) |

Each sample is a grayscale image capturing a single sperm.
The head of the sperm is roughly located at the center of the image.
Also, the sperm tail is not entirely visible in the images.

Labels can be either `0` (normal, positive) or `1` (abnormal, negative).

The dataset is available in `.npy` format.
You can load the `.npy` files using [numpy.load](https://docs.scipy.org/doc/numpy/reference/generated/numpy.load.html).
The details of the files are described in the table below.

| File                   | Shape              | Type    | Description                           |
| :--------------------- | :----------------- | :------ | :------------------------------------ |
| `x_128_train.npy`      | `(1000, 128, 128)` | `uint8` | Training set, 128x128-pixel version   |
| `x_128_valid.npy`      | `(240, 128, 128)`  | `uint8` | Validation set, 128x128-pixel version |
| `x_128_test.npy`       | `(300, 128, 128)`  | `uint8` | Test set, 128x128-pixel version       |
| `x_64_train.npy`       | `(1000, 64, 64)`   | `uint8` | Training set, 64x64-pixel version     |
| `x_64_valid.npy`       | `(240, 64, 64)`    | `uint8` | Validation set, 64x64-pixel version   |
| `x_64_test.npy`        | `(300, 64, 64)`    | `uint8` | Test set, 64x64-pixel version         |
| `y_acrosome_train.npy` | `(1000,)`          | `uint8` | Training set labels for acrosome      |
| `y_acrosome_valid.npy` | `(240,)`           | `uint8` | Validation set labels for acrosome    |
| `y_acrosome_test.npy`  | `(300,)`           | `uint8` | Test set labels for acrosome          |
| `y_head_train.npy`     | `(1000,)`          | `uint8` | Training set labels for head          |
| `y_head_valid.npy`     | `(240,)`           | `uint8` | Validation set labels for head        |
| `y_head_test.npy`      | `(300,)`           | `uint8` | Test set labels for head              |
| `y_vacuole_train.npy`  | `(1000,)`          | `uint8` | Training set labels for vacuole       |
| `y_vacuole_valid.npy`  | `(240,)`           | `uint8` | Validation set labels for vacuole     |
| `y_vacuole_test.npy`   | `(300,)`           | `uint8` | Test set labels for vacuole           |
| `y_tail_train.npy`     | `(1000,)`          | `uint8` | Training set labels for tail          |
| `y_tail_valid.npy`     | `(240,)`           | `uint8` | Validation set labels for tail        |
| `y_tail_test.npy`      | `(300,)`           | `uint8` | Test set labels for tail              |

## Citing

If you use this dataset in your research, please kindly cite [our work](https://doi.org/10.1016/j.compbiomed.2019.04.030) as:

```bibtex
@article{javadi2019novel,
  title={A novel deep learning method for automatic assessment of human sperm images},
  author={Javadi, Soroush and Mirroshandel, Seyed Abolghasem},
  journal={Computers in Biology and Medicine},
  year={2019},
  doi={10.1016/j.compbiomed.2019.04.030}
}
```

## License

This dataset is made available under the [CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/) license.

## Credits

MHSMA is based on the Human Sperm Morphology Analysis Dataset (HSMA-DS) [(Ghasemian et al., 2015)](https://doi.org/10.1016/j.cmpb.2015.08.013).
