# Tensorflow Object Detection with Tensorflow 2
This repo was forked from 
[Gilbert Tanner](https://github.com/TannerGilbert/Tensorflow-Object-Detection-with-Tensorflow-2.0) and adds some minor
changes to go with my YouTube tutorial series.
---
## [How to Install Tensorflow 2 Object Detection:](https://www.youtube.com/watch?v=rRwflsS67ow&t=28s&ab_channel=LazyTech)
![thumbnail](./misc/Tensorflow%202%20Object%20Detection.jpg)

## [Tensorflow 2 Object Detection on Webcam and Videos:](https://www.youtube.com/watch?v=O6BsjQat4aE&ab_channel=LazyTech)
![thumbnail](./misc/Tensorflow%202%20Object%20Detection%20on%20Webcam%20and%20Videos.jpg)

## [Tensorflow 2 Custom Object Detection Model](https://youtu.be/8ktcGQ-XreQ)
![thumbnail](./misc/Tensorflow%202%20Custom%20Model.jpg)

---

## Some commands used:
*Note: You will probably need to update path names and model names in these commands to match your own environment*
#### Generate TF records
`python generate_tfrecord.py --csv_input=images/test_labels.csv --image_dir=images/test --output_path=test.record`<br>
`python generate_tfrecord.py --csv_input=images/train_labels.csv --image_dir=images/train --output_path=train.record`
#### Start training
`python model_main_tf2.py --pipeline_config_path==ssd_efficientdet_d0_512x512_coco17_tpu-8.config 
--model_dir==training --alsologtostderr`
#### Export graph
`python exporter_main_v2.py --trained_checkpoint_dir=training 
--pipeline_config_path=ssd_efficientdet_d0_512x512_coco17_tpu-8.config --output_directory inference_graph`

### Potential future work:
- Extraction of objects detected
- Recording position data of detections
- Robot or physical device that uses results of detection (i.e. robot arm)
- 
- **Leave suggestions of other things you'd like to see!**

### Forked Repo Author
 **Ben Greenfield**
### Original Author
 **Gilbert Tanner**