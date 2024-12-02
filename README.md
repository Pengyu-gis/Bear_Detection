<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Intelligent Bear Prevention System</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 20px;
            background-color: #f9f9f9;
            color: #333;
        }
        h1, h2, h3 {
            text-align: center;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        table, th, td {
            border: 1px solid #ddd;
        }
        th, td {
            padding: 12px;
            text-align: center;
        }
        th {
            background-color: #f2f2f2;
        }
        img {
            max-width: 100%;
            height: auto;
            display: block;
            margin: 10px auto;
        }
        .center {
            text-align: center;
        }
        .note {
            font-style: italic;
            color: #666;
            margin: 10px 0;
            text-align: center;
        }
    </style>
</head>
<body>

<h1>Intelligent Bear Prevention System Based on Computer Vision and IoT</h1>
<h2>A New Approach to Reduce Human-Bear Conflicts</h2>

<h2>Dataset</h2>
<p>The dataset contains a total of 6 labels and 1,195 images, organized as follows:</p>

<table>
    <tr>
        <th>Label</th>
        <th>Training Set / Validation Set</th>
        <th>Total</th>
    </tr>
    <tr>
        <td>Cat</td>
        <td>133 / 6</td>
        <td>139</td>
    </tr>
    <tr>
        <td>Cow</td>
        <td>155 / 7</td>
        <td>162</td>
    </tr>
    <tr>
        <td>Dog</td>
        <td>154 / 7</td>
        <td>161</td>
    </tr>
    <tr>
        <td>Bear</td>
        <td>794 / 10</td>
        <td>804</td>
    </tr>
    <tr>
        <td>Goat</td>
        <td>70 / 6</td>
        <td>76</td>
    </tr>
    <tr>
        <td>Human</td>
        <td>131 / 6</td>
        <td>137</td>
    </tr>
</table>

<h2>Training Parameters</h2>
<h3>Image Augmentation</h3>
<ul>
    <li>Random mirroring: Enabled</li>
    <li>Random rotation: Disabled</li>
    <li>Random blurring: Enabled</li>
    <li>Scaling method: Contain</li>
    <li>Scaling size: 224 x 224</li>
    <li>Mean value: 123.5</li>
    <li>Standard deviation: 58.395</li>
</ul>

<h3>Model Information</h3>
<ul>
    <li>Deployment platform: nncase</li>
    <li>Model architecture: YOLOv2</li>
    <li>Backbone network: MobileNet_0.75</li>
</ul>

<h3>Training Parameters</h3>
<ul>
    <li>Training epochs: 150</li>
    <li>Batch size: 32</li>
    <li>Learning rate: 0.001</li>
    <li>Bounding box limit: 8</li>
    <li>Data balancing: Disabled</li>
    <li>Allow negative samples: Enabled</li>
</ul>

<h2>Training Results</h2>
<p>The best accuracy on the validation set was achieved at the 150th training iteration: <strong>0.654</strong>.</p>

<div class="center">
    <img src="https://github.com/user-attachments/assets/efc49203-af0e-4688-a9e8-fdcd2bdf20f3" alt="Training Results Visualization">
</div>

<h3>Validation Set Results</h3>

<h4>Correct Results</h4>
<div class="center">
    <img src="https://github.com/user-attachments/assets/eaf3997c-ee4a-422b-80e9-7d6364908e45" alt="Correct Result 1">
    <img src="https://github.com/user-attachments/assets/21c88ac9-24a0-4a07-a99c-77eb79e7c828" alt="Correct Result 2">
    <img src="https://github.com/user-attachments/assets/6d375edf-8404-48fd-8f80-1b6bfcfc0ea3" alt="Correct Result 3">
    <img src="https://github.com/user-attachments/assets/bdd65ba1-653b-41f2-8265-41d3d5dd4447" alt="Correct Result 4">
</div>

<h4>False Results</h4>
<div class="center">
    <img src="https://github.com/user-attachments/assets/93f39411-53c7-4c55-a106-09bd4305cf78" alt="False Result 1">
    <img src="https://github.com/user-attachments/assets/f31dcce2-121d-4aa9-9937-de81589aac77" alt="False Result 2">
    <img src="https://github.com/user-attachments/assets/fe7f89ea-a063-4c96-b7b1-d9d2e054dc83" alt="False Result 3">
    <img src="https://github.com/user-attachments/assets/9c6d58a9-971b-4b5e-9d92-9b716100a411" alt="False Result 4">
</div>

<div class="note">
    <p>- <em>White boxes are user-labeled boxes.</em></p>
    <p>- <em>The green box is the model's correct prediction box.</em></p>
    <p>- <em>The red box is the model's incorrect prediction box.</em></p>
    <p>- <em>Only white boxes indicate that the model did not detect the target.</em></p>
</div>

</body>
</html>
