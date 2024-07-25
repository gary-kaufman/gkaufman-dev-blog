---
date: 2024-07-25
authors: 
  - gary-kaufman
categories:
  - Python
---

# Python: Download High Quality YouTube Videos

This guide will explain how to download the highest quality video/audio files from YouTube using a Python library.

<!-- more -->

!!! note
    You will also have to use a movie maker software to combine the video/audio files.

Firstly, you will need Python installed. You will also need the [GitHub repo](https://github.com/gary-kaufman/garys-pytube-video-downloader) related to this project. Clone this repo locally.

When opening the project in your favorite IDE/text editor (I used PyCharm) firstly, pip install the needed dependencies:

```commandline
pip install pytubefix
```

Now work your way to the `main.py` file to where you will replace the url with your selected video url:

```python
url = "https://youtu.be/2jVBWyih-RU?si=Gne7gjpW_XlFIu5G"
```

Now add a breakpoint on the following line:

```python
yt.streams.filter()
```

Now using an IDE, debug the programming, stopping on the above breakpoint. This will allow you to inspect the `yt` object.

You are looking for the `itag_index` array that is nested in `yt` as `yt.streams.itag_index`.

![A gif to show how to find the itag](../gifs/find_itag.gif)

I chose the following video and audio file because they were of the highest quality. I chose the `webm` video format because it worked best with Clipchamp.

![Video File Image](../images/python-youtube-download/video-file.png)
![Audio File Image](../images/python-youtube-download/audio-file.png)

Now change the line of code with your selected `itag` and run the script, then do it again for the other file.

```python
    stream = yt.streams.get_by_itag(248)
```
After this, head into Clipchamp and import both files in the project.

![Place both files inside the project](../images/python-youtube-download/add-files-to-project.png)

Then place them on the timeline together!

![Place media on timeline](../images/python-youtube-download/place-files.png)

Finally, use the `Export` button in the upper-right hand corner to export your video to your computer!

![Export button in Clipchamp](../images/python-youtube-download/export.png)

Thanks for taking a chance to read this guide. I hope you found it helpful!
