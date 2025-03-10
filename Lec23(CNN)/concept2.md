- Let's take example of digits classification in CNN
- We are given an handwritten number 9 , and we have to recognise it.
- Problem is every person draws it differently.
  ![img.png](img.png) (Here 9 is in middle) (1 represent black, where 9 is written, and remaining pixels are -1)
  ![img_1.png](img_1.png) (Here 9 is in left side)
  ![img_2.png](img_2.png) (Here there is no curvature in the lower part)
- So there is a pattern to recognise 9, 9 has a loop in the top, and a vertical line in the middle and a diagonal line in the lower part.
- So to detect these we have 3 kernels(filters)
- ![img_3.png](img_3.png)
  This is the kernel to detect loop. It iterates over whole image and then finds ki kis position par loop hai. Feature mao mai jaha 1 hai vaha loop hai.
- ![img_5.png](img_5.png)
  9 ke feature map mai uper 1 hai since uper hai loop and 6 ke feature map mai neeche hai 1 since loop neche hai 
- Similarly baaki 2 filters bhi apply karo and then unke bhi feature map banao
  ![img_6.png](img_6.png)
- Ye abhi feature extraction hua.These extracted features ki loop kis position mai hai, straight line kis position mai hai are now fed to Neural Network.

---
CNNs are **invariant** to the following transformations:

###  Translation Invariance
✅ CNNs can recognize objects even if they are **shifted** in the image.  
🔹 **Why?** The **Pooling layer** reduces spatial sensitivity, making CNNs robust to small translations.

###  Deformation Invariance
✅ CNNs can recognize distorted or deformed objects.  
🔹 **Why?** **Pooling layers** and multiple filters detect flexible patterns.

###  Illumination and Contrast Invariance
✅ CNNs work well with changes in **lighting and contrast**.  
🔹 **Why?** Deep layers extract high-level features (shapes, textures) independent of pixel intensity.

### **🔍 What CNNs Are *Not* Invariant To?**

###  Scale Invariance
✅ CNNs can not recognize objects at different **scales** (sizes).  
🔹 **Why?** Different filter sizes capture features at multiple scales.  
🔹 **Limitation:** CNNs struggle with extreme scale variations unless techniques like **data augmentation** or **multi-scale training** are used.

###  Rotation Invariance 
✅ CNNs can handle small **rotations** but not large ones.  
🔹 **Why?** Filters detect edges and patterns regardless of slight rotation.  
🔹 **Limitation:** Large rotations require **rotation-augmented training data** or **Capsule Networks**.
