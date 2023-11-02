# Problem Statement
To develop a computer aided diagnosis tool to detect the presence of diabetic  retinopathy and classify whether it is a normal diabetic retinopathy or an abnormal  diabetic retinopathy.

# Introduction
Diabetic Retinopathy is a condition that may occur in people who have diabetes. It causes progressive damage to the retina, the light-sensitive lining at the back of the eye. Diabetic retinopathy is a serious sight-threatening complication of diabetes. Diabetes interferes with the body's ability to use and store sugar (glucose). The disease is characterized by too much sugar in the blood, which can cause damage throughout the body, including the eyes. Over time, diabetes damages small blood vessels throughout the body, including the retina Diabetic retinopathy occurs when these tiny blood vessels leak blood and other fluids. This causes the retinal tissue to swell, resulting in cloudy or blurred vision.

Diabetic retinopathy usually affects both eyes. The longer a person has diabetes, the more likely they will develop diabetic retinopathy. If left untreated, diabetic retinopathy can cause blindness when people with diabetes experience long periods of high blood sugar, fluid can accumulate in the lens inside the eye trat controls focusing. This changes the curvature of the lens, leading to changes in vision. However, once blood sugar levels are controlled, usually the lens will return to its original shape and vision improves. Patients with diabetes who can better control their blood sugar levels will slow the onset and progression of diabetic retinopathy.

According to a 2018 American Eye-Q survey conducted by the AOA, nearly half of Americans didn't know whether diabetic eye diseases have visible symptoms (often which the early stages of diabetic retinopathy do not). The same survey found that more than one-third of Americans didn't know a comprehensive eye exam is the only way to determine if a person's diabetes will cause blindness, so the ADA recommends that everyone with diabetes have a comprehensive dilated eye examination at least once a year. Early detection and treatment can limit the potential for significant vision loss from diabetic retinopathy.

# Proposed Methodology
ResNet model is used to classify the images. The model is built using PyTorch in which the pre-processing is done internally. The ResNet model consists of 152 layers. The depth of the deep network plays a pivotal role in their performance. With the increase in layers, the model gives better performance.

However, it has also been observed that the addition of layers may increase the error rate. This is named as an issue of vanishing gradients. The residual neural network, also known as ResNet, was introduced to address this problem. Residual Network uses the skip connection to indiscriminately allow some input to the layer to incorporate the flow of information and also to prevent its loss, hence, addressing the problem of vanishing gradients (which also suppresses the generation of some noise). Suppressing the noise means averaging the models, which keeps a balance between precision and generalization. To achieve higher precision and an estimated level of traversal, the most efficient way is to increase more labeled data. The structure of ResNet speeds up the training of ultra-deep neural networks and increases the model's accuracy on large training data.

This model is first trained and is later tested inorder to classify the images. The training of the data set is done using 3662 images and the testing is for approximately 1900+ images. At a later stage, a GUI is developed using Tkinter in python which asks the user to upload the image of a fundus retinal image and then gives the predicted label as the output.

# Design Diagram
![image](https://github.com/SomyanshAvasthi/Retinopathy-Detection-using-ResNet-Model/assets/107310391/77564256-8866-40d4-99ce-3b1554524bc2)

# Architecture
ResNet includes the skip connection feature which enables the training of 152 layers without vanishing gradient issues. The approach behind this network is instead of layers learning the underlying mapping we allow the network to fit the residual mapping.

So, instead of say H(x), initial mapping, let the network fit, F(x)= H(x) gives H(x) F(x)+x. where: x shows the input of building block. -x which

F(x) shows the output of the layer within the building block of the residual network.

![image](https://github.com/SomyanshAvasthi/Retinopathy-Detection-using-ResNet-Model/assets/107310391/24fcc088-b7ec-4daa-a3f8-3b9d447ce63e)

# Conclusion
In this project, able to classify the images into different stages of DR using the pretrained RESNET model. The GUI we developed will be helpful for both doctors and also the common people.


