# DeepLens
using Deep Lens for project on individuals self-monitoring of a skin condition

## Consists of primary data and machine-learning Jupyter notebook for training
-- note the data consists of primary images and masks to enable scoring of the segmentation

## To build the project
### Steps
1) Have setup and installed DeepLens as specified by AWS documentation, should have account access and registration of the device, along with at least an initial model installed to verify that the Deep Lens device is working correctly
2) MQTT and IoT needs to be set up with appropriate policy permissions and links to the ARN for Deep Lens
3) Lambda function needs to be modified for each Deep Lens registration and for the MQTT/IoT, the code in the repository can be modified for the appropriate permissions
4) Testing of the output is from a video stream of pictures and the MQTT streaming results; to accomplish that please set up the console monitor (e.g. in our case the http is: https://s3-us-west-2.amazonaws.com/im-examples/console/index.html?region=us-east-1&host=a3u3tjptc1o2rk.iot.us-east-1.amazonaws.com&id-pool=us-east-1:94124864-7a94-4976-8ec8-02443779e9f8)
5) This same endpoint is used for our App (seen in the YouTube) and enables the streaming video analysis from the DeepLens to be seen on the App
6) Note that video as well as text is enabled in the MQTT
7) We plan to do more Machine Learning training, both MXNet and TensorFlow.  The submission is based on the Caltech classifiction work (http://www.vision.caltech.edu/Image_Datasets/Caltech256/) 
8) Note that the original data is from a dataset collected in France, two years back: https://github.com/EliseTellier/Medical-Image-Processing/tree/master/data/skinimg
9) We plan to further enlarge this dataset and to look at the use of machine-learning algorithms for dealing with noise (in our case especially changes in lighting, focus, and image sizes).  For this later step we will be using ideas from this paper: https://arxiv.org/abs/1701.06487

