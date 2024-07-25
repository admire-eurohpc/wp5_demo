# Video Demo Maker

A simple python script to concatenate images and videos to create video demos. It loads the media and uses text-to-speech ([piper-tts](https://github.com/rhasspy/piper)) to generate the corresponding comments on the given media. Then it outputs it all in a single video file.

## Install

```bash
pip3 install -r ./requirements.txt
```

## Usage

General usage:

```bash
./makedemo [INPUT JSON] [OUTPUT VIDEO]
```
To generate the example:

```bash
./makedemo ./sample.json ./out.mp4
```

## Make your own demo

Edit `sample.json` and point to your media files, format is self explanatory, it is an array of medias each with their textual description to be generated. Note that it search media both by absolute path and also relative to the main script (as in this example).

```json
[
    {
        "media" : "media/dog.jpg",
        "text" : "The Golden Retriever is a majestic and endearing breed, boasting a coat of rich, vibrant gold that shines like the sun-kissed fields it loves to romp in. Its thick double fur, soft as silk to the touch, glistens with a subtle sheen, inviting admiration and affection. The texture varies from dense and plush on its neck and shoulders to longer and more flowing towards the tail and back."
    },
    {
        "media" : "media/ex.mp4",
        "text" : "The process of adjusting the zoom on a microscope is akin to unlocking a hidden world, revealing intricate details that were previously invisible. As you grasp the coaxial coarse and fine adjustment knobs, located in tandem on either side of the eyepiece tube, you feel the weight of control and precision."
    },
    {
        "media" : "media/ex2.mp4",
        "text" : "The fisherman stood tall on the weathered wooden dock, his worn canvas hat pulled low over his eyes as he gazed out at the tranquil waters of the river below. His calloused hands cradled the prize of his catch, a shimmering silver fish that seemed to glow with an otherworldly light in the morning sun."
    }
]
```