# 01_POP909_midi2remi
This code works well for POP909 dataset. Generic MIDI datasets won't work because they don't provide chords, beats, or keys. Set the input dir to be as follows:

input_directory/
├── 001/
│   ├── 001.mid
│   ├── beat_midi.txt
│   ├── chord_midi.txt
│   ├── key_audio.txt
│   └── ...
├── 002/
│   ├── 002.mid
│   ├── beat_midi.txt
│   ├── chord_midi.txt
│   ├── key_audio.txt
│   └── ...
├── 003/
│   ├── 003.mid
│   ├── beat_midi.txt
│   ├── chord_midi.txt
│   ├── key_audio.txt
│   └── ...
└── ... (additional subdirectories)

# 02_POP909_remi2np
Please run this code after executing code 01. It is convenient to use the output dir used in code 01 as the input dir in this code.

# 03_np_augmentation
This code is used to augment the np dataset. You can also check statistics of your preprocessed dataset. 


