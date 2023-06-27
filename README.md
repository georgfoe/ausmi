# AUSMI

AUSMI is a virtual assistant that runs on Telegram. It can receive and respond to text messages and voice messages. AUSMI uses OpenAI's GPT-3.5-turbo model for text generation, the Whisper model for speech recognition, and the Thorsten-VITS model from Coqui-ai for text-to-speech conversion.

This project is a fork of the original [ausmi](https://github.com/marciojmo/ausmi) project by Marcio Mourão. The main change in this fork is the replacement of the Google TTS interface with the Coqui-ai TTS interface. Many thanks to Marcio for the original code!

## Features

- Text-to-Speech: AUSMI can convert a given text into speech and send it as an audio file. The text-to-speech model is currently set to use the German Thorsten-VITS model, but you can change this to any other model supported by Coqui-ai. You can find more information about the available models on the [Coqui-ai website](https://coqui.ai/models).
- Speech Recognition: AUSMI can transcribe a voice message and respond to it.
- Text Generation: AUSMI can respond to text messages by generating relevant responses.

## Installation

1. Clone the repository: `git clone https://github.com/georgfoe/ausmi.git`
2. Change into the directory: `cd ausmi`
3. Install the required packages: `pip install -r requirements.txt`
4. Set the `OPENAI_TOKEN` and `TELEGRAM_TOKEN` environment variables to your OpenAI and Telegram API keys.
5. Start the bot: `python bot.py`

## Docker

You can also run the bot in a Docker container. Here's how:

1. Build the Docker image: `docker build -t ausmi .`
2. Run the Docker container: `docker run -e OPENAI_TOKEN=<your_openai_token> -e TELEGRAM_TOKEN=<your_telegram_token> ausmi`

Replace `<your_openai_token>` and `<your_telegram_token>` with your OpenAI and Telegram API keys.

## Usage

After starting the bot, you can chat with it on Telegram. You can send it text messages or voice messages, and it will respond accordingly.

Available commands:

- `/read [text]`: Makes AUSMI read out the given text.
- `/help`: Displays a help message.

## Disclaimer

Please note that I have not been able to test the code yet due to lack of access to the OpenAI API. If you try it out and have any feedback or suggestions, I would be very happy to hear from you!

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
