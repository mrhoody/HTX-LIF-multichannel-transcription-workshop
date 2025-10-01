# HTX-LIF Multichannel Transcription Workshop

A comprehensive workshop for learning speech-to-text transcription using OpenAI's Whisper model, with focus on multichannel audio processing and speaker diarization techniques.

**✨ This workshop is designed to run in Google Colab - no local installation required! ✨**

## Purpose

This repository provides hands-on tutorials and examples for:
- Understanding speech-to-text technology fundamentals
- Using OpenAI's Whisper model for automatic transcription
- Processing single-speaker and multi-speaker audio
- Implementing speaker diarization techniques
- Working with multichannel audio files
- Separating and transcribing individual audio channels

Perfect for researchers, developers, and audio engineers working with audio transcription and analysis tasks.

## Getting Started with Google Colab

### Quick Start (Recommended)

The easiest way to use this workshop is through Google Colab:

1. **Open the notebook in Google Colab:**
   - Navigate to the `notebooks/` folder in this repository
   - Click on `whisper_multichannel_tutorial.ipynb`
   - Click the "Open in Colab" badge at the top of the notebook, OR
   - Go to [Google Colab](https://colab.research.google.com/)
   - Select "GitHub" tab
   - Enter the repository URL: `mrhoody/HTX-LIF-multichannel-transcription-workshop`
   - Select the `whisper_multichannel_tutorial.ipynb` notebook

2. **Enable GPU acceleration (Recommended):**
   - In Colab, go to `Runtime` → `Change runtime type`
   - Select `T4 GPU` or `GPU` as the hardware accelerator
   - Click `Save`
   - This will significantly speed up transcription with Whisper

3. **Run the setup cells:**
   - The notebook includes installation commands for all required packages
   - Simply run the cells in order - dependencies will be installed automatically
   - Note: The first run may take a few minutes to install all packages

### Setting up Hugging Face Token (For Speaker Diarization)

To use speaker diarization features with pyannote.audio, you'll need a Hugging Face token:

1. **Create a Hugging Face account** (if you don't have one):
   - Visit https://huggingface.co/join

2. **Accept model conditions:**
   - Visit https://huggingface.co/pyannote/speaker-diarization
   - Click "Agree and access repository"

3. **Create an access token:**
   - Go to https://huggingface.co/settings/tokens
   - Click "New token"
   - Give it a name (e.g., "colab-workshop")
   - Select "Read" role
   - Click "Generate"
   - Copy the token

4. **Set the token in Google Colab:**
   ```python
   import os
   os.environ['HF_TOKEN'] = 'your_token_here'  # Replace with your actual token
   ```
   
   Or use Colab's Secrets feature (recommended):
   - Click the 🔑 key icon in the left sidebar
   - Add a new secret named `HF_TOKEN`
   - Paste your token as the value
   - Enable notebook access
   - In your notebook, access it with:
   ```python
   from google.colab import userdata
   os.environ['HF_TOKEN'] = userdata.get('HF_TOKEN')
   ```

### Local Installation (Alternative)

If you prefer to run the notebook locally instead of using Google Colab:

**Prerequisites:**
- Python 3.8 or higher
- pip package manager
- (Optional) CUDA-compatible GPU for faster processing

**Setup Instructions:**

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

4. Launch Jupyter Notebook:
```bash
jupyter notebook
```

5. Navigate to `notebooks/whisper_multichannel_tutorial.ipynb` in your browser

## Tutorial Contents

The main tutorial notebook covers:

1. **Speech-to-Text Primer**: Introduction to automatic speech recognition concepts
2. **Whisper Introduction**: Overview of OpenAI's Whisper model and its capabilities
3. **Single-Speaker Demo**: Basic transcription with a single speaker audio file
4. **Multi-Speaker Demo**: Handling audio with multiple speakers
5. **Speaker Diarization**: Identifying and separating different speakers in audio
6. **Multichannel Processing**: Splitting multichannel audio and transcribing each channel separately

### Working with Audio Files in Colab

The tutorials work with sample audio files. In Google Colab, you can:
- **Generate synthetic audio** directly in the notebook (examples provided)
- **Upload your own audio files** using Colab's file upload feature:
  ```python
  from google.colab import files
  uploaded = files.upload()
  ```
- **Access files from Google Drive:**
  ```python
  from google.colab import drive
  drive.mount('/content/drive')
  ```
- **Download sample audio files** from public datasets or URLs directly in the notebook

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
