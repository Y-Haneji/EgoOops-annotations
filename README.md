# [EgoOops](https://y-haneji.github.io/EgoOops-project-page/ "Project page") annotations

## Overview

EgoOops is a dataset collecting egocentric videos where workers follow procedural texts.
The video contains mistake actions.

## Annotations

`meta/metadata.json`: annotations of video-text alignment (time stamps and steps), mistake labels, descripion explaining errors

```json
{
    "videos": [
	{
	    "task_id": str,
	    "video_id": str,
	    "segments": [
		{
		    "startTime": float (seconds),
		    "endTime": float (seconds),
		    "instruction": int (zero-based index),
		    "labels": list[int] (zero-based index, an empty list means a correct step),
		    "caption": str (an empty string means a correct step),
		},
		...
	    ],
	},
	...
    ],
    "instructions": {
	"blacklight": list[str],
	...
    }
}
```

`meta/microqr/${task_id}.json`: alignment between the number embedded in a QR code attached an object and the name of the object

`meta/mistake_classes.json`: a list of the names of the annotated mistake classes 

## Videos

Download the videos from our laboratory's web page: http://www.lsta.media.kyoto-u.ac.jp/resource/data/EgoOops/

```
|-- blacklight
|   |-- S1800001.MP4
|   |-- S1800002.MP4
|   ...
|
|-- cardboard
|   ...
|
...
```

## The conversion table of task names

The task names in the dataset are different from ones used in the paper. Refer to the table below.

| Dataset     | Paper                           |
| :---------- | :------------------------------ |
| blacklight  | ionic reaction experiments (IR) |
| cardboard   | cardboard crafts (CB)           |
| electronics | electrical circuits (EC)        |
| ion         | ionic reaction experiments (IR) |
| tsumiki     | toy block building (BB)         |

