# FAQ

## The original model is sensitive to the resolution of the data it was trained on
    
So this are correct resolutions for the weights

- Tusimple 1280×720
- Culane 1640×590
    
Got to improve generalization ability of the model

- Increase data size for trainning, addtional datasets
- Run with origin resolution or the similar scale ration
    
So choose to preprocess the image size to 352*640 due to the 'h' of final input size should be divisible by 32 from reading the source code

- CULane, cropping 284 pixels both side
- CurveLanes, cropping 32 pixels on the top of image and scaling it by 4 times
    
## The 0, 1 behind gt_image is not used so it can be omitted