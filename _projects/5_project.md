---
layout: page
title: Animal data science project3
description: Automated acquisition of top-view dairy cow depth image data using an RGB-D sensor camera.
img: assets/img/Aut/title.png
importance: 5
category: work
---


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Aut/title.png" title="title" class="img-fluid rounded z-depth-0" %}
    </div>
</div>

Paper: [https://doi.org/10.1093/tas/txac163](https://doi.org/10.1093/tas/txac163)  
Codes: [https://github.com/codeandstuf/CattleDepthCollection](https://github.com/codeandstuf/CattleDepthCollection)

<strong>Abstract</strong>  
Animal dimensions are essential indicators for monitoring their growth rate, diet efficiency, and health status. A computer vision system is a recently emerging precision livestock farming technology that overcomes the previously unresolved challenges pertaining to labor and cost. Depth sensor cameras can be used to estimate the depth or height of an animal, in addition to two-dimensional information. Collecting top-view depth images is common in evaluating body mass or conformational traits in livestock species. However, in the depth image data acquisition process, manual interventions are involved in controlling a camera from a laptop or where detailed steps for automated data collection are not documented. Furthermore, open-source image data acquisition implementations are rarely available. The objective of this study was to 1) investigate the utility of automated top-view dairy cow depth data collection methods using picture- and video-based methods, 2) evaluate the performance of an infrared cut lens, 3) and make the source code available. Both methods can automatically perform animal detection, trigger recording, capture depth data, and terminate recording for individual animals. The picture-based method takes only a predetermined number of images whereas the video-based method uses a sequence of frames as a video. For the picture-based method, we evaluated 3- and 10-picture approaches. The depth sensor camera was mounted 2.75 m above-the-ground over a walk-through scale between the milking parlor and the free-stall barn. A total of 150 Holstein and 100 Jersey cows were evaluated. A pixel location where the depth was monitored was set up as a point of interest. More than 89% of cows were successfully captured using both picture- and video-based methods. The success rates of the picture- and video-based methods further improved to 92% and 98%, respectively, when combined with an infrared cut lens. Although both the picture-based method with 10 pictures and the video-based method yielded accurate results for collecting depth data on cows, the former was more efficient in terms of data storage. The current study demonstrates automated depth data collection frameworks and a Python implementation available to the community, which can help facilitate the deployment of computer vision systems for dairy cows.


<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Aut/fig1.jpeg" title="cv1" class="img-fluid rounded z-depth-0" %}
    </div>

</div>
<div class="caption">
Figure 1. Schematic representation of the depth data acquisition system from A) top and B) side views. The depth camera was positioned above the walk-through path.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-3">
        {% include figure.html path="assets/img/Aut/fig2.jpeg" title="cv2" class="img-fluid rounded z-depth-0" %}
    </div>

</div>
<div class="caption">
FIGURE 2. Locations of point-of-interests (black points) in depth data for A) picture- and B) video-based methods. The point-of-interests were enlarged for a visualization purpose. Depth information is indicated with the level of brightness.Fi
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0 d-flex align-items-center">
        {% include figure.html path="assets/img/Aut/fig3.jpeg" title="fig3" class="img-fluid rounded z-depth-0" %}
    </div>
</div>
<div class="caption">
FIGURE 3. Example of image segmentation steps. A) Cropped depth picture taken using the D435 camera. B) Hue, saturation, value image. C) Threshold image. D) Final result. The largest contour was kept, and morphological closing was used to fill small empty areas within contour. Depth information is indicated with the level of brightness.
</div>



<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/Aut/fig4.jpeg" title="fig4" class="img-fluid rounded z-depth-0" %}
    </div>
</div>
<div class="caption">
FIGURE 4. Examples of postsegmented depth image data. A) Successful image. B) Unsuccessful image due to quality. C) Unsuccessful image due to the cow not being in the field of vision. D) Unsuccessful image due rail separation. E) Unsuccessful image due to quality and rail separation. F) Unsuccessful image due obstructed view from multiple cows in the same image.
</div>
