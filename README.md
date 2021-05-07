# run NSFW model as a service

## How to use
```
git clone https://github.com/yahoo/open_nsfw.git
cd open_nsfw/nsfw_model/
```
using docker:
```
docker run -p 0.0.0.0:3005:3005 --volume=$(pwd):/workspace bvlc/caffe:cpu python ./server.py --model_def nsfw_model/deploy.prototxt --pretrained_model nsfw_model/resnet_50_1by2_nsfw.caffemodel
```
get NSFW score:
```curl localhost:3005:/http://image.location.jpg```


