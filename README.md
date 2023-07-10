# Realtime AI Character
Realtime AI Character is a revolutionary project enabling dynamic audio-visual interactions between humans and AI. Powered by Language Learning Model (LLM), it offers instant, natural, and context-aware responses, paving the way for a new era of interactive AI experiences.

## Prerequisites

Before you begin setting up this project, please ensure you have completed the following tasks:

### 1. Prepare OpenAI API Token

This application utilizes the OpenAI API to access its powerful language model capabilities. In order to use the OpenAI API, you will need to obtain an API token.

To get your OpenAI API token, follow these steps:

1. Go to the [OpenAI website](https://beta.openai.com/signup/) and sign up for an account if you haven't already.
2. Once you're logged in, navigate to the [API keys page](https://beta.openai.com/account/api-keys).
3. Generate a new API key by clicking on the "Create API Key" button.
4. Copy the API key and store it safely.
5. Add the API key to your environment variable, e.g. `export OPENAI_API_KEY=<your API key>`

### 2. Prepare ElevenLabs API Key

1. Creating an ElevenLabs Account
Visit [ElevenLabs](https://beta.elevenlabs.io/) to create an account. You'll need this to access the speech synthesis and voice cloning features.

2. In your Profile Setting, you can get an API Key. Save it in a safe place.

3. Set API key in your .env file:
```
XI_API_KEY=<api key>
```

## Installation
1. Clone the repo
   ```sh
   git clone
    ```
2. Install requirements
   - (For Mac) Install portaudio and ffmpeg
    ```sh
    brew install portaudio
    brew install ffmpeg
    ```
    Then install all python requirements
    ```sh
    pip install -r requirements.txt
    ```
3. Run db upgrade
    ```sh
    alembic upgrade head
    ```
4. Run the app & then go to http://localhost:8000/static/index.html
    ```sh
    uvicorn realtime_ai_character.main:app --reload
    ```
5. (Optional) Run client - python cli
    ```sh
    python client/client.py
    ```
6. Select one character to talk to, then start talking


## Tech Stack
Speech to Text: Whisper

Voice Clone and Sound Synthesis: ElevenLabs
