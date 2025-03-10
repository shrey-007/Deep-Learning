### **Gradient Descent Variants**

Gradient Descent (GD) is an optimization algorithm used to update model parameters by minimizing the loss function. There are three main types:

| Type                     | Update Frequency | Pros ✅ | Cons ❌ |
|--------------------------|-----------------|--------|--------|
| **Batch Gradient Descent (BGD)** | After processing the **entire dataset** | Stable, converges smoothly | Slow for large datasets |
| **Stochastic Gradient Descent (SGD)** | After **each training sample** | Faster updates, good for online learning | Noisy convergence |
| **Mini-Batch Gradient Descent (MBGD)** | After processing a **small batch** of samples | Balance between BGD and SGD, efficient | Needs batch tuning |

---

### **1️⃣ Batch Gradient Descent (BGD)**
- Uses **all training samples** to compute the gradient.
- **Pros**:  
  ✔ More stable updates, less noisy.  
  ✔ Guaranteed to reach the minimum (for convex functions).
- **Cons**:  
  ❌ Computationally expensive for large datasets.  
  ❌ Requires loading all data into memory.

🚀 **Used in small datasets where memory is not a concern.**

---

### **2️⃣ Stochastic Gradient Descent (SGD)**
- Updates the model **after each training example**.
- **Pros**:  
  ✔ Faster updates, allows **real-time learning**.  
  ✔ Good for **online learning** and streaming data.
- **Cons**:  
  ❌ Updates are noisy, causing fluctuations.  
  ❌ May not converge smoothly.

🚀 **Used for large datasets, online learning, reinforcement learning.**

---

### **3️⃣ Mini-Batch Gradient Descent (MBGD)**
- Uses a **subset (batch) of data** to compute gradients.
- **Pros**:  
  ✔ Faster than BGD, more stable than SGD.  
  ✔ Efficient with **GPU acceleration**.
- **Cons**:  
  ❌ Needs proper batch size selection.  
  ❌ Still requires memory for batches.

🚀 **Most commonly used in deep learning (e.g., TensorFlow, PyTorch).**

---

### **Comparison Summary**

| Method | Stability | Speed | Memory | Best For |
|--------|----------|-------|--------|----------|
| **Batch GD** | High ✅ | Slow ❌ | High ❌ | Small datasets |
| **SGD** | Noisy ❌ | Fast ✅ | Low ✅ | Large datasets, online learning |
| **Mini-Batch GD** | Balanced ✅ | Fast ✅ | Medium ✅ | Deep learning |

---

### **Which One to Use?**
🔹 **Small datasets** → **Batch GD**  
🔹 **Large datasets / Online Learning** → **SGD**  
🔹 **Deep Learning (most cases)** → **Mini-Batch GD**

Would you like an example implementation in Java? 🚀