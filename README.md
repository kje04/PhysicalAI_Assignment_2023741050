# PhysicalAI Assignment

## Environment

- Ubuntu 20.04
- Python 3.8
- CUDA 12.2
- NVIDIA A100 80GB

## Dataset

- 400 Episodes Generated
- Train: 360
- Validation: 40

## Dataset Extension

Added multiple language instructions.

Examples:

- grasp the red cylinder
- pick up the red cylinder
- grab the red cylinder
- lift the red cylinder

## Code Improvements

1. Inference time logging
2. Action logging

## Fine-tuning

- OpenVLA-7B
- LoRA Rank: 8
- Batch Size: 1
- Learning Rate: 5e-4
- Max Steps: 1000

## Results

- Dataset generation success
- TFDS conversion success
- Fine-tuning success (in progress)
- Inference pending

## Screenshots

See screenshots directory.
