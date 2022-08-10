# Highres Deepdream 

The size/resolution limitation of the original deepdream Caffe implementation made deep dreaming large photos tricky. However, the [offical Google Deepdream example that comes with Tensorflow](https://github.com/tensorflow/tensorflow/blob/master/tensorflow/examples/tutorials/deepdream/deepdream.ipynb) by Alex Mordvintsev, doesnt suffer from those limitations. However it only came as a IPython notebook, so here's a little commandline app based on Alex's notebook for just applying deepdream to large images in bulk. 

Install Requirements:

- Python 3
- TensorFlow (>=r0.7)
- NumPy

Download pretrained Inception V5 from here:
https://storage.googleapis.com/download.tensorflow.org/models/inception5h.zip

Run deepdream like this:
  py deepdream.py --input .\images\DSC01845.jpg --output .\3\sleepTomas2 --layer mixed5a_3x3_pre_relu --frames  1  --octaves 14 --iterations  5 --feature 50

py deepdream.py --input .\
images\DSC01845medres.jpg --output .\15\onewhithnature --layer mixed4e_1x1_pre_re
lu --frames  250  --octaves 8 --iterations  1 --feature 141 --octave_scale 1.3

Or create a zoom-in series like so:

python deepdream.py --input mystart.jpg --output output.jpg --layer import/mixed4d_3x3 --frames 100 --frame_scale 1.4 --frame_crop --octaves 4  --iterations  10

For help & options:
 python deepdream.py --help
