# Image Generation with GANs

A learning project that builds Generative Adversarial Networks (GANs) in PyTorch to generate images. It has a basic GAN trained on CIFAR-10 and a DCGAN meant for face images such as CelebA.

## Scripts

| File | What it does |
|---|---|
| `Image Generation with GANs.py` | GAN trained on CIFAR-10 (downloaded automatically by torchvision). Trains for 50 epochs, saving checkpoints, or loads `generator.pth` / `discriminator.pth` if they exist. Then saves a grid of generated images to `generated_images.png`. |
| `image generation using DCGAN.py` | DCGAN that trains on a folder of your own images resized to 64×64 (written for the CelebA face dataset). Saves sample images to `output/` after each epoch. |
| `image generation.py` | Loads a trained `generator.pth` and saves a grid of new images |
| `version_check.py` | Small helper that lists the images found in a dataset folder |

## Tech

Python 3, PyTorch, torchvision, Pillow, Matplotlib

## How to run

```bash
pip install torch torchvision pillow matplotlib
python "Image Generation with GANs.py"
```

For the DCGAN, download a face dataset such as [CelebA](https://mmlab.ie.cuhk.edu.hk/projects/CelebA.html) and put its images in a folder called `img_celeba` in the directory you run the script from, or change `root_dir` in `image generation using DCGAN.py` to point somewhere else. Training is much faster on a GPU (CUDA is used if available).

## Results

Trained model weights and generated images are not included in this repository. Run the scripts to produce them.
