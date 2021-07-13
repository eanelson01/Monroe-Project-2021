## Overview of Training Dataset Used

### Intro to Dataset and Origins
In order to train the prospected model and to preview the code, I used the [Inria Aerial Image Labeling Dataset](https://project.inria.fr/aerialimagelabeling/files/). I became aware of the dataset from [Weijia Li's GitHub page](https://github.com/liweijia), the lead author of the [main research paper](https://www.mdpi.com/2072-4292/11/4/403/htm) I have used as guidance for this project.

### Content of Dataset
The dataset is conveniently broken into training and testing data. The training data has ground truth images, illustrating the true segmentation of the buildings in the image. This allows for validation of the model's results once it is trained on the dataset. Additionally, the dataset contains satellite images from Austin, Chicago, Vienna, and more. This provides images from varying environments for analysis. The images are .3 m resolution, providing clear outlines of buildings.

