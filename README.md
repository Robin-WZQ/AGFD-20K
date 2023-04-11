# A Generated Face Dataset: AGFD-30K

<div align=center>
    <img src=https://github.com/Robin-WZQ/AGFD-30/blob/main/logo.png width="700"/>
</div>

Can we use generated human face to train a model? If the model can generate faces that are realistic enough, how can we use it to generate faces we want? What is the mapping between prompt and vary human faces?

Besides, many times we need to construct a good test dataset to test the robustness of the trained model. But selecting images carefully from searching engines is laborious and also facing the problem of cleaning (due to the low quality of the data like: unrelated, low-resolution, unbalanced, etc.). How the diffusion model can help us solve this problem?

In the past 3 years, we have seen the explosive growth of the **Diffusion Model**, it now can generate brilliant pictures according to user's prompt. In this program, I test the diffusion model in the capacity of generating realistic human faces. And purposes of this program are the following two points:

1. Construct a not bad faces dataset for robustness testing;
2. Use these data to do something interesting. I don't know if it helps anyone, but it works for me 🤣🤣🤣 

The principles I followed in generated face are:

- Realistic (use **[Realistic_Vision_V2.0:1](https://civitai.com/models/4201/realistic-vision-v20)** by **[SG_161222](https://civitai.com/user/SG_161222)**)
- High-resolution (the resolution of all images are 512*512)
- Vary & Balanced (support vary faces and keep good data distribution)

Here is the generated face data and corresponding descriptions:

|  Attribute   |  Specific Features  | Male | Female |                        Special Prompt                        |
| :----------: | :-----------------: | :--: | :----: | :----------------------------------------------------------: |
|     Age      |     Child (0-5)     | 300  |  300   |                        1 y.o., 3 y.o.                        |
|              |   Teenager (5-18)   | 600  |  600   |                       8 y.o., 15 y.o.                        |
|              | Young adult (18-40) | 300  |  300   |                       25 y.o., 35 y.o.                       |
|              |  Old adult (40-60)  | 300  |  300   |                       45 y.o., 55 y.o.                       |
|              |      Old (60+)      | 600  |  600   |               60,80,100 y.o., Grandma，Grandpa               |
|   Emotion    |        Smile        | 600  |  600   |                      smiling, laughing                       |
|              |        Angry        | 600  |  600   |               Angry, pissed-off face, yelling                |
|  Occlusion   |    Only glasses     | 600  |  600   |     glasses,sunglasses,swimming goggles,skiing goggles,      |
|              |      Only mask      | 300  |  300   |                  (masked:1.2), antigas mask                  |
|              |    Only make up     | 300  |  300   | highly make up, eyeshadow,heavy black eyeliner, joker, Halloween makeup |
|              |     Only hands      | 300  |  300   |     put Hand in front of face,put Hand in front of hair      |
|              |       Complex       | 300  |  300   | glasses，(masked:1.2),Halloween makeup，put Hand in front of face,put Hand in front of hair |
| Illumination |     Under water     | 300  |  300   |                         under water                          |
|              |    Strong light     | 300  |  300   |              (sun behind:1.2), strong sun shine              |
|              |        Dark         | 300  |  300   |       in the night, dark light, (very dark scene:1.2)        |
|  Large pose  |    Left & right     | 2000 |  2000  |                          side view                           |
|              |         Up          | 300  |  300   |                       (looking up:1.3)                       |
|     Hair     |        Blond        | 300  |  300   |                          blond hair                          |
|              |        Brown        | 300  |  300   |                                                              |
|              |         Red         | 300  |  300   |                                                              |
|              |        Bangs        | 300  |  300   |                         (Bangs:1.5)                          |
|              |    Straight_Hair    | 300  |  300   |                                                              |
|              |      Wavy_Hair      | 300  |  300   |                                                              |
|              |        Bald         | 300  |  300   |                             man                              |
|    Others    |     Small scale     | 2000 |  2000  |                           clothes                            |
|              |      Mustache       | 300  |  300   |                  mustache,sideburns,goatee                   |
|              |         Hat         | 300  |  300   |                                                              |
|              |       Blurry        | 300  |  300   |                                                              |
|              |     Open Mouse      | 300  |  300   |                      screaming, cfg:15                       |
|              |     Close Eyes      | 300  |  300   |                   sleepy, (close eyes:1.2)                   |
|              |      Earrings       | 300  |  300   |                                                              |
|     ALL      |         all         | 30K  |  30K   |                                                              |

All the pictures can be downloaded at Google Drive | Baidu Disk.

## Usage

> **A more detailed instructions are available at [HERE](https://github.com/Robin-WZQ/AGFD-30K/blob/main/Instructions.md).**

I use this template to get good generation results:

- **Prompt:**

RAW photo, a close up portrait photo of [*year*] y.o [*sex*], [*human race*],[*special prompt*],(high detailed skin:1.2), 8k uhd, dslr, high quality, film grain, Fujifilm XT3.

- **Negative Prompt:**

(deformed iris, deformed pupils, semi-realistic, cgi, 3d, render, sketch, cartoon, drawing, anime:1.4), text, close up, cropped, out of frame, worst quality, low quality, jpeg artifacts, ugly, duplicate, morbid, mutilated, extra fingers, mutated hands, poorly drawn hands, poorly drawn face, mutation, deformed, blurry, dehydrated, bad anatomy, bad proportions, extra limbs, cloned face, disfigured, gross proportions, malformed limbs, missing arms, missing legs, extra arms, extra legs, fused fingers, too many fingers, long neck.

- **Hyper-parameter:**

DPM++ 2M Karras with 20 steps

CFG Scale 7

## Acknowledgement

Thanks the creator of the model for his brilliant work and also thanks his reference models. 

 **[Realistic_Vision_V2.0:1](https://civitai.com/models/4201/realistic-vision-v20)** by **[SG_161222](https://civitai.com/user/SG_161222)**

## Future Work

- I will use this fake faces to launch a program of facial landmark detection. In my plan, the program supports 240 points and keeps a good capacity under complex scene (like large pose, occlusion, extreme expression…). Also, it supports both large model and tiny model (pth & onnx), for mobile using.
- keep expanding the dataset.

## Citation

```
@repo{2023agfd30k,
    title={A Generated Face Dataset: AGFD-30K},
    author={Robin_WZQ},
    howpublished = {\url{https://github.com/Robin-WZQ/AGFD-30K}},
    year={2023}
}
```


