
# 🎵 Music Generation with AI  
Author: **rajjadhav7348**

---

## 🚀 Project Overview

This project explores the use of deep learning, particularly LSTM (Long Short-Term Memory) networks, to generate music.  
The model is trained on MIDI files and learns patterns in note sequences to generate new, original music.

The project supports:
- Automatic MIDI parsing
- Sequence preparation for training
- Model building using LSTM
- Music generation from trained weights
- Saving generated sequences as MIDI

---

## 🧠 Key Features

- ✅ LSTM-based sequence model for music learning  
- ✅ Handles chords and individual notes  
- ✅ Converts generated notes into MIDI format  
- ✅ Automatically creates a test MIDI file if none exist  
- ✅ Training checkpoints saved for reuse or generation

---

## 📁 Directory Structure

```
music-generation/
├── midi_songs/             # Folder containing .mid files
│   └── sample.mid          # Example created if no files exist
├── weights/                # Trained model weights (optional)
├── train.py                # Script to parse, train, and generate
├── generate.py             # Optional: script to generate music
└── README.md               # This file
```

---

## ⚙️ Requirements

Install required libraries using:

```bash
pip install tensorflow music21 numpy
```

Python version: **3.7+**

---

## 🛠️ How It Works

1. **MIDI Collection**: All `.mid` files in `midi_songs/` are parsed using `music21`.
2. **Note Extraction**: Notes and chords are extracted into sequences.
3. **Sequence Preparation**: Sequences are converted to integer encoding and split into input/output.
4. **Model Training**: A stacked LSTM model is trained to predict next notes.
5. **Music Generation**: The model generates new music notes, saved as a new `.mid` file.

---

## ▶️ How to Run

### Step 1: Add MIDI Files

Put MIDI files into the folder `midi_songs/`. If empty, a sample file is auto-created.

### Step 2: Train the Model

```bash
python train.py
```

Optional (if generation code is separate):

```bash
python generate.py
```

---

## 🏁 Output

* Training prints loss and saves best weights (e.g., `weights-improvement-05-1.2345.hdf5`)
* Generated MIDI file is saved as `output.mid` or similar
* Can be opened in any MIDI player (MuseScore, LMMS, etc.)

---

## 🧩 Sample Notes Generated

```
['C4', 'D4', 'E4', 'F4', 'G4', 'A4', 'B4', 'C5']
```

---

## 💡 Tips

* Increase the dataset size for better generation quality
* Reduce sequence length for faster training
* Train longer (more epochs) to generate more complex music
* Use genres (classical, jazz) as focused datasets

---

## 📬 Contact

**Author:** rajjadhav7348  
You can reach me through GitHub or community forums for questions and collaboration.

---
