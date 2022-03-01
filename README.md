# Pedestrian Speed Estimation using yolov5, deepsort and homography matrix

## Demo gif

<img src="MOT16_eval/demo.gif" width="600"/>

## Before you run the tracker

1. Clone the repository

2. Install dependencies

`pip install -r requirements.txt`

## Download weights 

Download [weights](https://drive.google.com/file/d/1gglIwqxaH2iTvy6lZlXuAcMpd_U0GCUb/view?usp=sharing) and place it in yolov5/weights folder

## Quick run
Add a video to data/videos folder and run the following command.

```bash
python track.py --source data/videos/test.mp4 --yolo_model yolov5/weights/crowdhuman_yolov5m.pt --classes 0 --show-vid --save-vid
```

Results are saved to folder `track/expN`

## Tracking sources

Tracking can be run on most video formats

```bash
$ python track.py --source 0  # webcam
                           img.jpg  # image
                           vid.mp4  # video
                           path/  # directory
                           path/*.jpg  # glob
                           'https://youtu.be/Zgi9g1ksQHc'  # YouTube
                           'rtsp://example.com/media.mp4'  # RTSP, RTMP, HTTP stream
```

### DeepSort

Choose a ReID model based on your needs from this ReID [model zoo](https://kaiyangzhou.github.io/deep-person-reid/MODEL_ZOO)

```bash


$ python track.py --source 0 --deep_sort_model osnet_x1_0
                                               nasnsetmobile
                                               resnext101_32x8d
                                               ...
```
## Reference

```latex
@misc{yolov5deepsort2020,
    title={Real-time multi-object tracker using YOLOv5 and deep sort},
    author={Mikel Broström},
    howpublished = {\url{https://github.com/mikel-brostrom/Yolov5_DeepSort_Pytorch}},
    year={2020}
}
```