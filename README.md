# calibration-primer

This GitHub repository accompanies the (CVC seminar)[https://www.cvc.uab.es/blog/2023/06/30/jordy-van-landeghem-cvc-seminar/] on probability estimation, calibration and failure prediction. 

It contains the code to reproduce the experiments and examples from the presentation.


`src/` 
    `intuition_calibration.ipynb` is the main notebook containing examples of how to use the calibration and failure prediction modules
    `metrics.py` contains implementations metrics of interest
    `check_ICDAR_proceedings.ipynb` contains the code to reproduce the keyword search on the ICDAR 2021 Proceedings 
    
`data/` contains different model logits and references


## Intuition on calibration and failure prediction

The main notebook contains examples of how to use the calibration and failure prediction modules.

We measure metrics of interest on:
- CIFAR-10 ResNet-18
- RVL-CDIP LayoutLMv3
- Running example from the [presentation](https://www.cvc.uab.es/blog/2023/06/30/jordy-van-landeghem-cvc-seminar/) 

We use the following metrics:
- Accuracy
- F1 score (micro,macro)
- ECE
- Brier score
- Negative Loglikelihood
- AURC

We test the influence of a popular calibration method (Temperature Scaling) on the metrics of interest

As a bonus, we plot risk-coverage curves for DiT-base models trained on RVL-CDIP from *Beyond Document Page Classification* 2023 (Van Landeghem, Biswas 2023)