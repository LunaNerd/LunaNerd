## Hi there 👋

Welcome to my github profile. Here I showcase what I've been working on lately and my past projects.

### Intro:

My name is Luna and I'm a IT-student currently looking for a job while finishing my masters in Information Engineering Technology (dutch: Industrieel ingenieur informatica).  
My main focus is currently on my master thesis project where I'm creating synthetic data to train an object detection model to detect flower species in drone images of grasslands. Past projects include: 
- An old computer vision group project,
- Google FooBar and Advent Of Code
- ... and maybe some more projects if and when I get around to putting them online

Feel free to poke around. Some of this code is a bit older and might not reflect what I've learned over the years.

# MasterThesis 🪻🌺🏵️ 🚁📷
> Subjects: Computer Vision, synthetic data, machine learning, object detection  
> Used technologies:
> - Python
> - OpenCV
> - Pillow
> - Fiftyone
> - Wandb
> - YOLOv8
> - GroundingDINO
> - Meta's SegmentAnything

#### Short description
The goal of this master thesis is to create synthetic data to improve an existing annotated dataset or even replace the annotated dataset all together. The dataset this is being tested on is an object detection dataset of drone images made from grasslands. The annotated objects are flowers. The synthetic data is being created by downloading flower images from citizen science projects like Pl@ntNET and obsidentify. This project is not yet where I want it to be so more updates will follow as I improve the project.

Challenges in this project include:
- The flowers being small objects making it more difficult to avoid pasting artifacts
- High interclass simularity between the flower groups (some flower groups look alike a lot) making this a challenging dataset

| The annotated drone images I'm trying to imitate |  The various steps of the datapipeline |
| ------------------------------------------------ | -------------------------------------- |
| ![image](https://github.com/user-attachments/assets/03ac51b7-77d4-4e91-931e-c16dc5ec9ed5) |   ![image](https://github.com/user-attachments/assets/79469eda-a959-4a9b-9c91-057626afc98d) |

The codebase for my mastersthesis is spread across 3 repos:

1. ([link coming soon]()): A repository responsible for the downloading of flowers images from GBIF, creating cutouts and creating json files with the correct ratios of every flower species so every flower group is equally represented. EDA on the drone dataset also happens in this dataset.
2. [synthetic-dataset-generation](https://github.com/LunaNerd/synthetic-dataset-generation): A heavily modified fork of an existing implementation for synthetic data creation. Here GBIF cutouts get composited onto background images according to a ever growing list of config values to minimize the domain shift.
3. ([link coming soon]()): An evaluation repository. Here code can be found to train a YOLOv8 model on different ratios of real and synthetic data to test how effective the synthetic data is for this purpose. Various visualization scrips can be found here aswell to visually inspect the synthetic data and compare it to the real drone images.

This project is not done yet so expect some more exciting results soon as I further improve the pipeline.

#### Results

Currently, synthetic data is only partially capable of replacing a real dataset when training it to detect a single flower group (but still including all the other flower groups as distractors). I expect this the synthetic data to get better in the upcoming weeks.

| Downloaded and segmented GBIF images             | An example synthetic image | Current Training results on a single flower group with all 20 other groups as distractors |
| ------------------------------------------------ | ------                     | --------------------------------------                                                     |
| ![image](https://github.com/user-attachments/assets/793e69de-e7e2-400d-b76b-18b103e3f35d) | ![image](https://github.com/user-attachments/assets/aeb7965a-e042-44f7-849f-c08512e46270) | ![image](https://github.com/user-attachments/assets/21db1508-9269-4948-af1f-48912e8ebbce)  <ul><li>Orange (a model trained on synthetic data only)</li><li>Pink (a model trained on real data only)</li><li>Purple (a model trained on a mix of real and synthetic data)</li></ul>| 

# Computer Vision group project 🌳

> Subjects: computer vision, machine learning, deep learning, Structure-from-Motion (SfM) and Multi-View Stereo (MVS)
> Used technologies:
> - Python
> - COLMAP
> - OpenCV

[This repository](https://github.com/LunaNerd/computer_vision_tree_detection) got used for a group project of the ComputerVision course.  

The goal of this project is to identify, localize and measure the with of trees on a video made from a scooter. Us (the students) were free to choose our approach and chose one using: 

- PercepTreeV1​ (A Mask R-CNN model trained on synthetische data)
- COLMAP ( Structure-from-Motion (SfM) and Multi-View Stereo (MVS) CLI/GUI software)

| Description| Result |
|-------------|------|
| GIF clip of the output of our model | ![output_video_eastbound_200_frames-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/a4c9fab2-ec98-44af-b06a-416a91c99c18) |

# Coding challenges: Google Foobar and Advent Of Code 🎄
> Used technologies:
> - Java

Some of my solutions to coding riddles can be found in these two repositories. Looking forward to [AOC2025](https://adventofcode.com/).

- [Google FooBar](https://github.com/LunaNerd/GoogleFooBar)
- [Advent of Code](https://github.com/LunaNerd/AoC-2021)

<!--
**LunaNerd/LunaNerd** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
