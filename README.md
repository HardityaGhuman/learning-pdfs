# Assignment - PDF Learning using GAN

Roll Number: 102303230  
a_r = 0.5, b_r = 0.3

## Folder structure

```
learning_pdf/
├── data/
│   └── india_air_quality_data.csv   
├── outputs/                          
├── gan_pdf.ipynb
├── requirements.txt
└── README.md
```

## Steps to run

1. Put `india_air_quality_data.csv` inside the `data/` folder
2. Open `gan_pdf.ipynb` in Jupyter
3. Run all cells top to bottom (Kernel > Restart and Run All)
4. Plots will appear inline and also save to `outputs/`

## Output files

- `outputs/z_distribution.png` - histogram of transformed variable z

![Z Distribution](outputs/z_distribution.png)

- `outputs/training_loss.png` - GAN training curve

![Training Loss](outputs/training_loss.png)

- `outputs/gan_pdf.png` - final learned PDF overlaid on real data

![GAN PDF](outputs/gan_pdf.png)

## Observations

### Mode Coverage
The generator learns the overall right skewed shape and correctly captures the main peak around z = 10–15. However, smaller bumps in the real data are smoothed out. The tail is slightly underrepresented, showing incomplete coverage of rare high values.

### Training Stability
Training was unstable in the early epochs. Around epoch 1000, the losses stabilized with no divergence observed. This indicates the model eventually reached a steady training phase.

### Quality of Generated Distribution
Generated samples fall in the expected range and follow the general skew of the real data. The main trend is captured, but fine details are not perfectly matched so there is scope for improvement.
