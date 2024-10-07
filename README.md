# [EgoOops](https://y-haneji.github.io/EgoOops-project-page/ "Project page") annotations

## Overview

This is the official repository for annotations of the EgoOops dataset proposed in [EgoOops: A Dataset for Mistake Action Detection from Egocentric Videos with Procedural Texts](https://y-haneji.github.io/EgoOops-project-page/, "Project page").

## Annotations

[`meta/metadata.json`](/meta/metadata.json): annotations of video-text alignment (time stamps and steps), mistake labels, descripion explaining errors

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

[`meta/microqr/${task_id}.json`](/meta/microqr/): alignment between the number embedded in a QR code attached an object and the name of the object

[`meta/mistake_classes.json`](/meta/mistake_classes.json): a list of the names of the annotated mistake classes

## Videos

Download the videos from [our laboratory's web page](http://www.lsta.media.kyoto-u.ac.jp/resource/data/EgoOops/videos-processed-720p.zip)

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

## License

<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="https://y-haneji.github.io/EgoOops-project-page/">EgoOops</a> by <a rel="cc:attributionURL dct:creator" property="cc:attributionName" href="https://y-haneji.github.io/homepage/">Yuto Haneji</a> is licensed under <a href="https://creativecommons.org/licenses/by-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-SA 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1" alt=""></a></p>

## BibTex

```bibtex
@misc{haneji2024egooops,
  title={EgoOops: A Dataset for Mistake Action Detection from Egocentric Videos with Procedural Texts},
  author={Haneji, Yuto and Nishimura, Taichi and Kameko, Hirotaka and Yoshida, Tomoya and Shirai, Keisuke and Kajimura, Keiya and Yamamoto, Koki and Cui, Taiyu and Nishimoto, Tomohiro and Mori, Shinsuke},
  year={2024},
  eprint={TBW},
  archivePrefix={arXiv},
  primaryClass={cs.CV}
}
```
