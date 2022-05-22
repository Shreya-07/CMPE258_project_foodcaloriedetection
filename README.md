# CMPE258_project_foodcaloriedetection

# Dataset Food-11 from EPFL research university
https://drive.google.com/drive/folders/1R0CTfX1UB2SRE56Ut2nQah1V7SV9Rug2?usp=sharing

    -The dataset is Food-11 from a public research university from switzerland called EPFL.
    -The main difference between original and this dataset is that we placed each category of food in separate folder to make model training process more convenient.
    -This dataset contains 16643 food images grouped in 11 major food categories.

# MobileNetV2
    -MobileNetV2 is a general architecture and can be used for multiple use cases. Depending on the use case, it can use different input layer size and different width factors. This allows different width models to reduce the number of multiply-adds and thereby reduce inference cost on mobile devices.
    -MobileNetV2(...): Instantiates the MobileNetV2 architecture.

# ConV2D Model
    Architecture:
    -Input Layer - Its a core layer, what it does is just provide the input image shape.
    -Convolution Layer - In this layer model learns weights. To calculate the learnable parameters here, all we have to do is just multiply the by the shape of width m, height n, previous layer filters d and account for all such filters k in the current layer. Filter used when scanned over the input image gives out the probability of the image which maps to the class. The filter extract the features from input image. The filter will feature identifier as it will enlighten certain features in the image and other parts has to be darkened resulting a feature map. Activation function 'relu' acts as feature rectifier where non linear operations will replace all the negative values from feature map to zero.
    -Pooling Layer - all it does is to calculate a specific number, no backprop learning involved
        -Max Pooling
        -Average Pooling
        -Global Pooling
        Max pooling is added to CNN. Max pooling is a pooling operation that selects the maximum element from the region of the feature map covered by the filter. Max pooling layer will reduce the diemntionality of the feature map while retaining feature information. This layer will reduce computationality complexity of the model. In our model we have used 2X2 matrix, minimum pixel loss and get a precise region where the feature are location
    -Fully Connected Layer - In this layer every neuron is connected to every other neuron. Dense is used to add a fully connected layer, units is where we defie the number of nodes that should be present in this hidden layer and these units value will be always between the number of inpu nodes and the output nodes. Final dense which is the fully connected layer converts vector map with numbe of vectors = number of classes model need to classify. activation function in the layer used is 'sigmoid', this layer will convert vector map into probability for the number of classes specified.
# Metrics of Models
    Accuracy of MobileNetV2 is 94 percent and loss of the model is 0.17. 
    Accuracy of ConV2D model is 99 percent and loss of the model built is 1.8. 
    When compared both the models ConV2D model is overfitting on the dataset. So Using MobileNetV2 model to built application. 

# Application
    -Used Streamlit for deploying our application.
    -The Streamlit application file uses our trained model and labels for prediction.
    -The application file has functions for searching the calories based on predicted food.
    -For running our application, we have used local tunnel which is a simple tool that provides you a publicly-accessible URL that reroutes every request to your locally-running process.
