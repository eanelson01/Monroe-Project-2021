## Results of the UNet Model
### Results on Training Data
As mentioned in the previous sections, I trained the UNet model on the Inria Challenge dataset. I split those larger images into the smaller 250 x 250 format and then resized them further to fit into the model. I ultimately had 3,120 images that were 256 x 256 in size. I implemented the train test split and trained the model for a total of 15 epochs with a batch size of 32. Here are the results I gathered and the loss graph for the duration of training:

| Train vs Test | Accuracy | Loss | 
| ------------- | -------- | ---- |
| Train | 96.65% | 0.0811 |
| Test | 94.61% | 0.1500 |

![Loss Graph for Training](loss_graph.png)

From the table, you can see that the model was able to reach a 96.65% accuracy on the training data and a 94.61% testing accuracy. For the training data, this means that the model correctly predicted the label of an individual pixel, building vs non-building, ~96% of the time. The same concept applies to the testing dataset. These results are promising given the variety exhibited in architecture with most buildings not looking the same. For this reason, I was reasonably pleased with the initial results of the model. To look beyond these base quantitative results I began to look at the images that the model was actually predicting. A sample of them is below.

#### Training Images and Masks

| Actual Image | Generated Mask | 
| ------------ | -------------- | 
| ![img.png](images/16_train_actual.png) | ![img.png](images/16_test_gen.png)|
| ![img.png](images/921_train_actual.png) | ![img.png](images/921_test_gen.png) |
| ![img.png](images/630_train_actual.png) | ![img.png](images/630_test_gen.png) |
| ![img.png](images/520_train_actual.png) | ![img.png](images/520_test_gen.png) | 
| ![img.png](images/410_train_actual.png) | ![img.png](images/410_test_gen.png) |

Above is a sample of the training images and the generated masks. On the left is the image that was provided to the model and on the right is the generated label. The black area is pixels labeled as being non-building. Contrarily, the white pixels are the areas classified as being building. The model does a good job of picking out these areas but sometimes lacks full definition. The 4th picture shows this. There are some areas in between the two larger buildings where the model mistakenly labels the ground as being building. Additionally, there are some issues with defining buildings that are covered by trees or some shadow. Overall, these limitations do not halt the model from successfully illustrating areas where buildings are, especially on this training and testing data. These images provide reassurance that building segmentation using the UNet model is not only possible but relatively effective. With this in mind, I moved on to applying this model to the images of Harrisonburg that I retrieved from the USGS Earth Explorer. 
### Results on Harrisonburg Images
Having the model work relatively well on the training set made me confident in its ability to then be applied to the Harrisonburg images I retrieved. To do so, I loaded the images in 9 different batches for each time period. Each batch had 390 images and covered a 5000 x 5000 pixel range. I then called the function model.predict() on the images, viewing the results with the im.show() command. Below are the results for 2002.

#### 2002 Images

| Actual | Generated |
| :------: | :--------: | 
| ![img.png](images/512_25_02_actual.png) | ![img.png](images/512_25_02_gen.png) |
| ![img.png](images/07_37_actual.png) | ![img.png](images/07_37_gen.png) |
| ![img.png](images/07_36_actual.png) | ![img.png](images/07_36_gen.png) |
| ![img.png](images/07_60_actual.png) | ![img.png](images/07_60_gen.png) |
| ![img.png](images/07_65_actual.png) | ![img.png](images/07_65_gen.png) |

#### 2011 Images 

| Actual | Generated |
| :------: | :---------: | 
| ![img.png](images/11_25_actual.png) | ![img.png](images/11_25_gen.png) | 
| ![img.png](images/11_37_actual.png) | ![img.png](images/11_37_gen.png) |
| ![img.png](images/11_36_actual.png) | ![img.png](images/11_36_gen.png) | 
| ![img.png](images/11_60_actual.png) | ![img.png](images/11_60_gen.png) |
| ![img.png](images/11_65_actual.png) | ![img.png](images/11_65_gen.png) |


The images above are the satellite images on the left and the generated mask on the right. I separated them by 2002 and 2011 but the images are from the same area. This means that the first image in the 2002 section is the same area as the 1st image in 2011 and so on. The most striking visual is the differences in the masks for the second image for both. There are a total of 9 buildings in 2011 compared to the 1 in 2002. These images demonstrate a dramatic increase in residential density for this area. The model did an effective job on these Harrisonburg images but had similar faults as the training images. The borders can be blurry and fail to be fully defined. Additionally, there is sometimes extra noise when there are shadows or tree coverage. These and more factors result in less accurate results. The results are satisfactory overall, however, and paint a decent picture of the residential makeup of an area. The next step is to congregate these smaller images into larger 5000 x 5000 maps to provide additional context. 

#### [Link to additional comparitve images for 2002  vs 2011](images.md)

#### Larger Images 
The model did a great job picking up on where buildings are in the above images. These results show the effectiveness of the model in its designed goal. The images I've shown above are the smaller images derived from the original 5000 x 5000 format. Using the GDAL model, I was able to recreate the larger 5000 x 5000 image with the mask, giving more context than the smaller images. These were the intended end product of the model: maps showing where buildings are in a given section. With these images, we can directly compare the number of buildings in a given area from 2002 compared to 2011. 


#### [Information about Future Goals](future.md)

#### [Home Page](README.md)
