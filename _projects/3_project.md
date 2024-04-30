---
layout: page
title: Deep learning prediction of dairy cattle body weight
description: Depth video data-enabled predictions of longitudinal dairy cow body weight using thresholding and Mask R-CNN algorithms
img: assets/img/DairyBW/bw.png
importance: 1
category: work
---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DairyBW/bw.png" title="title" class="img-fluid rounded z-depth-0" %}
    </div>
</div>

Paper: [https://doi.org/10.1016/j.atech.2023.100352](https://doi.org/10.1016/j.atech.2023.100352)  
Codes: [https://github.com/yebigithub/BW_dairy](https://github.com/yebigithub/BW_dairy)

<strong>Abstract</strong>  
Monitoring cow body weight is crucial to support farm management decisions due to its direct relationship with the growth, nutritional status, and health of dairy cows. Cow body weight is a repeated trait, however, the majority of previous body weight prediction research only used data collected at a single point in time. Furthermore, the utility of deep learning-based segmentation for body weight prediction using videos remains unanswered. Therefore, the objectives of this study were to predict cow body weight from repeatedly measured video data, to compare the performance of the thresholding and Mask R-CNN deep learning approaches, to evaluate the predictive ability of body weight regression models, and to promote open science in the animal science community by releasing the source code for video-based body weight prediction. An Intel RealSense D435 camera was installed on Virginia Tech dairy complex to collect top-view videos of 10 lactating Holstein cows twice a day for 28 days after milking sessions and 2 non-lactating, pregnant Jersey cows once a week upon calving. At the same time, the ground truth body weight records were collected using a walk-over weighing system. A total of 40,405 depth images and depth map files were obtained. Three approaches were investigated to segment the cow's body from the background, including single thresholding, adaptive thresholding, and Mask R-CNN. Four image-derived biometric features, such as dorsal length, abdominal width, height, and volume, were estimated from the segmented images and fitted using ordinary least squares, ridge regression, least absolute shrinkage and selection operator, and linear mixed models. Two cross-validation designs, forecasting and leave-three-cows-out, were used to evaluate prediction performance. The Pearson correlation between image-derived biometric features and scale-based body weight ranged from 0.74 to 0.95. On average, the Mask-RCNN approach combined with a linear mixed model resulted in the best prediction coefficient of determination and mean absolute percentage error of 0.98 and 2.03%, respectively, in the forecasting cross-validation. The Mask-RCNN approach was also the best in the leave-three-cows-out cross-validation, followed by adaptive and single thresholding. The prediction coefficients of determination and mean absolute percentage error of the Mask-RCNN coupled with the linear mixed model were 0.90 and 4.70%, respectively. Our results suggest that deep learning-based segmentation improves the prediction performance of cow body weight from longitudinal depth video data.



<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DairyBW/Fig.10.png" title="cv1" class="img-fluid rounded z-depth-0" %}
    </div>

</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/DairyBW/Table2.png" title="cv1" class="img-fluid rounded z-depth-0" %}
    </div>

</div>