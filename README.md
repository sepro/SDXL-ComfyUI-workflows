# SDXL-ComfyUI-workflows
A collection of my own ComfyUI workflows for working with SDXL. These are all based on [Sytan SDXL ComfyUI](https://github.com/SytanSD/Sytan-SDXL-ComfyUI), so all credits for the base implementation go to them. Have a look at this repository as these workflows included here are more advanced.

## Workflow for photographs

For photographs the refiner can be a huge boon. Here it is applied twice once as part of the initial image generation, once after the upscaling step. This helps creating crips images with a lot of detail. This workflow includes the Offset Noise Lora and the option to include an additional Lora (make sure to set the weights higher than zero to use this option) and an OpenPose ControlNet is included. 

![an example of four androids generated using this workflow](./images/photography_examples.jpeg)

Positive prompt used:
```
cinematic closeup photo of a futuristic android made from metal and glass. Neon lights, hdr, f1.8, intricate details, nikon, canon,
```
Negative prompt used:
```
noise, grit, dull, washed out, low contrast, blurry, deep-fried, hazy, malformed, warped, deformed, grayscale, illustration, painting
```

**Workflow:** [./workflow/photography_workflow.json](./workflow/photography_workflow.json)

## Workflow for artistic/painterly styles

While for photographs the refiner helps, the opposite seems true when an artistic style is desired. In this workflow the refiner has been removed and CLIP skip has been added. 

**Workflow:** [./workflow/painterly_style_workflow.json](./workflow/painterly_style_workflow.json)