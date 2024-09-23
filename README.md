This project introduces an enhanced version for instance segmentation, bringing more precise and scalable object detection capabilities. This update includes a significant upgrade to the validation process, integrating COCO dataset metrics to provide a comprehensive performance overview.

Key Features:

Instance Segmentation Upgrade: The enhance version focuses on better delineating individual objects, making it especially suitable for complex scenes where multiple objects overlap or are closely packed. Referred to gelan-e-dseg.yaml;
gelan-e-seg.yaml

Expanded Metrics for Validation: Validation now includes multiple COCO dataset metrics such as 'mAP' (mean Average Precision), 'mAP_50', 'mAP_75', and size-specific mAPs ('mAP_s', 'mAP_m', 'mAP_l'). These metrics provide a granular insight into model performance across different object scales and detection thresholds.

Configuration Changes in val_dual.py: Users must modify the anno_json variable at line 359 to direct to the correct .json path for labels. This change is crucial for accurately assessing model performance against the annotated instances.

Enhanced Metric Calculations in utils/metrics.py: The script has been updated to output detailed precision, recall, and F1-score metrics during validation. It now provides metrics at ten different Intersection over Union (IoU) thresholds, ranging from 0.5 to 0.95 in steps of 0.05. This includes maximum precision, recall, F1-score, as well as average values across these thresholds.

This enhanced YOLOv9 model is designed for researchers and developers needing robust and accurate instance segmentation tools. The updated validation metrics and configuration requirements ensure that users can fully leverage the improved functionalities for their specific use cases.



Acknowledgements 

This project is based on 'YOLOv9: Learning What You Want to Learn Using Programmable Gradient Information' and https://github.com/WongKinYiu/yolov9/tree/main.
