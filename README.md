# LeNet Variant Comparison

Comparison of LeNet CNN Architecture Variants with Fashion MNIST Dataset

## Models
### Baseline
Original LeNet 5 architecture changed to use ReLU activation functions and max-pooling layers

![Baseline](/architectures/model_1.png)

![Baseline metrics](/graphs/lenet5_metrics.png)

### Variant 1
Learning rate changed to adaptive learning rate (1/2 every 5 epochs from initial 0.001 learning rate)

![Variant 1](/architectures/model_1.png)

![Variant 1 metrics](/graphs/lenet5_v1_metrics.png)

### Variant 2
Number of filters in convolution layers increased from 6 and 16 to 32 and 64

![Variant 2](/architectures/model_2.png)

![Variant 2 metrics](/graphs/lenet5_v2_metrics.png)

### Variant 3

Neurons in fully connected layers increased from 120 and 84 to 200 and 140 (0.7 ratio maintained)

![Variant 3](/architectures/model_3.png)

![Variant 3 metrics](/graphs/lenet5_v3_metrics.png)

### Variant 4
Batch normalization layers added before ReLU activations

![Variant 4](/architectures/model_4.png)

![Variant 4 metrics](/graphs/lenet5_v4_metrics.png)

## Results

| Model (@ best epoch) | Training top-1 accuracy (%) | Validation top-1 accuracy (%) | Testing top-1 accuracy (%) |
|:----------------------:|:-----:|:-----:|:-----:|
| Baseline (@ epoch 14)  | 90.9% | 89.6% |  N/A  |
| Variant 1 (@ epoch 15) | 92.1% | 90.3% |  N/A  |
| Variant 2 (@ epoch 14) | 94.9% | 91.6% |  N/A  |
| Variant 3 (@ epoch 13) | 94.7% | 91.9% |  N/A  |
| Variant 4 (@ epoch 15) | 95.7% | 92.6% | 92.5% |
| Variant 4 retrained on train + val data (@ epoch 15) | 95.7% |  N/A  | 93% |

Variant 4 testing confusions:

![Best model cm](/graphs/cm_best_model.png)

Retrained Variant 4 testing confusions:

![Best model retrained cm](/graphs/cm_best_model_retrained.png)

## Dataset

![tSNE](/graphs/tSNE.png)

![Classifications](/graphs/test_set_classific.png)
