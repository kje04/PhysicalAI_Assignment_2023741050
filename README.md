# PhysicalAI Assignment 2023741050

## Environment

* Ubuntu 20.04
* Python 3.8.10
* CUDA 12.2
* GPU: NVIDIA A100 80GB
* Model: OpenVLA-7B

## Dataset

The original task was color-conditioned cylinder grasping.

I generated MuJoCo demonstration data for four target colors:

* red
* blue
* green
* yellow

Generated dataset:

* Total episodes: 400
* Train split: 360
* Validation split: 40
* Dataset format: RLDS / TFDS
* Dataset name: raccoon_pick_place

## Training Pipeline

The generated demonstrations were converted into RLDS format and then built as a TFDS dataset for OpenVLA training.

Main steps:

1. MuJoCo demonstration generation
2. RLDS conversion
3. TFDS build
4. Dataset verification
5. OpenVLA fine-tuning

## Fine-tuning

Fine-tuning was performed using LoRA.

Settings:

* LoRA rank: 8
* Batch size: 1
* Gradient accumulation steps: 16
* Learning rate: 5e-4
* Max steps: 1000

Checkpoint path:

/data/2023741050/openvla-runs/openvla-7b+raccoon_pick_place+b16+lr-0.0005+lora-r8+dropout-0.0--raccoon-eef-1000step--image_aug

## Results

* Dataset generation completed successfully
* RLDS conversion completed successfully
* TFDS build completed successfully
* Dataset transform test passed
* OpenVLA LoRA fine-tuning completed for 1000 steps
* Model checkpoint saved successfully

## Repository Structure

* screenshots/ : result screenshots
* logs/ : training logs
* modified_files/ : modified source files
* report/ : assignment report
