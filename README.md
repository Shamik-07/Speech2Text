# Speech2Text with Transformers

The entire repo has been tested on Ubuntu-18.04. \
The environment with their relevant packages can be installed through the `environment.yml` file.

The `data/` folder contains all the audio files. \
The ouputs of the full transcripts are under `outputs/`.\
Under `notebooks/` there is a notebook to download, extract audio and make short video clips of YouTube videos, along with other notebooks. 

All audio has been converted using the ffmpeg tool and can be installed through bash. 

Some examples of audio conversions.

ffmpeg converting mp3 into a flac with sr=16000 and for initial 45 sec 
```sh
ffmpeg -i apple/Q4\ FY21\ Apple\ Quarterly\ Earnings\ Cal.mp3 -ar 16000  -t 45 apple/Q4\ FY21\ Apple\ Quarterly\ Earnings\ Cal45sec_1.flac
```
ffmpeg converting mp3 into a flac with sr=16000 and for a specific time period 
```sh
ffmpeg -i apple/Q4\ FY21\ Apple\ Quarterly\ Earnings\ Cal.mp3 -ar 16000  -ss 00:00:05 -t 00:00:10 apple/Q4\ FY21\ Apple\ Quarterly\ Earnings\ Cal45sec_1.flac
```
Additional links for ffmpeg commands [link](https://gist.github.com/protrolium/e0dbd4bb0f1a396fcb55)

**Note:** ffmpeg cannot convert all types of video and one might need to install additional software decoder e.g., for AV1, more info [here](https://stackoverflow.com/a/68174327)


---
