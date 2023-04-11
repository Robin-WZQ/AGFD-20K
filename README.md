# A Generated Face Dataset: AGFD-30K

<div align=center>
    <img src=https://github.com/Robin-WZQ/AGFD-30/blob/main/logo.png width="700"/>
</div>

Many times, we may find that our trained model does not work well on some special samples. But collecting these data from search engines is laborious and requires a long time of cleaning (due to the low quality of the data, like: unrelated, low-resolution, unbalanced, etc.)

Thanks to the **Diffusion Model,** we can generate the data we need from prompt. I have generated the following **face portraits** for someone in need. Although the amount of data is not large, it is enough for fine-tuning. (At least it can be used for **testing** the robust capacity of the model 🤣🤣🤣 )

The principles I followed in generated face are:

- Realistic (use [Realistic_Vision_V2.0:1](https://civitai.com/models/4201/realistic-vision-v20) from civitai.com)
- High-resolution (the resolution of all images are 512*512)
- Vary & Balanced (support vary faces and keep good data distribution)

Here is the generated face data and corresponding descriptions:

**A more detailed instructions are avaliable at [HERE](https://github.com/Robin-WZQ/AGFD-30K/blob/main/Instructions.md).**


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



### Thanks

RAW photo, a close up portrait photo of 2 y.o child boy, skin pores,  big face,(high detailed skin:1.2),soft lighting, 8k uhd, dslr, high quality, film grain, Fujifilm XT3

 African, pale skin, Asian, Middle East, Latino

(deformed iris, deformed pupils, semi-realistic, cgi, 3d, render, sketch, cartoon, drawing, anime:1.4), text, close up, cropped, out of frame, worst quality, low quality, jpeg artifacts, ugly, duplicate, morbid, mutilated, extra fingers, mutated hands, poorly drawn hands, poorly drawn face, mutation, deformed, blurry, dehydrated, bad anatomy, bad proportions, extra limbs, cloned face, disfigured, gross proportions, malformed limbs, missing arms, missing legs, extra arms, extra legs, fused fingers, too many fingers, long neck

### Future Work

- I will use this fake faces to launch a program of facial landmark detection. In my plan, the program supports 280 points and keep a good capacity under complex scene (like large pose, occlusion, extreme expression…). Also, it supports both large model and 轻量 model (pth & onnx), for mobile using.
- keep 扩充数据
- 尝试应用在更多的任务上

### Citation

