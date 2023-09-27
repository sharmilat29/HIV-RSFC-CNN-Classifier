### HIV-RSFC-CNN-Classifier

##### Dataset: 

2D image matrix representations of resting state functional connectivity within people with HIV (PWH) and without HIV (PLWH) split into training and validation sets.

##### Model: 

3 sets of Convolution -> Max Pooling layers followed by a Flattening layer and 2 Dense layers (ReLU and Sigmoid activations respectively)

```mermaid
graph TD;
id1[Conv2D]-->id2[MaxPooling];
id2[MaxPooling]-->id3[Conv2D];
id3[Conv2D]-->id4[MaxPooling];
id4[MaxPooling]-->id5[Conv2D];
id5[Conv2D]-->id6[MaxPooling];
id6[MaxPooling]-->Flatten;
Flatten-->id7[Dense ReLU activation];
id7[Dense ReLU activation]-->id8[Dense sigmoid activation];
```

##### Observation:

- Number of training and test samples were low
- Could attempt different model architectures to see if it does any better
- At present, model performance is only a tad better than chance sometimes :)

