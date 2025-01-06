# SR-YOLO-Dataset: Strawberry fruit target detection data set of different ripeness

 [![CC BY-NC-SA 4.0][cc-by-nc-sa-shield]][cc-by-nc-sa]
 
## Introduction
This repository is built for:

SR-YOLO-Dataset: A data set for target detection of strawberry


The SR-YOLO-Dataset includes more than 15,000 photos of strawberries of different ripenness

      

## How to use
To train a network on the RS-YOLO-Dataset make sure that you download the code first from [yolo11](https://github.com/ultralytics/ultralytics). And then clone this repository to yolov8 folder and  train a yolo11 network with the commands below.

```
# Clone yolo11 repo and install requirements.txt
git clone https://github.com/ultralytics/ultralytics  # clone
cd yolo11
pip install -r requirements.txt  # install
```

```
# Clone this repository to yolo11 folder
git clone https://github.com/ganyang0720/SR-YOLO
```

```
# Train yolo11
yolo detect train data=RS-YOLO-Dataset/dataset.yaml model=yolo11n.yaml epochs=200 imgsz=640
```



## License

This work is licensed under a
[Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License][cc-by-nc-sa].

[![CC BY-NC-SA 4.0][cc-by-nc-sa-image]][cc-by-nc-sa]

[cc-by-nc-sa]: http://creativecommons.org/licenses/by-nc-sa/4.0/
[cc-by-nc-sa-image]: https://licensebuttons.net/l/by-nc-sa/4.0/88x31.png
[cc-by-nc-sa-shield]: https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg
