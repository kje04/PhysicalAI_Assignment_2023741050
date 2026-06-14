# PhysicalAI Assignment Report

## 1. Objective

The objective of this assignment was to generate a robot manipulation dataset in MuJoCo and fine-tune OpenVLA using the generated demonstrations.

## 2. Dataset Generation

A color-conditioned cylinder grasping task was used in the MuJoCo environment.

Four target colors were included:

* red
* blue
* green
* yellow

A total of 400 successful episodes were generated.

Dataset split:

* Train: 360 episodes
* Validation: 40 episodes

The dataset was converted into RLDS format and then built as a TFDS dataset named `raccoon_pick_place`.

## 3. OpenVLA Fine-tuning

OpenVLA-7B was fine-tuned using LoRA.

Training configuration:

* LoRA Rank: 8
* Batch Size: 1
* Gradient Accumulation Steps: 16
* Learning Rate: 5e-4
* Training Steps: 1000

The training was performed on an NVIDIA A100 GPU server.

## 4. Results

The following tasks were completed successfully:

* Dataset generation
* RLDS conversion
* TFDS build
* Dataset verification
* OpenVLA fine-tuning

The model checkpoint was successfully saved after 1000 training steps.

## 5. Conclusion

This assignment demonstrated the complete OpenVLA training pipeline, including dataset generation, dataset conversion, verification, and fine-tuning using a custom MuJoCo environment.
