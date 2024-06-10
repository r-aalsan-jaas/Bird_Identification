<!DOCTYPE html>
<html lang="en">
<head>
    
</head>
<body>
    <h1>Bird Identification Project</h1>

  <h2>Overview</h2>
    <p>This project utilizes a convolutional neural network (CNN) to identify whether an image contains a bird or not. It's built using the fastai library and trained on images sourced from the web.</p>

  <h2>Installation</h2>
    <p>To run this project, you need to install the <code>fastbook</code> library which includes the fastai library. You can install it using pip:</p>
    <pre><code>!pip install fastbook</code></pre>

  <h2>Usage</h2>
    <p>The project includes a script that downloads images of birds and forests, segregates them into separate directories, and then trains a CNN model to differentiate between the two.</p>
    <p>Here’s a quick rundown of the process:</p>
    <ul>
        <li>Search and download images from the web.</li>
        <li>Verify and clean any failed images.</li>
        <li>Create a DataBlock for the images.</li>
        <li>Display a batch of images.</li>
        <li>Train the model using cnn_learner.</li>
        <li>Predict and print the probability that an image contains a bird.</li>
    </ul>

  <h2>Results</h2>
    <p>After fine-tuning the model for 3 epochs, the error rate dropped to 0.0%, indicating that the model is highly accurate on the validation set.</p>

  <h2>Example Prediction</h2>
    <pre><code>is_bird,_,probs = learn.predict(PILImage.create('bird.jpg'))
print(f"This is a : {is_bird}.")
print(f"Probability it's a bird: {probs[0]:.6f}")</code></pre>
    <p>Output:</p>
    <pre><code>This is a : bird.
Probability it's a bird: 1.000000</code></pre>

  <h2>Contributing</h2>
    <p>Contributions to this project are welcome. Please fork the repository and submit a pull request with your changes.</p>
</body>
</html>
