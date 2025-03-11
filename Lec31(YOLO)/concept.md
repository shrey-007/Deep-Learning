![img.png](img.png)
Here in the images-:
- (Bx,By) are coordinates of center of the object
- Bw,Bh are width and height of the bounding box
- C1 and C2 are two classes (persona and dog). If C1 is 1 means it is a dog else if C2 is 1 then it is a person
- Pc is the probability of the of object of class C lying in the bounding box. In the first image there is 1.0 probability that a dog is in the bounding box
- we can now train the neural network , by providing such photos with their respective vectors. Photos are X_train and vectors will be Y_train  ![img_1.png](img_1.png)
- Now if you give new image to this neural network, it will give the output vector
- First issue is that it will detect multiple bounding box of same object having different probabilities. Toh hum IOU se overlapping area nikalte hi and agar IOU jyada hai toh sirf us bounding box ko rakho jiska prob. highest hai and baaki ko nikaal do ![img_2.png](img_2.png)
