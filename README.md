# HTX-LIF Multichannel Transcription Workshop

A comprehensive workshop for learning speech-to-text transcription using OpenAI's Whisper model, with focus on multichannel audio processing and speaker diarization techniques.

## Purpose

This repository provides hands-on tutorials and examples for:
- Understanding speech-to-text technology fundamentals
- Using OpenAI's Whisper model for automatic transcription
- Processing single-speaker and multi-speaker audio
- Implementing speaker diarization techniques
- Working with multichannel audio files
- Separating and transcribing individual audio channels

Perfect for researchers, developers, and audio engineers working with audio transcription and analysis tasks.

## Installation

### Prerequisites
- Python 3.8 or higher
- pip package manager
- (Optional) CUDA-compatible GPU for faster processing

### Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/mrhoody/HTX-LIF-multichannel-transcription-workshop.git
cd HTX-LIF-multichannel-transcription-workshop
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install -r requirements.txt
```

4. (Optional) For pyannote.audio, you may need to accept user conditions for models:
   - Visit https://huggingface.co/pyannote/speaker-diarization
   - Accept the user conditions
   - Create a Hugging Face access token
   - Set the token as an environment variable: `export HF_TOKEN=your_token_here`

## Usage

### Starting Jupyter Notebook

Launch Jupyter Notebook to access the interactive tutorials:

```bash
jupyter notebook
```

Then navigate to `notebooks/whisper_multichannel_tutorial.ipynb` in your browser.

### Tutorial Contents

The main tutorial notebook covers:

1. **Speech-to-Text Primer**: Introduction to automatic speech recognition concepts
2. **Whisper Introduction**: Overview of OpenAI's Whisper model and its capabilities
3. **Single-Speaker Demo**: Basic transcription with a single speaker audio file
4. **Multi-Speaker Demo**: Handling audio with multiple speakers
5. **Speaker Diarization**: Identifying and separating different speakers in audio
6. **Multichannel Processing**: Splitting multichannel audio and transcribing each channel separately

### Example Audio Files

The tutorials work with sample audio files. You can:
- Use the provided examples in the notebook
- Record your own audio samples
- Download sample audio files from public datasets

## Project Structure

```
HTX-LIF-multichannel-transcription-workshop/
├── README.md                           # This file
├── requirements.txt                    # Python dependencies
├── LICENSE                            # MIT License
└── notebooks/
    └── whisper_multichannel_tutorial.ipynb  # Main tutorial notebook
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- OpenAI for the Whisper model
- The pyannote.audio team for speaker diarization tools
- The open-source audio processing community

## Support

For questions or issues, please open an issue on GitHub.
