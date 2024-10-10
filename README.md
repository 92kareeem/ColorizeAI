# ColorizeAI
To recreate memories of B/w images.Advanced deep learning model for automatic image colorization from grayscale (B/W) Images.
   ![image](https://github.com/user-attachments/assets/a94c8252-a28b-4284-889d-ced25face5aa)


**+ automatic colorization functionality for Real-Time User-Guided Image Colorization with Learned Deep Priors, SIGGRAPH 2017!**

I converted this repo to support minimal test-time usage in PyTorch. I also added our SIGGRAPH 2017 (it's an interactive method but can also do automatic). See the [Caffe branch](https://github.com/richzhang/colorization/tree/caffe) for the original release.

**Clone the repository; install dependencies**

```
git clone https://github.com/92kareeem/ColorizeAI.git
pip install requirements.txt
```

**Colorize!** This script will colorize an image. The results should match the images in the output.

```
python main.py -i input_img/bw.jpg
```

**Model loading in Python** The following loads pretrained colorizers. See [demo_release.py](demo_release.py) for some details on how to run the model. There are some pre and post-processing steps: convert to Lab space, resize to 256x256, colorize, and concatenate to the original full resolution, and convert to RGB.

```python
import colorizers
colorizer_eccv16 = colorizers.eccv16().eval()
colorizer_siggraph17 = colorizers.siggraph17().eval()
```

### Original implementation (Caffe branch)

The original implementation contained train and testing, our network and AlexNet (for representation learning tests), as well as representation learning tests. It is in Caffe and is no longer supported. Please see the [caffe](https://github.com/richzhang/colorization/tree/caffe) branch for it.

### Citation ###

If you find these models useful for your resesarch, please cite with these bibtexs.




