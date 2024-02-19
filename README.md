# Download Youtube data. Ref: https://research.google.com/youtube8m/download.html
# To download youtube data, please use the following command. 
# You may start downloading a handful of shards, start developing the code, and later on kick off downloading the full shards


# Downlod video-level data
mkdir -p ~/data/yt8m/video; cd ~/data/yt8m/video

curl data.yt8m.org/download.py | partition=2/video/train mirror=us python
curl data.yt8m.org/download.py | partition=2/video/validate mirror=us python
curl data.yt8m.org/download.py | partition=2/video/test mirror=us python