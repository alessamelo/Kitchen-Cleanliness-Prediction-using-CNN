<h1 align="center">
Kitchen Cleanliness Prediction using CNN
</h1>

<p align="center">
Multimodal kitchen cleanliness monitoring module integrated into DepaYT.
</p>

---

<h2>Project Overview</h2>

<p>
This project implements a multimodal artificial intelligence module integrated into the <strong>DepaYT</strong> mobile platform inside the <strong>Kitchen Usage</strong> module.
</p>

<p>
The system combines:
</p>

<ul>
    <li>Computer Vision using Convolutional Neural Networks (CNNs)</li>
    <li>Contextual reasoning using a Multilayer Perceptron (MLP)</li>
    <li>Collaborative kitchen monitoring for shared apartment environments</li>
</ul>

<p>
The objective of the module is to assist roommates in maintaining shared kitchen cleanliness through contextual recommendations and visual cleanliness verification.
</p>

---

<h2>Workflow</h2>

<h3>1. Start Kitchen Usage</h3>

<p>
The user begins a kitchen session by pressing the <strong>Start Usage</strong> button inside DepaYT.
</p>

---

<h3>2. Stop Kitchen Usage</h3>

<p>
After finishing the cooking activity, the user presses the <strong>Stop Usage</strong> button.
</p>

<p>
The system then displays a contextual questionnaire related to the cooking activity performed.
</p>

<p>
The questionnaire includes information such as:
</p>

<ul>
    <li>Type of food prepared</li>
    <li>Cooking method</li>
    <li>Oil usage</li>
    <li>Spill occurrence</li>
    <li>Number of utensils used</li>
    <li>Number of people served</li>
</ul>

---

<h3>3. Contextual Dirtiness Prediction</h3>

<p>
The questionnaire answers are transformed into structured tabular data and processed by a <strong>Multilayer Perceptron (MLP)</strong>.
</p>

<p>
The MLP predicts the expected kitchen dirtiness level:
</p>

<ul>
    <li>Low</li>
    <li>Medium</li>
    <li>High</li>
</ul>

<p>
Based on the prediction, the system generates contextual cleaning recommendations for the user.
</p>

---

<h3>4. Kitchen Image Upload</h3>

<p>
After receiving the recommendation, the user uploads a final image of the induction kitchen surface.
</p>

<p>
The uploaded image is analyzed using a <strong>Convolutional Neural Network (CNN)</strong> trained for binary image classification.
</p>

<p>
The CNN predicts whether the kitchen surface is:
</p>

<ul>
    <li>Clean</li>
    <li>Dirty</li>
</ul>

---

<h3>5. Shared Kitchen Monitoring</h3>

<p>
The final cleanliness prediction and contextual information are stored inside the application database.
</p>

<p>
All roommates can later visualize:
</p>

<ul>
    <li>Kitchen cleanliness status</li>
    <li>Previous kitchen sessions</li>
    <li>Cleaning history</li>
    <li>Shared kitchen conditions</li>
</ul>

---

<h2>Model Architectures</h2>

<h3>Image Modality</h3>

<ul>
    <li>Convolutional Neural Networks (CNNs)</li>
    <li>Transfer Learning experiments using MobileNetV3</li>
    <li>Autoencoder experiments for anomaly detection</li>
</ul>

<h3>Textual / Contextual Modality</h3>

<ul>
    <li>Multilayer Perceptron (MLP)</li>
    <li>One-Hot Encoding preprocessing pipeline</li>
    <li>Contextual dirtiness classification</li>
</ul>

---

<h2>Project Structure</h2>

<pre><code>.
├── Code/
│   ├── Kitchen_Image_Prediction/
│   │   ├── CNN.ipynb
│   │   ├── TransferLearning.ipynb
│   │   ├── Autoencoders.ipynb
│   │   └── Data_augmentation.ipynb
│   │
│   ├── Text_Questions/
│   │   ├── MLP.ipynb
│   │   └── EDA.ipynb
│   │
│   └── Recommendations_model.ipynb
│
├── README.md
├── requirements.txt
└── .gitignore
</code></pre>

---

<h2>Environment Setup</h2>

<h3>Create Virtual Environment</h3>

<pre><code>python -m venv venv
</code></pre>

---

<h3>Activate Environment (Windows)</h3>

<pre><code>venv\Scripts\activate
</code></pre>

---

<h3>Activate Environment (Mac/Linux)</h3>

<pre><code>source venv/bin/activate
</code></pre>

---

<h3>Upgrade pip</h3>

<pre><code>python -m pip install --upgrade pip
</code></pre>

---

<h3>Install Requirements</h3>

<pre><code>pip install -r requirements.txt
</code></pre>

---

<h2>Technologies Used</h2>

<ul>
    <li>Python</li>
    <li>TensorFlow / Keras</li>
    <li>Scikit-learn</li>
    <li>Pandas</li>
    <li>NumPy</li>
    <li>Matplotlib</li>
    <li>Seaborn</li>
</ul>

---

<h2>Objective</h2>

<p>
This module aims to provide an intelligent and collaborative solution for monitoring kitchen cleanliness in shared apartment environments by combining contextual reasoning and computer vision techniques inside the DepaYT ecosystem.
</p>