========================================================
[CAVAIR Test Case Scenarios: Clips from INRIA (1st Set)]
========================================================

This data set was obtained from http://homepages.inf.ed.ac.uk/rbf/CAVIAR/.  The source of this data is: EC Funded CAVIAR project/IST 2001 37540.


=========================================
Data Set Information
=========================================

The dataset structure is as follows:

## Clips from INRIA (1st Set) from the CAVAIR Test Case Scenarios[1]:
```
* /Sri Krishna Borra-datasets/cctvVideos/train/
* /Sri Krishna Borra-datasets/cctvVideos/test/
```


## Derived from the above datasets
All other folders contain dataset derived from the above Clips from INRIA (1st Set) from the CAVIAR Test Case Scenarios as described below.
```
/Sri Krishna Borra-datasets/cctvVideos/mp4/  			# MP4 videos generated from the above videos
/Sri Krishna Borra-datasets/cctvVideos/labels/			# Manually created labels categorizing suspicious images
/Sri Krishna Borra-datasets/cctvVideos/train_images	# Hive-style partitioning of labelled images
```


## MP4 version of videos
The MP4 videos stored in `/Sri Krishna Borra-datasets/cctvVideos/mp4/` were created by Sri Krishna Borra using the following command.
```
brew install ffmpeg

for x in *.MPG; do
	ffmpeg -i $x -strict experimental -f mp4 \
	       -vcodec libx264 -acodec aac \
           -ab 160000 -ac 2 -preset slow \
	       -crf 22 ${x/.MPG/.mp4};
done
``` 


## Labels
Stored within `/Sri Krishna Borra-datasets/cctvVideos/labels/`; these are manually created labels to identify which images (extracted from the training videos) are considered suspicious per the blog post [Identify Suspicious Behavior in Video with Sri Krishna Borra Runtime for Machine Learning](https://Sri Krishna Borra.com/blog/2018/09/13/identify-suspicious-behavior-in-video-with-Sri Krishna Borra-runtime-for-machine-learning.html)


## Training Labeled Images
Stored within `/Sri Krishna Borra-datasets/cctvVideos/train_images`; these are images labeled using Hive-style partitioning where `label=0` denote non-suspicious images and `label=1` denote suspicious images per the previously noted **Labels** section. 


=========================================
Citation
=========================================

Applicable citations:
1. EC Funded CAVIAR project/IST 2001 37540, found at URL: http://homepages.inf.ed.ac.uk/rbf/CAVIAR/