<h1 align="center">YOLOv8 object detection example</h1>

- [Demo](#Demo)
- [Dataset](#dataset)
- [AP](#AP)
- [Classes](#Classes)
- [Training Log](#Log)
- [Weights](#weights)
- [Environment](#environment)
- [Speed](#speed)
- [Google Colab](#colab)
- [References](#ref)

<h2 id='Demo'>Demo</h2>

![1627216237257](https://github.com/ChangeMaker13/YOLOv8_Object-Detection/assets/22545460/e21f32e7-a288-419d-a836-7c97c83583d4)

<h2 id='dataset'>Dataset</h2>

https://drive.google.com/file/d/1rlDFnYgzLtDNS_tqJDE0-LfURDUtXwsn/view?usp=sharing

<h2 id='AP'>AP</h2>

                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95)
                   all       2091      15400      0.726      0.584      0.643      0.367
                   car       2091       9024      0.804      0.777       0.83      0.536
                 truck       2091        873      0.805      0.652      0.737      0.493
            pedestrian       2091       1638       0.65      0.516      0.572      0.275
             bicyclist       2091        151      0.665      0.503      0.556      0.303
                 light       2091       1747      0.833      0.682      0.739      0.377
               pothole       2091       1967      0.598      0.376      0.424      0.216

<h2 id='Classes'>Classes</h2>

![dataset chart](https://github.com/ChangeMaker13/YOLOv8_Object-Detection/assets/22545460/6e715ce6-83e9-44d1-9302-7304a1ee5190)

1. car: with 68,008 labels
2. truck: with 4,170 labels
3. pedestrian: with 8,590 labels
4. bicyclist: with 955 labels
5. light: with 8,723 labels
6. pothole: with 10,024 labels

- total: 100,470 labels
- Train : valid = 9:1

<h2 id='Log'>Training Log</h2>

| ![chart 2](https://github.com/ChangeMaker13/YOLOv8_Object-Detection/assets/22545460/927da203-552f-4c65-865a-b6d1025c0a2a)

<h2 id='weights'>Weights</h2>

trained with 300 epochs<br>
https://drive.google.com/file/d/1-mfFLoZrUd6jlrmd9V9ym5_g2J3SIyPV/view?usp=sharing

<h2 id='environment'>Environment</h2>

- VM: Google Colaboratory
- GPU: NVIDIA T4 Tensor GPU
- NVIDIA-SMI 525.105.17 Driver Version: 525.105.17 CUDA Version: 12.0
- nvcc: NVIDIA (R) Cuda compiler driver
- Cuda compilation tools, release 11.8, V11.8.89
- Build cuda_11.8.r11.8/compiler.31833905_0

<h2 id='speed'>Speed</h2>

![fps chart](https://github.com/ChangeMaker13/YOLOv8_Object-Detection/assets/22545460/e6f45825-2965-4b56-bc95-5fe9479b3edd)

network I/O : time of sending image from front page to inferencing server
<br>
inferencing time : time of detection of objects
<br>

- above chart represent results of processing 10 images with models trained only for 50 epochs

<h2 id="colab">Google Colab</h2>

<a href="https://colab.research.google.com/drive/1mmPZ8I6CigKF5zsv-T5-7M-QHh9Fey_T?usp=sharing">Link</a>

<h2 id='ref'>References</h2>

- Training data1(self-driving) : https://www.kaggle.com/alincijov/self-driving-cars
- Training data2(pothole) : https://www.dropbox.com/s/qvglw8pqo16769f/pothole_dataset_v8.zip?dl=1
- The dataset used for training was preprocessed with above 2 datasets(reducing size, cross labeling, balancing number of labels of each class)
- test videos
  <br>
  https://drive.google.com/file/d/1uYKr_ogmZp1U8akz3qWKsCov6hu9Voob/view?usp=sharing
  <br>
  https://drive.google.com/file/d/1IEPLROgmtc7MTDinsMRcIyaeaweNiBzU/view?usp=sharing
