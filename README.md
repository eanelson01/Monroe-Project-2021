![](wm_logo2.png)
## Abstract
The main objective of my research project this summer is to identify buildings in Harrisonburg using satellite imagery. This information will allow administrators in Harrisonburg to better understand housing trends over the years and the location of residential areas. The proposed model will take an input of satellite imagery and create a map of building segmentations. This will produce a clear outline of where buildings are in that image and area. The idea of this project came from multiple changes in the Rockingham County school district boundaries as administrators tried to accommodate for changing population counts in each area. These changes were a result of large-scale immigration, meaning the city had to create more residential areas in a short time span. This resulted in fluctuations in the student body for the school system, the creation of new schools, and the movement of students in the school system based on their place of residence. With this model, school districts have estimates of where students and families are living, allowing them to better predict changes in student location in order to anticipate potential changes in the student enrollment numbers in the coming years.

My first goal for this project is to undergo a thorough literature review of current techniques in building segmentation using machine learning techniques. I will analyze various published papers on the topic, taking note of the machine learning techniques, satellite imagery sources, and methods used in order to meet their goals. With this information, I will better understand the direction I should take in my own pursuit and solidify my vision of the project. I will look into the methods beyond what is presented in the papers, watching various instructive videos on machine learning architectures and methods to get further background knowledge. Additionally, I will examine the authors' GitHub accounts, looking for potential skeleton code to base my implementation around.

My second goal is to find the best sources of data that I need and to take steps to clean the data if necessary. I will mostly base this search for data sources on the methods I read about in the literature review. I will analyze the different satellite imagery I find to see which best fits my objective and goals. I will take suggestions based on the sources of data used by the authors of the papers I read. This includes possibly using the same data that they used for training the model alongside finding additional images to use for my Harrisonburg implementation. Spending time on finding the correct dataset will pay dividends later on as it will improve the results of the model and research project as a whole. 

For my third goal, I will properly create, test, and assess the chosen CNN method to understand its effectiveness in building segmentation in Harrisonburg, VA. I will train based on the datasets I find from the literature review and then apply the model to the Harrisonburg images I find. This will allow me to see the accuracy on the training data as well as how applicable the model is on datasets that it was not trained on. Overall, the model's effectiveness on the Harrisonburg will be the ultimate metric that I try to improve and understand. This process will create an effective model for building segmentation in Harrisonburg, VA. With this model, I will then compare the trends of urbanization in Harrisonburg from the year 2002 to 2011.

With these steps, I feel confident that I will be able to create a model capable of building segmentation from satellite imagery which will aid Harrisonburg as well as the schools in the surrounding areas. 

### Detailed account of the process
[1. Proposed Calendar for Project Completion](calendar.md)

[2. Literature Review](litreview.md)

[3. Dataset used for training](dataset.md)

[4. Harrisonburg Dataset](hdataset.md)

[5. Explanation of Model](model.md)

[6. Script for Model](https://colab.research.google.com/drive/10a7IHhAniHaWLncCkWme0V3sdgyEwUYO?usp=sharing)

[7. Results of Model](results.md)

[8. Further Comparison Images of 2002 vs 2011 Harrisonburg](images.md)

[9. Future Goals and Implementation](future.md)
