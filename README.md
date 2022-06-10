# ECE-228-Porject

This respository is used fro UCSD Spring 2022 ECE 228 project.

To run our program of Faster R-CNN, you need to first download Torchvision from this url:https://github.com/pytorch/vision. 
Then, repalce our detection folder to reference/detetion in the torchvision. And also put the data tt100k_2021 under detetion folder. 
Third, cearte a folder named annotations inside the tt100k_2021 dataset.
Last, go back to detetion folder run the command:

torchrun --nproc_per_node=1 train.py --dataset coco --data-path=data/tt100k_2021 --lr = 0.0001 --model fasterrcnn_resnet50_fpn --epochs 20 --lr-steps 16 22 --aspect-ratio-group-factor 3 --weights-backbone ResNet50_Weights.IMAGENET1K_V1

To run our YOLOv4 model. Please check the readme under that folder.
