### 1) guitar_chords_dataset_analysis.ipynb: 

    This Jupyter Notebook aims to explore the characteristics of the Guitar Chords v2 dataset. It was found that there were both mono and stereo audio files in the Guitar Chords v2 dataset. The majority of the audio was sampled at 16 kHz, but approximately 2/3 of the files were at 44100 Hz. The distribution of the duration time is random, with some audio files being less than 2 seconds long and others nearly 15 seconds long. The only consistent pattern observed was in the bit depth, as all audio files were in PCM_16.

### 2) dataset_preprocessing.ipynb:

    This Jupyter Notebook aimed to standardize all the audio files in the dataset. The original audio files are located in /datasets/guitar_chords_v2/original_test_set/audio_files/, and the standardized output was saved in /datasets/guitar_chords_v2/preprocessed_original/audio_files/. The standardization followed these parameters: 16 kHz sampling rate, mono, PCM_16, a half-second fade-out at the end of the audio, and the addition of 3 seconds of silence. The inclusion of fade-out and silence was considered for sound effects that require more time to be perceived, such as reverb.

### 3) apply_original_effects.ipynb:

    This Jupyter Notebook aims to apply the original effects on the Guitar Chords v2 Dataset. Audio inputs: /datasets/guitar_chords_v2/preprocessed_original/audio_files/. Audio outputs: /datasets/guitar_chords_v2/fx/audio_files/.

### 4) impulse_response_and_convolution.ipynb:

    This Jupyter Notebook aims to generate an impulse response for each fx described in /datasets/guitar_chords_v2/fx/parameters.json and simulate them using convolutons. Audio inputs: /datasets/guitar_chords_v2/preprocessed_original/audio_files/ Outputs: /datasets/guitar_chords_v2/impulse_response_emulation/audio_files/

### 5) compare_original_fx_with_ir_emulation.ipynb:

    This Jupyter Notebook aims to compare the original fx results with the IR emulation results for each FX. The metrics used for comparison are described in this file.