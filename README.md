# Brazilian traffic sign detection using Deep Learning
### Authors
[Felipe de Oliveira](https://github.com/felipeinagaki), [Suemy Inagaki](https://github.com/suemyinagaki) and Carlos David

[Paper](https://github.com/felipeinagaki/traffic_sign_detection/blob/main/docs/final-report.pdf)

We trained 4 distinct object detection models and applied BoT-SORT object track model. 
The object detection models were: Yolov8-small, Yolov8-medium, Yolov8-nano and RTDETR-L
![doc-image](docs/imgs/doc_im_1.png)

As can be seen on the previous images, RTDETR-L is very sensitive, creating several false positive results.

This impact the tracking model as can be seen on the image below, where the same RTDETR-L identifies a traffic sign as 29th while the other models only counted 5/6.
![doc-image](docs/imgs/doc_im_2.png)

A complete discussion about the results can be found in our report.
## Accessing the Code

All code can be accessed in the `root_directory/traffic_sign_detection` directory. For example, if the root directory is `/home/user/projects`, then the code would be located at `/home/user/projects/traffic_sign_detection`.



## Installation Instructions

1. Clone the repository:

    ```bash
    git clone https://github.com/felipeinagaki/traffic_sign_detection.git
    ```

2. Navigate to the project directory:

    ```bash
    cd traffic_sign_detection
    ```

3. Install the package using pip:

    ```bash
    pip install -r requirements.txt.
    ```
4. Run the Get_data notebook to retrieve our training data (optional)

5. Run the train notebook to repeat out training process (optional)

6. Download your video on a video_test folder. You can work with any kind of input, such as images, but you will need to adapt the code. Instructions can be found here: https://docs.ultralytics.com/modes/predict/

7. Run the inference notebook 

## Repository Structure

- `results/`: Folder containing the video result with our approach.

- `README.md`: Main documentation file.

- `runs/detect`: Folder with our trained models
- `docs/`: Documentation files for the project.
    - `imgs/`: Images used in the documentation.

    
```{sh} 
traffic_sign_detection/
│
├── results/
│   ├── detect/
│       └── combined.mp4
│   └── track/
│       └── combined.mp4
├── docs/
│   ├── final_report.pdf
│   └── imgs/
│      
│
├── runs/detect
│   ├── rtdetr-l_trained
│   ├── yolov8m_trained
│   ├── yolov8n_trained
│   └── yolov8s_trained
│
  
```

