# StyleNet
A cute multi-layer LSTM network that can perform like a human 🎶 It learns the dynamics of music! If you wish to learn more about my findings, then please read my [blogpost](http://imanmalik.com/cs/2017/06/05/neural-style.html). The architecture was specifically designed to handle music of different genres.

![GitHub Logo](http://imanmalik.com/assets/img/stylenet.png)



## Prerequisites
You will need a few things in order to get started. 

1. Tensorflow
2. mido
3. pretty_midi
4. fluidsynth

## How to Run
``` python main.py -current_run <name-of-session> -bi ```

Flags:  
`-load_last` : Loads and continues from last epoch.  
`-load_model`: Loads specified model.  
`-data_dir` : Directory of datasets.  
`-data_set` : Dataset name.  
`-runs_dir` : Directory of session files.  
`-forward_only` : For making predictions (not training).  
`-bi` : If you wish to use bi-directional LSTMs. (HIGHLY recommended)

## Files
`pionify.ipynb` : This was used to ensure the files across the dataset were consistent in their musical properties.
`generate_audio.ipynb` : This was used to make predicitions using StyleNet and generate the audio.
`convert-format.rb` : This was used to convert format 1 MIDIs into format 0.
`file_util.py` : This contains folder/file-handling functions.
`midi_util.py` : This contains MIDI-handling functions.
`model.py` : StyleNet's Class.
`data_util.py` : For shuffling and batching data during training.

