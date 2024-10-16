# Transcription Project with Whisper :shipit:

This project uses OpenAI's Whisper to transcribe audio files into text. The code is designed to run on Google Colab, leveraging the Whisper model for automatic transcription of files in different languages.

## Prerequisites

Before starting, you must have:

 1. A Google account to use Google Colab

 2. An audio file saved in Google Drive

## Installation

Open a new Google Colab notebook and follow these steps to install Whisper and mount Google Drive.

```sh
!pip install git+https://github.com/openai/whisper.git
```
## Monta Google Drive

```python
from google.colab import drive
drive.mount('/content/drive')
```

# Audio File Transcription

Once you have Whisper installed and Google Drive mounted, you can transcribe your audio file.

## Transcribe the Audio File

Replace the path /content/drive/MyDrive/folder_audio/name_audio.mp3 with the path to your file.

```python
!whisper "/content/drive/MyDrive/folder_audio/name_audio.mp3" --model small --language German
```
> [!WARNING]
> ⚠️ remember to replace "folder_audio" and "name_audio" with the specific names of your directori !!!


# Model Options

Whisper offers several different model sizes, including `tiny`, `basic`, `small`, `medium`, and `large`. If you want more accuracy, you can use a larger template, for example:

```python
!whisper “/content/drive/MyDrive/folder_audio/name_audio.mp3” --model large --language German
```












