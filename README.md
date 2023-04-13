# A Generated Face Dataset: AGFD-25K

<div align=center>
    <img src=https://github.com/Robin-WZQ/AGFD-30/blob/main/logo.png width="700"/>
</div>

Can we use generated human faces to train a model? If the model can generate faces that are realistic enough, how can we use it to generate faces we want? What is the mapping between prompt and vary human faces?

Besides, many times we need to construct a good test dataset to test the robustness of the trained model. But selecting images carefully from searching engines is laborious and also facing the problem of cleaning (due to the low quality of the data like unrelated, low-resolution, unbalanced, etc.). How the diffusion model can help us solve this problem?

In the past 3 years, we have seen the explosive growth of the **Diffusion Model**, it now can generate brilliant pictures according to user's prompt. Here I test the diffusion model in the capacity of generating realistic human faces. And purposes of this project are the following two points:

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
|              |      Mustache       | 300  |   -    |             mustache,sideburns,goatee,front view             |
| Illumination |     Under water     | 300  |  300   |                         under water                          |
|              |    Strong light     | 300  |  300   |              (sun behind:1.2), strong sun shine              |
|              |        Dark         | 300  |  300   |       in the night, dark light, (very dark scene:1.2)        |
|  Large pose  |    Left & right     | 2000 |  2000  |                          side view                           |
|              |         Up          | 300  |  300   |                       (looking up:1.3)                       |
|     Hair     |        Blond        | 300  |  300   |                          blond hair                          |
|              |        Bangs        | 300  |  300   |                         (Bangs:1.2)                          |
|              |        Bald         | 300  |  300   |                             Bald                             |
|    Others    |     Small scale     | 2000 |  2000  |                           clothes                            |
|              |     Open Mouse      | 600  |  600   |              (talking loudly:1.4),smile,neutral              |
|              |     Close Eyes      | 600  |  600   |                    (sleep,close eyes:1.4)                    |
|     ALL      |       origin        | 25K  |  25K   |                              -                               |
|              |       aligned       | 25K  |  25K   |                              -                               |

All the pictures can be downloaded at Google Drive | Baidu Disk.

## Usage

I use this template to get good generation results:

- **Prompt:**

RAW photo, a close up portrait photo of [*year*] y.o [*sex*], [*human race*],[*special prompt*],(high detailed skin:1.2), 8k uhd, dslr, high quality, film grain, Fujifilm XT3.

- **Negative Prompt:**

(deformed iris, deformed pupils, semi-realistic, cgi, 3d, render, sketch, cartoon, drawing, anime:1.4), text, close up, cropped, out of frame, worst quality, low quality, jpeg artifacts, ugly, duplicate, morbid, mutilated, extra fingers, mutated hands, poorly drawn hands, poorly drawn face, mutation, deformed, blurry, dehydrated, bad anatomy, bad proportions, extra limbs, cloned face, disfigured, gross proportions, malformed limbs, missing arms, missing legs, extra arms, extra legs, fused fingers, too many fingers, long neck.

- **Hyper-parameter:**

DPM++ 2M Karras with 20 steps

CFG Scale 7

## Instruction

A reference containing Portraits and Keywords that you can use with Stable Diffusion.

