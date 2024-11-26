# Research Introduction

🪧

This project is part of my undergraduate thesis, where I propose a novel methodology combining Transformer and BiLSTM models to accurately predict Key and Chord information from MIDI Note data. The predicted information is then used to transform the data into the REMI format. This approach achieves higher accuracy compared to existing MIDI-to-REMI conversion processes based on chroma vectors. The POP909 dataset was utilized, and 12-key augmentation was applied to address dataset bias. The model achieved 86% accuracy in key prediction and 93% accuracy in chord prediction. By integrating the results into the REMI format, this project aims to enhance the usability of MIDI data.

You can check my project paper at : (... will be linked later ...)

---

# Research Goals

🎯

1. Propose a model methodology for predicting key and chord from melodies.
2. Develop a higher-quality MIDI-to-REMI conversion process using the predicted key and chord information.
3. Train a prototype model to validate the proposed methodology.

---

# Research Contributions

🏅

1. Proposing a multi-input model methodology for predicting key and chord from melodies.
2. Designing a more robust MIDI-to-REMI conversion process leveraging Key and Chord information.
3. Training and evaluating a prototype model to validate the methodology.
4. Providing foundational resources for future research and commercialization.

---

# Research Limitations and Improvements

🚫

This project has the following limitations:

1. **Dataset Limitations**: The project exclusively uses the POP909 dataset, which limits generalization to other genres such as classical and jazz. Future work could expand the scope by incorporating additional datasets.
2. **Modulation Issues**: The current model may overlook frequent modulations in certain songs as it focuses on chord prediction. Additional algorithms or techniques for key prediction can address this limitation.
3. **64-Bar Limitation**: Due to resource constraints, the prototype model processes sequences up to 64 bars. With more time and GPU resources, the model and dataset preprocessing can be extended to support longer time steps.
4. **Lack of Substitute Chord Support**: The model does not allow substitute chords for the same melody, limiting harmonic diversity. This can be addressed in future research.
5. **REMI Compatibility Issues**: While largely compatible, the generated REMI data has some minor differences from the original REMI format. Adjustments are needed for full compatibility.
6. **Prototype Status**: The project prioritizes validating the methodology over optimizing model performance, and it is not yet at a production-ready level. I was a time-constrained undergraduate student. 🫠

---

# Requirements

⚖️

This project was implemented in a Jupyter Notebook environment using Python 3.9.19. To avoid conflicts, it is recommended to use a virtual environment.

The following libraries were used:

- **NumPy**: 1.23.5
- **Pandas**: 2.0.3
- **Matplotlib**: 3.7.2
- **Seaborn**: 0.13.2
- **Scikit-learn**: 1.5.1
- **PyTorch**: 2.4.1+cu124
- **miditoolkit**: 1.0.1

---

# Dataset

📑

The [POP909 Dataset](https://github.com/music-x-lab/POP909-Dataset) was used in this project. Special thanks to Ziyu Wang*, Ke Chen*, Junyan Jiang, Yiyi Zhang, Maoran Xu, Shuqi Dai, Guxian Bin, and Gus Xia for providing this excellent dataset under the [Creative Commons Attribution 4.0 License](https://creativecommons.org/licenses/by/4.0/).

The raw MIDI dataset can be downloaded from the repository linked above. Preprocessed numpy-format datasets used in this project can be found in the `data` folder.

---

# Repository Structure

🌲

- **README**: Project introduction
- **data**: Information on the dataset and preprocessed numpy-format datasets.
- **model checkpoint**: Pretrained model weights. Training was conducted on an NVIDIA A5000 GPU and took approximately 2 hours.
- **script**: Includes code for data preprocessing, model training, model validation, and REMI reconstruction examples.
