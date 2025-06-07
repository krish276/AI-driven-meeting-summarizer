# AI-Driven Meeting Summarizer

This project provides a small script that can record meeting audio, transcribe it using OpenAI's Whisper API, summarize key action items using ChatGPT, and generate a Word document containing the minutes of the meeting.

## Requirements

- Python 3.8+
- [sounddevice](https://pypi.org/project/sounddevice/)
- [soundfile](https://pypi.org/project/SoundFile/)
- [openai](https://pypi.org/project/openai/)
- [python-docx](https://pypi.org/project/python-docx/)
- [google-generativeai](https://pypi.org/project/google-generativeai/)

Install dependencies with:

```bash
pip install sounddevice soundfile openai python-docx google-generativeai
```

You will also need an OpenAI API key available in the environment variable `OPENAI_API_KEY` for audio transcription and a Gemini API key in `GEMINI_API_KEY` for summarization.

## Usage

Run the script from the command line:

```bash
python meeting_summarizer.py --duration 120 --output-dir my_minutes
```

This records audio from your microphone for 120 seconds, transcribes the recording, extracts action items, and saves a Word document in the `my_minutes` directory.

The resulting document contains both the raw transcript and a short summary of action items and key decisions.

