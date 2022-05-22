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
-Convolution Layer - In this layer model learns weights. To calculate the learnable parameters here, all we have to do is just multiply the by       the shape of width m, height n, previous layer filters d and account for all such filters k in the current layer
-Pooling Layer - all it does is to calculate a specific number, no backprop learning involved
    -Max Pooling
    -Average Pooling
    -Global Pooling
-Fully Connected Layer - In this layer every neuron is connected to every other neuron.

# Application
-Used Streamlit for deploying our application.
-The Streamlit application file uses our trained model and labels for prediction.
-The application file has functions for searching the calories based on predicted food.
-For running our application, we have used local tunnel which is a simple tool that provides you a publicly-accessible URL that reroutes every request to your locally-running process.
