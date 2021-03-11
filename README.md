# kmeans4yolo

Kmeans algorithm for Yolo anchor boxes.

## Usage

Just import this python file and use it.

## Example
```
import numpy as np
from numpy.random import rand
import matplotlib.pyplot as plt
from kmeans import kmeans, iou_dist

n_data = 100
data_boxes = rand(n_data*2).reshape((n_data, 2))

center = kmeans(data_boxes,
                n_cluster=3,
                dist_func=iou_dist,
                stop_dist=0.01)

plt.scatter(data_boxes[..., 0], data_boxes[..., 1])
plt.scatter(center[..., 0],
            center[..., 1])
plt.title("Use random data as an example")
plt.legend(["data", "center"])
plt.show()
```
or type ```python kmeans.py``` in your terminal.
