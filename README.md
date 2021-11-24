# Tensorflow Object Detection with Tensorflow 2

In this repository you can find some examples on how to use the Tensorflow OD API with Tensorflow 2. 
Referenced from [Tensorflow Object Detection with Tensorflow 2 (Gilbert Tanner)](https://gilberttanner.com/blog/object-detection-with-tensorflow-2)

This TF2 OD example code was used for the demo in my talk, UP ACM Fest 2021 "AI Hackathon: Building Your First Prototype"

Accompanying slides can be found here: [Google Slides Link](https://bit.ly/acmfest_ai_prototyping)

## I. Project Setup

1. Creating python virtual env

```bash
$ python3 -m venv ~/venvs/[name_of_env]

e.g.
$ python3 -m venv ~/venvs/tf-od
```
2. Activating python virtual env

```bash
$ source ~/venvs/[name_of_env]/bin/activate

e.g.
$ source ~/venvs/tf-od/bin/activate
```

3. Install the project's requirements

```bash
$ pip3 install -r requirements.txt
```


### II. Download Pre-trained Model

1. Go to [TF Object Detection Model Zoo](https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf2_detection_zoo.md) 

2. Choose one of the models and download

3. Extract 

**For the example output, `efficientdet_d2_coco17_tpu-32` was used

### III. Video Inference

1. Upload your video in the `vids` folder

2. Run the following command but replace the parameters as needed

```
python3 detect_from_video.py --model=efficientdet_d2_coco17_tpu-32/ \
                                --video_path=vids/smarthome.mp4 \
                                --labelmap=mscoco_label_map.pbtxt
```

3. Your video output should be inside the `outputs` folder
