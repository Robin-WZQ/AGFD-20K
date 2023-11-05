# A Generated Face Dataset: AGFD-20K

<div align=center>
    <img src=https://user-images.githubusercontent.com/60317828/232225866-1b87ce2c-c83b-4866-a4ea-2e7ab6bb5d93.png width="700"/>
</div>

Can we use generated human faces to train a model? If the model can generate faces that are realistic enough, how can we use it to generate faces we want? What is the mapping between prompt and vary human faces?

Besides, many times we need to construct a good test dataset to test the robustness of the trained model. But selecting images carefully from searching engines is laborious and also facing the problem of cleaning (due to the low quality of the data like unrelated, low-resolution, unbalanced, etc.). How the diffusion model can help us solve this problem?

What's more, fake faces detection is also a essential topic of AI safety. We can generate target faces directly through deep generative models, but just as important is how do we detect them? For example, our logo is A FAKE FACE!

In the past 3 years, we have seen the explosive growth of the **Diffusion Model**, it now can generate brilliant pictures according to user's prompts. Here I test the diffusion model in the capacity of generating realistic human faces. And purposes of this project are the following two points:

1. Construct a not bad **fake** faces dataset;
2. Use these data to do something interesting. I don't know if it helps anyone, but it works for me 🤣🤣🤣 

The principles I followed in generating faces are:

- Realistic (use **[Realistic_Vision_V2.0:1](https://civitai.com/models/4201/realistic-vision-v20)** by **[SG_161222](https://civitai.com/user/SG_161222)**)
- High-resolution (the resolution of all images are 512*512)
- Vary & Balanced (support vary faces and keep good data distribution)

Here is the generated face data and corresponding descriptions:

|  Attribute   |  Specific Features   | Male | Female |                        Special Prompt                        |
| :----------: | :------------------: | :--: | :----: | :----------------------------------------------------------: |
|     Age      |     Child (0-5)      | 300  |  300   |                        1 y.o., 3 y.o.                        |
|              |   Teenager (5-18)    | 600  |  600   |                       8 y.o., 15 y.o.                        |
|              | Young people (18-40) | 300  |  300   |                       25 y.o., 35 y.o.                       |
|              | Middle aged (40-60)  | 300  |  300   |                       45 y.o., 55 y.o.                       |
|              |   Old people (60+)   | 600  |  600   |               60,80,100 y.o., Grandma，Grandpa               |
|   Emotion    |        Smile         | 600  |  600   |                      smiling, laughing                       |
|              |        Angry         | 600  |  600   |               Angry, pissed-off face, yelling                |
|  Occlusion   |     Only glasses     | 600  |  600   |     glasses,sunglasses,swimming goggles,skiing goggles,      |
|              |      Only mask       | 300  |  300   |                  (masked:1.2), antigas mask                  |
|              |     Only make up     | 300  |  300   | highly make up, eyeshadow,heavy black eyeliner, joker, Halloween makeup |
|              |      Only hands      | 300  |  300   |     put Hand in front of face,put Hand in front of hair      |
|              |       Complex        | 300  |  300   | glasses，(masked:1.2),Halloween makeup，put Hand in front of face,put Hand in front of hair |
| Illumination |     Under water      | 300  |  300   |                         under water                          |
|              |     Strong light     | 300  |  300   |              (sun behind:1.2), strong sun shine              |
|              |         Dark         | 300  |  300   |       in the night, dark light, (very dark scene:1.2)        |
|  Large pose  |     Left & right     | 2000 |  2000  |                          side view                           |
|              |          Up          | 300  |  300   |                       (looking up:1.3)                       |
|     Hair     |        Blond         | 300  |  300   |                          blond hair                          |
|              |        Bangs         | 300  |  300   |                         (Bangs:1.2)                          |
|              |         Bald         | 300  |  300   |                             Bald                             |
|    Others    |       Moustache       | 300  |   -    |             moustache,sideburns,goatee,front view             |
|              |      Open Mouse      | 600  |  600   |              (talking loudly:1.4),smile,neutral              |
|              |      Close Eyes      | 600  |  600   |                   (sleepy,close eyes:1.4)                    |
|     ALL      |        Origin        | 20K  |  20K   |                              -                               |

All the pictures can be downloaded at 

Link1: [Baidu Disk](https://pan.baidu.com/s/1Nz7oDuavQnmp4gVQa1AmoQ) [extract code: tqxd]. 

Link2: [terabox](https://terabox.com/s/1PJkbnrQGyfjPwzPY8VBPCQ)

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

- <details><summary> 👨‍👩‍👧‍👦 Age </summary><p><div align="center">

  |                     1 y.o., 3 y.o., boy                      |                     1 y.o., 3 y.o., girl                     |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![young_child_small](https://user-images.githubusercontent.com/60317828/230921787-eae427f4-2655-4fc8-9195-420186f6fe04.png) | ![young_child_girl_small](https://user-images.githubusercontent.com/60317828/230921807-59d9291f-ea97-415f-a3a7-6648bab9f638.png) |

  <br>
  
  |                     8 y.o., 15 y.o., boy                     |                    8 y.o., 15 y.o., girl                     |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![teenager_man_small](https://user-images.githubusercontent.com/60317828/230921966-818d3088-4428-4e35-816d-5e0734dce315.png) | ![teenager_woman_small](https://user-images.githubusercontent.com/60317828/230921910-37680c5c-a2be-4cd1-b256-661e787f270e.png) |

  <br>
  
  |                    25 y.o., 35 y.o., man                     |                   25 y.o., 35 y.o., woman                    |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![young_adult_man_small](https://user-images.githubusercontent.com/60317828/230922592-21961c2c-faa1-42ae-906c-4fa06090dd55.png) | ![young_adult_woman_small](https://user-images.githubusercontent.com/60317828/230925134-f457837e-77a5-44bf-b0b7-a6a0612680a5.png) |

  <br>
  
  |                    45 y.o., 55 y.o., man                     |                   45 y.o., 55 y.o., woman                    |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![old_adult_man_small](https://user-images.githubusercontent.com/60317828/230922649-00d3c796-bc83-42b1-8fc2-e19b8e77b56e.png) | ![old_adult_woman_small](https://user-images.githubusercontent.com/60317828/230922504-95a1249d-e5f2-4a9c-bcd5-6762beed53ed.png) |

  <br>
  
  |                 60,80,100 y.o., man, grandpa                 |               60,80,100 y.o., woman,  grandma                |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![Old_man_small](https://user-images.githubusercontent.com/60317828/230925226-7c507214-f8d3-4fb7-8dac-a12cd32082a8.png) | ![old_woman_small](https://user-images.githubusercontent.com/60317828/231047264-152b8f4e-1182-4384-ad21-dae56cabe6ca.png) |

- <details><summary> 😃 Emotion </summary><p><div align="center">

  |                    smiling, laughing, man                    |                   smiling, laughing, woman                   |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![smile_man_small](https://user-images.githubusercontent.com/60317828/230925316-a333694d-a954-4af7-bc4b-8c82235658e2.png) | ![smile_woman_small](https://user-images.githubusercontent.com/60317828/230925301-196ca6ff-ab27-49f2-bf5b-2fc6d17dc875.png) |

  <br>

  |             Angry, pissed-off face, yelling, man             |            Angry, pissed-off face, yelling, woman            |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![angry_man png_small](https://user-images.githubusercontent.com/60317828/230921290-1a560151-1ae1-4344-9b83-88a31d202d6c.png) | ![angry_woman_small](https://user-images.githubusercontent.com/60317828/231047315-a88d0635-98d5-4efa-9a67-8547138bbdeb.png) |

- <details><summary> 🥸 Occlusion </summary><p><div align="center">

  |   glasses,sunglasses,swimming goggles,skiing goggles, man    |  glasses,sunglasses,swimming goggles,skiing goggles, woman   |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![glasses_man_small](https://user-images.githubusercontent.com/60317828/231047342-d98dcbbb-9a3e-4fac-816b-8e3fc894e559.png) | ![glasses_Woman_small](https://user-images.githubusercontent.com/60317828/231047362-f9faff25-197d-4ccc-80d3-b58b9034403e.png) |

  <br>

  |               (masked:1.2), antigas mask, man                |              (masked:1.2), antigas mask, woman               |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![mask_man_small](https://user-images.githubusercontent.com/60317828/231047415-c48c7579-234a-4256-9222-ae7a5e045b3b.png) | ![mask_woman_small](https://user-images.githubusercontent.com/60317828/231047504-8fc9d908-7a04-4432-a5c0-83de6a547255.png) |

  <br>

  | highly make up, eyeshadow,heavy black eyeliner, joker, Halloween makeup, man | highly make up, eyeshadow,heavy black eyeliner, joker, Halloween makeup, woman |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![makeup_man_small](https://user-images.githubusercontent.com/60317828/231047659-95262578-e0f1-417a-98cf-bb1d7bc988b0.png) | ![makeup_woman_small](https://user-images.githubusercontent.com/60317828/231047639-04f0e031-dbb9-469e-ad79-a52f3c84ab48.png) |

  <br>

  |  put Hand in front of face, put Hand in front of hair, man   | put Hand in front of face, put Hand in front of hair, woman  |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![hand_man_small](https://user-images.githubusercontent.com/60317828/231047682-3593e531-043a-4a41-88e7-c7bbce34fd82.png) | ![hand_Woman_small](https://user-images.githubusercontent.com/60317828/231047697-6113d99c-462b-47ca-bbec-fa353cb01259.png) |

  <br>

  | glasses，(masked:1.2), Halloween makeup，put Hand in front of face, put Hand in front of hair, man | glasses，(masked:1.2), Halloween makeup，put Hand in front of face, put Hand in front of hair, woman |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![complex_man_small](https://user-images.githubusercontent.com/60317828/231047722-b0089d11-b441-4ec0-9df0-58b12abaad7d.png) | ![complex_woman_small](https://user-images.githubusercontent.com/60317828/231047732-c593a4a8-5ed1-4bd9-9a0a-b57350948607.png) |

- <details><summary> 🔆 Illumination </summary><p><div align="center">

  |                       under water, man                       |                      under water, woman                      |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![under_water_man_small](https://user-images.githubusercontent.com/60317828/231047856-2ec1c35e-e748-4e7b-a0cb-9dcedce40d01.png) | ![under_water_woman_small](https://user-images.githubusercontent.com/60317828/231047867-1f2a1644-5f2c-4509-85e6-510e829d0967.png) |
  
  <br>

  |           (sun behind:1.2), strong sun shine, man            |          (sun behind:1.2), strong sun shine, woman           |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![sun_behind_man_small](https://user-images.githubusercontent.com/60317828/231047908-0114d0c5-a992-4e1d-a943-bb93e30bd6b3.png) | ![sun_behind_woman_small](https://user-images.githubusercontent.com/60317828/231047920-2d904852-77ae-4ec8-90ca-b1e04c8a98bf.png) |

  <br>

  |     in the night, dark light, (very dark scene:1.2), man     |    in the night, dark light, (very dark scene:1.2), woman    |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![dark_man_small](https://user-images.githubusercontent.com/60317828/231047941-7a2f19ac-2cb7-4efa-b8b7-5aa735947867.png) | ![dark_woman_small](https://user-images.githubusercontent.com/60317828/231047949-b6246475-703b-43bf-b040-f2e3828b2338.png) |

- <details><summary> 🔭 Large pose </summary><p><div align="center">

  |                        side view, man                        |                       side view, woman                       |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![sideview_man_small](https://user-images.githubusercontent.com/60317828/231048001-a00fc301-658a-4eee-aeb8-95b4974beb81.png) | ![sideview_woman_small](https://user-images.githubusercontent.com/60317828/231047986-f455ea7e-4947-4034-a939-123705407819.png) |

  <br>

  |                    (looking up:1.3), man                     |                   (looking up:1.3), woman                    |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![up_man_small](https://user-images.githubusercontent.com/60317828/231048047-b0b15f91-c66a-4cb8-8fa6-564e45249186.png) | ![up_woman_small](https://user-images.githubusercontent.com/60317828/231048033-f25194e4-0dc0-49c6-a371-d34048c377db.png) |

- <details><summary> 🦱 Hair </summary><p><div align="center">

  |                       blond hair, man                        |                      blond hair, woman                       |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![blond_man_small](https://user-images.githubusercontent.com/60317828/231630521-1c0ba435-3465-4d92-a31f-8c56315bbed5.png) | ![blond_woman_small](https://user-images.githubusercontent.com/60317828/231630529-9c97dbd6-4e1b-4025-b43c-9bc55c406b06.png) |

  <br>
  
  |                       (Bangs:1.2), man                       |                      (Bangs:1.2), woman                      |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![bang_man_small](https://user-images.githubusercontent.com/60317828/231630561-6bd1e8e2-3fe1-4319-bf37-74c987b00c5b.png) | ![bang_woman_small](https://user-images.githubusercontent.com/60317828/231630568-8a7e4aea-5eba-47c7-9f14-7ab7c7276d0b.png) |
  
  <br>

  |                          Bald, man                           |                         Bald, woman                          |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![bald_man_small](https://user-images.githubusercontent.com/60317828/231630591-3532cf89-6314-4cb9-8d3d-ec28fbe70d17.png) | ![bald_woman_small](https://user-images.githubusercontent.com/60317828/231630607-c46726f9-88e8-4d7b-8c6e-0811ee0c1c17.png) |

- <details><summary> 🧑‍💻 Others </summary><p><div align="center">

  |          moustache,sideburns,goatee,front view, man           | moustache,sideburns,goatee,front view, woman |
  | :----------------------------------------------------------: | :-----------------------------------------: |
  | ![mustache_man_small](https://user-images.githubusercontent.com/60317828/231630899-dfa1df68-78d2-4608-8ebb-82f048e10777.png) |              cannot generate 💔              |
  
  <br>

  |           (talking loudly:1.4),smile,neutral, man            |          (talking loudly:1.4),smile,neutral, woman           |
  | :----------------------------------------------------------: | :----------------------------------------------------------: |
  | ![oen_mouse_man_small](https://user-images.githubusercontent.com/60317828/231630953-ce42adc8-37d2-4c20-a721-3e5d153e77e9.png) | ![open_mouse_woman_small](https://user-images.githubusercontent.com/60317828/231631009-3dc1f7ea-02eb-4921-ace7-86d98659c00c.png) |
  
  <br>

  |                 (sleepy,close eyes:1.4), man                 | (sleepy,close eyes:1.4), woman |
  | :----------------------------------------------------------: | :----------------------------: |
  | ![close_eye_man_small](https://user-images.githubusercontent.com/60317828/231631079-ab1dedbc-9af5-44df-ab8e-074a97de42bd.png) |              ![close_eyes_woman_small](https://user-images.githubusercontent.com/60317828/232202641-c2ef73dc-4ebf-4d61-825a-8080c438b91b.png)                  |

## Acknowledgement

Thanks the creator of the model for his brilliant work and also thanks his reference models. 

 **[Realistic_Vision_V2.0:1](https://civitai.com/models/4201/realistic-vision-v20)** by **[SG_161222](https://civitai.com/user/SG_161222)**

## Future Work

- Although the realistic ability of this version model to generate pictures is enhanced, **the generalization is weakened**. As reported in [MidJourney-Styles-and-Keywords](https://github.com/willwulfken/MidJourney-Styles-and-Keywords-Reference/blob/main/Pages/MJ_V5/Style_Pages/V5_Alpha_1.md),  the Mid-v5 has a better ability to process finer facial details. I will keep focusing on the generated model and use better model to generated more controllable human faces. 

## Citation

```
@repo{2023agfd20k,
    title={A Generated Face Dataset: AGFD-20K},
    author={Robin_WZQ},
    howpublished = {\url{https://github.com/Robin-WZQ/AGFD-20K}},
    year={2023}
}
```