- <details><summary> Age </summary><p><div align="center">

  | 1 y.o., 3 y.o., boy | 1 y.o., 3 y.o., girl |
  | :-----------------: | :------------------: |
  |       ![young_child_small](https://user-images.githubusercontent.com/60317828/230921787-eae427f4-2655-4fc8-9195-420186f6fe04.png)|        ![young_child_girl_small](https://user-images.githubusercontent.com/60317828/230921807-59d9291f-ea97-415f-a3a7-6648bab9f638.png)|

  <br>
  
  | 8 y.o., 15 y.o., boy | 8 y.o., 15 y.o., girl |
  | :------------------: | :-------------------: |
  |                ![teenager_man_small](https://user-images.githubusercontent.com/60317828/230921966-818d3088-4428-4e35-816d-5e0734dce315.png) |         ![teenager_woman_small](https://user-images.githubusercontent.com/60317828/230921910-37680c5c-a2be-4cd1-b256-661e787f270e.png)   |

  <br>
  
  | 25 y.o., 35 y.o., man | 25 y.o., 35 y.o., woman |
  | :-------------------: | :---------------------: |
  |            ![young_adult_man_small](https://user-images.githubusercontent.com/60317828/230922592-21961c2c-faa1-42ae-906c-4fa06090dd55.png)|      ![young_adult_woman_small](https://user-images.githubusercontent.com/60317828/230925134-f457837e-77a5-44bf-b0b7-a6a0612680a5.png)          |

  <br>
  
  | 45 y.o., 55 y.o., man | 45 y.o., 55 y.o., woman |
  | :-------------------: | :---------------------: |
  |              ![old_adult_man_small](https://user-images.githubusercontent.com/60317828/230922649-00d3c796-bc83-42b1-8fc2-e19b8e77b56e.png)         |            ![old_adult_woman_small](https://user-images.githubusercontent.com/60317828/230922504-95a1249d-e5f2-4a9c-bcd5-6762beed53ed.png) |

  <br>
  
  | 60,80,100 y.o., man, grandpa | 60,80,100 y.o., woman,  grandma |
  | :--------------------------: | :-----------------------------: |
  |               ![Old_man_small](https://user-images.githubusercontent.com/60317828/230925226-7c507214-f8d3-4fb7-8dac-a12cd32082a8.png)          |                        ![old_woman_small](https://user-images.githubusercontent.com/60317828/231047264-152b8f4e-1182-4384-ad21-dae56cabe6ca.png)         |

- <details><summary> Emotion </summary><p><div align="center">

  | smiling, laughing, man | smiling, laughing, woman |
  | :--------------------: | :----------------------: |
  |            ![smile_man_small](https://user-images.githubusercontent.com/60317828/230925316-a333694d-a954-4af7-bc4b-8c82235658e2.png)            |               ![smile_woman_small](https://user-images.githubusercontent.com/60317828/230925301-196ca6ff-ab27-49f2-bf5b-2fc6d17dc875.png)           |

  <br>

  | Angry, pissed-off face, yelling, man | Angry, pissed-off face, yelling, woman |
  | :----------------------------------: | :------------------------------------: |
  |            ![angry_man png_small](https://user-images.githubusercontent.com/60317828/230921290-1a560151-1ae1-4344-9b83-88a31d202d6c.png)                          |                          ![angry_woman_small](https://user-images.githubusercontent.com/60317828/231047315-a88d0635-98d5-4efa-9a67-8547138bbdeb.png)              |

- <details><summary> Occlusion </summary><p><div align="center">

  | glasses,sunglasses,swimming goggles,skiing goggles, man | glasses,sunglasses,swimming goggles,skiing goggles, woman |
  | :-----------------------------------------------------: | :-------------------------------------------------------: |
  |                  ![glasses_man_small](https://user-images.githubusercontent.com/60317828/231047342-d98dcbbb-9a3e-4fac-816b-8e3fc894e559.png)                                       |                              ![glasses_Woman_small](https://user-images.githubusercontent.com/60317828/231047362-f9faff25-197d-4ccc-80d3-b58b9034403e.png)                             |

  <br>

  | (masked:1.2), antigas mask, man | (masked:1.2), antigas mask, woman |
  | :-----------------------------: | :-------------------------------: |
  |          ![mask_man_small](https://user-images.githubusercontent.com/60317828/231047415-c48c7579-234a-4256-9222-ae7a5e045b3b.png)          |                              ![mask_woman_small](https://user-images.githubusercontent.com/60317828/231047504-8fc9d908-7a04-4432-a5c0-83de6a547255.png)     |

  <br>

  | highly make up, eyeshadow,heavy black eyeliner, joker, Halloween makeup, man | highly make up, eyeshadow,heavy black eyeliner, joker, Halloween makeup, woman |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  |                                       ![makeup_man_small](https://user-images.githubusercontent.com/60317828/231047659-95262578-e0f1-417a-98cf-bb1d7bc988b0.png)                       |                                  ![makeup_woman_small](https://user-images.githubusercontent.com/60317828/231047639-04f0e031-dbb9-469e-ad79-a52f3c84ab48.png)                            |

  <br>

  | put Hand in front of face, put Hand in front of hair, man | put Hand in front of face, put Hand in front of hair, woman |
  | :-------------------------------------------------------: | :---------------------------------------------------------: |
  |                                      ![hand_man_small](https://user-images.githubusercontent.com/60317828/231047682-3593e531-043a-4a41-88e7-c7bbce34fd82.png)                     |                                            ![hand_Woman_small](https://user-images.githubusercontent.com/60317828/231047697-6113d99c-462b-47ca-bbec-fa353cb01259.png)                 |

  <br>

  | glasses，(masked:1.2), Halloween makeup，put Hand in front of face, put Hand in front of hair, man | glasses，(masked:1.2), Halloween makeup，put Hand in front of face, put Hand in front of hair, woman |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  |                        ![complex_man_small](https://user-images.githubusercontent.com/60317828/231047722-b0089d11-b441-4ec0-9df0-58b12abaad7d.png)                                      |                                            ![complex_woman_small](https://user-images.githubusercontent.com/60317828/231047732-c593a4a8-5ed1-4bd9-9a0a-b57350948607.png)                  |

- <details><summary> Illumination </summary><p><div align="center">

  | under water, man | under water, woman |
  | :--------------: | :----------------: |
  |         ![under_water_man_small](https://user-images.githubusercontent.com/60317828/231047856-2ec1c35e-e748-4e7b-a0cb-9dcedce40d01.png)         |         ![under_water_woman_small](https://user-images.githubusercontent.com/60317828/231047867-1f2a1644-5f2c-4509-85e6-510e829d0967.png)           |
  
  <br>

  | (sun behind:1.2), strong sun shine, man | (sun behind:1.2), strong sun shine, woman |
  | :-------------------------------------: | :---------------------------------------: |
  |                          ![sun_behind_man_small](https://user-images.githubusercontent.com/60317828/231047908-0114d0c5-a992-4e1d-a943-bb93e30bd6b3.png)               |                  ![sun_behind_woman_small](https://user-images.githubusercontent.com/60317828/231047920-2d904852-77ae-4ec8-90ca-b1e04c8a98bf.png)                         |

  <br>

  | in the night, dark light, (very dark scene:1.2), man | in the night, dark light, (very dark scene:1.2), woman |
  | :--------------------------------------------------: | :----------------------------------------------------: |
  |                         ![dark_man_small](https://user-images.githubusercontent.com/60317828/231047941-7a2f19ac-2cb7-4efa-b8b7-5aa735947867.png)                             |                                ![dark_woman_small](https://user-images.githubusercontent.com/60317828/231047949-b6246475-703b-43bf-b040-f2e3828b2338.png)                        |

- <details><summary> Large pose </summary><p><div align="center">

  - Left & right

  | side view, man | side view, woman |
  | :------------: | :--------------: |
  |       ![sideview_man_small](https://user-images.githubusercontent.com/60317828/231048001-a00fc301-658a-4eee-aeb8-95b4974beb81.png)         |        ![sideview_woman_small](https://user-images.githubusercontent.com/60317828/231047986-f455ea7e-4947-4034-a939-123705407819.png)          |

  - Up

  | (looking up:1.3), man | (looking up:1.3), woman |
  | :-------------------: | :---------------------: |
  |               ![up_man_small](https://user-images.githubusercontent.com/60317828/231048047-b0b15f91-c66a-4cb8-8fa6-564e45249186.png)        |                 ![up_woman_small](https://user-images.githubusercontent.com/60317828/231048033-f25194e4-0dc0-49c6-a371-d34048c377db.png)        |

- <details><summary> Hair </summary><p><div align="center">

  | blond hair | blond hair |
  | :--------: | :--------: |
  |            |            |

  <br>
  
  | (Bangs:1.2) | (Bangs:1.2) |
  | :---------: | :---------: |
  |             |             |
  
  <br>

  | Bald | Bald |
  | :--: | :--: |
  |      |      |

- <details><summary> Others </summary><p><div align="center">

  | clothes | clothes |
  | :-----: | :-----: |
  |         |         |
  
  <br>

  | mustache,sideburns,goatee,front view | mustache,sideburns,goatee,front view |
  | :----------------------------------: | :----------------------------------: |
  |                                      |                                      |
  
  <br>

  | (talking loudly:1.4),smile,neutral | (talking loudly:1.4),smile,neutral |
  | :--------------------------------: | :--------------------------------: |
  |                                    |                                    |
  
  <br>

  | (sleepy,close eyes:1.4) | (sleepy,close eyes:1.4) |
  | :---------------------: | :---------------------: |
  |                         |                         |
  


## Acknowledgement

Thanks the creator of the model for his brilliant work and also thanks his reference models. 

 **[Realistic_Vision_V2.0:1](https://civitai.com/models/4201/realistic-vision-v20)** by **[SG_161222](https://civitai.com/user/SG_161222)**

## Future Work

- I will use this fake faces to launch a program of facial landmark detection. In my plan, the program supports 240 points and keeps a good capacity under complex scene (like large pose, occlusion, extreme expression…). Also, it supports both large model and tiny model (pth & onnx), for mobile using.
- keep expanding the dataset.

## Citation

```
@repo{2023agfd25k,
    title={A Generated Face Dataset: AGFD-25K},
    author={Robin_WZQ},
    howpublished = {\url{https://github.com/Robin-WZQ/AGFD-30K}},
    year={2023}
}
```
