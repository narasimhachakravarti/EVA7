# YOLOV3OpenCV

OpenCV Inference using YOLOV3

### Load YOLOv3 model

```python
net = cv2.dnn.readNet("yolov3.weights", "yolov3.cfg")
classes = []
with open("coco.names", "r") as f:
    classes = [line.strip() for line in f.readlines()]
layer_names = net.getLayerNames()
output_layers = [layer_names[i[0] - 1] for i in net.getUnconnectedOutLayers()]
colors = np.random.uniform(0, 255, size=(len(classes), 3))
```

### Upload Image for inference

[![image.png](https://github.com/narasimhachakravarti/EVA7/blob/main/Images/11a-output.png)](https://github.com/narasimhachakravarti/EVA7/blob/main/Images/11a-output.png)

### Reference

https://pysource.com/2019/06/27/yolo-object-detection-using-opencv-with-python/
