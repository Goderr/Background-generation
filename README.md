
# Image Segmentation and Background Generation

In this project I have used the SAM model form META AI to segment the obejcts in the images(which can be done by clicking on the objects), then according to a given prompt, using stable diffusion, a Background can be generated for the objects in the images.


## Model Checkpoints

The ```default``` or ```vit_h``` checkpoints have been used for the SAM model. The link is given below.

```vit_h```: https://dl.fbaipublicfiles.com/segment_anything/sam_vit_h_4b8939.pth

SAM model provides two more checkpoints. Following are the links

```vit_l```: https://dl.fbaipublicfiles.com/segment_anything/sam_vit_l_0b3195.pth

```vit_b```: https://dl.fbaipublicfiles.com/segment_anything/sam_vit_b_01ec64.pth

To use the above two checkpoints instead of the default checkpoints edit the following code snippet in the code.

```bash
  sam = sam_model_registry["<model_type>"](checkpoint="<path/to/checkpoint>")
```
## Technology Used

The follwing technologies were used:

1. Segment Anything Model by META - for images segmentation

2. HugginFace Stable Diffusion - For generating the background

3. Gradio - To create an interactive UI


