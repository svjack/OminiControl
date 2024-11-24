# OminiControl


<img src='./assets/demo/demo_this_is_omini_control.jpg' width='100%' />
<br>

<a href="https://arxiv.org/abs/2411.xxxx">
  <img src="https://img.shields.io/badge/ariXv-2411.xxxx-A42C25.svg" alt="arXiv">
</a>
<a href="https://huggingface.co/Yuanshi/OminiControl">
  <img src="https://img.shields.io/badge/🤗_HuggingFace-Model-ffbd45.svg" alt="HuggingFace">
</a>

> **OminiControl: Minimal and Universal Control for Diffuison Transformer**
> <br>
> Zhenxiong Tan, 
> [Songhua Liu](http://121.37.94.87/), 
> [Xingyi Yang](https://adamdad.github.io/), 
> Qiaochu Xue, 
> and 
> [Xinchao Wang](https://sites.google.com/site/sitexinchaowang/)
> <br>
> [Learning and Vision Lab](http://lv-nus.org/), National University of Singapore
> <br>


## Features

OmniControl is a minimal yet powerful universal control framework for Diffusion Transformer models like [FLUX](https://github.com/black-forest-labs/flux).

* **Universal Control 🌐**: Supports both subject-driven signals (like [IP-Adapter](https://github.com/tencent-ailab/IP-Adapter)) and spatial control (like [ControlNet](https://github.com/lllyasviel/ControlNet)).

* **Minimal Design 🚀**: Injects control signals while preserving original model structure. Only introduces 0.1% additional parameters to the base model.

## Usage examples
1. Subject-driven generation: `examples/subject.ipynb`
2. In-painting: `examples/inpainting.ipynb`
3. Canny edge to image, depth to image, colorization, deblurring: `examples/spatial.ipynb`

## Generated samples
### Subject-driven generation
**Demos** (Left: condition image; Right: generated image)

<div float="left">
  <img src='./assets/demo/oranges_omini.jpg' width='48%'/>
  <img src='./assets/demo/rc_car_omini.jpg' width='48%' />
  <img src='./assets/demo/clock_omini.jpg' width='48%' />
  <img src='./assets/demo/shirt_omini.jpg' width='48%' />
</div>

<details>
<summary>Text Prompts</summary>

- Prompt1: *A close up view of this item. It is placed on a wooden table. The background is a dark room, the TV is on, and the screen is showing a cooking show. With text on the screen that reads 'Omini Control!.'*
- Prompt2: *A film style shot. On the moon, this item drives across the moon surface. A flag on it reads 'Omini'. The background is that Earth looms large in the foreground.*
- Prompt3: *In a Bauhaus style room, this item is placed on a shiny glass table, with a vase of flowers next to it. In the afternoon sun, the shadows of the blinds are cast on the wall.*
- Prompt4: *In a Bauhaus style room, this item is placed on a shiny glass table, with a vase of flowers next to it. In the afternoon sun, the shadows of the blinds are cast on the wall.*
</details>

### Spaitally aligned control
1. **Image Inpainting** (Left: original image; Center: masked image; Right: filled image)
  - Prompt: *The Mona Lisa is wearing a white VR headset with 'Omini' written on it.*
    </br>
    <img src='./assets/demo/monalisa_omini.jpg' width='700px' />
  - Prompt: *A yellow book with the word 'OMINI' in large font on the cover. The text 'for FLUX' appears at the bottom.*
    </br>
    <img src='./assets/demo/book_omini.jpg' width='700px' />
2. **Other spatially aligned tasks**  (Canny edge to image, depth to image, colorization, deblurring) 
    </br>
    <div float="left">
      <img src='./assets/demo/room_corner_canny.jpg' width='48%'/>
      <img src='./assets/demo/room_corner_depth.jpg' width='48%' />
      <img src='./assets/demo/room_corner_coloring.jpg' width='48%' />
      <img src='./assets/demo/room_corner_deblurring.jpg' width='48%' />
    </div>
   



<!-- ## Models
| Model          | Base model | Tasks                                                                    |                                                       |
| -------------- | ---------- | ------------------------------------------------------------------------ | ----------------------------------------------------- |
| `experimental` | FLUX.1     | Canny edge to image, depth to image, colorization, deblurring, mask fill | [🤗](https://huggingface.co/Yuanshi/OminiControl-FLUX) | --> |

## Citation
```
@article{
  tan2024omini,
  title={OminiControl: Minimal and Universal Control for Diffusion Transformer},
  author={Zhenxiong Tan, Songhua Liu, Xingyi Yang, Qiaochu Xue, and Xinchao Wang},
  journal={arXiv preprint arXiv:2411.xxxx},
  year={2024}
}
```