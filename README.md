
# Little Speech Game – Spanish Edition

A speech-driven educational game for practicing Spanish words and phrases with real-time feedback, MIDI music, and engaging visuals. This version is focused on Spanish, with auto-generated audio and support for custom word lists.

-----

## Features


- **Enhanced Speech Recognition**: Calibrates to ambient noise for improved accuracy. Uses your microphone to recognize spoken Spanish words and phrases.
- **Selectable Word Lists**: Choose from multiple word lists (e.g., animals, food) from the main menu.
- **Text-to-Speech & Auto SFX**: Prompts and feedback are spoken aloud using gTTS. Missing word audio is auto-generated.
- **Multiple Modes**: Practice with words or phrases, with translations shown.
- **Custom Content**: Easily edit `config_es.json` to add or change word/phrase lists. Each entry can have a translation.
- **Visual Feedback**: Animated highlights, clipart for words, and progress indicators.
- **Sound & Music**: Audio feedback for correct/incorrect answers, celebration melodies (MIDI), and a dance animation sequence.
- **Clipart Support**: Shows relevant images for each word (from `assets/images/clipart/vector`).
- **Configurable**: Toggle fullscreen/windowed mode, adjust content lists, and more.
- **Cross-platform**: Runs on Windows, Linux, and macOS (Python 3.8+).

-----

## Installation


### Requirements

- Python 3.8 or newer
- [SDL2 libraries](https://www.libsdl.org/) (required by Pygame)
- A MIDI synthesizer (most operating systems include one by default)
- Microphone (for speech input)
- Internet connection (for gTTS and Google Speech API)


### Install dependencies

```bash
pip install -r requirements.txt
```


### Assets

- **Sounds**: Place sound effects in `assets/sounds/` (e.g., `mouse_click.wav`, `beep_shorter.wav`). Word audio is auto-generated as needed.
- **Images**: Place word clipart in `assets/images/clipart/vector/` (filenames should contain the word or translation).
- **Dance Animation**: Place dance frame images in `assets/videos/dance2/`.
- **Microphone Icon**: Place `microphone_001.png` in `assets/images/images/`.
- **Fallback Image**: Place `unknown_001.png` in `assets/images/images/`.
- **Main Menu Image**: Place `cover_speaking_girl.png` in `assets/images/images/`.


### Configuration

Edit `config_es.json` to customize word and phrase lists. The config supports multiple lists, each with an `items` array (with `word` and optional `translate`), and an `order` ("random" or "sequential"). The game will auto-create a default config if missing.

Example structure:

```json
{
  "word_list_animals": {
    "items": [
      {"word": "gato", "translate": "cat"},
      {"word": "perro", "translate": "dog"},
      {"word": "león", "translate": "lion"}
    ],
    "order": "random"
  },
  "phrase_list": {
    "items": [
      {"word": "Buenos días", "translate": "Good morning"},
      {"word": "¿Cómo estás?", "translate": "How are you?"}
    ],
    "order": "sequential"
  }
}
```

-----


## Running the Game

```bash
python speak-es.py
```

-----


## Controls

| Key / Action    | Effect                                   |
| :-------------- | :----------------------------------------|
| Mouse click     | Select menu options, dropdowns, buttons   |
| Alt + Enter     | Toggle fullscreen/windowed mode           |
| Esc             | Return to menu / quit                     |
| Q               | Quit game                                 |
| C               | Open configuration file (`config_es.json`)|

-----


## File Structure

```
learn-spanish/
├── speak-es.py
├── config_es.json
├── requirements.txt
├── assets/
│   ├── images/
│   │   ├── images/
│   │   │   ├── cover_speaking_girl.png
│   │   │   ├── microphone_001.png
│   │   │   └── unknown_001.png
│   │   └── clipart/vector/
│   │       └── ... (word images)
│   ├── sounds/
│   │   ├── mouse_click.wav
│   │   ├── beep_shorter.wav
│   │   └── ... (auto-generated word audio)
│   └── videos/dance2/
│       └── ... (dance frames)
```

-----

## Dependencies


- `pygame`
- `gtts`
- `SpeechRecognition`
- `numpy`
- `sounddevice`
- `python-dotenv` (optional, for environment config)

-----

## Credits & Acknowledgements

### Core Technologies

| Technology | Purpose | Link |
| :--- | :--- | :--- |
| **Pygame** | Game engine, graphics & MIDI | [pygame.org](https://www.pygame.org) |
| **gTTS** | Text-to-speech synthesis | [gTTS Docs](https://gtts.readthedocs.io) |
| **SpeechRecognition**| Speech-to-text recognition | [SpeechRecognition](https://pypi.org/project/SpeechRecognition/) |
| **Sounddevice** | Audio recording & playback | [pypi.org/project/sounddevice/](https://pypi.org/project/sounddevice/) |
| **NumPy** | Audio data processing | [numpy.org](https://numpy.org) |
| **SDL2** | Multimedia backend (Pygame) | [libsdl.org](https://www.libsdl.org) |

### Assets

| Asset Type | Source | License |
| :--- | :--- | :--- |
| Sound Effects | [Kenney.nl](https://kenney.nl/assets) | CC0 1.0 Universal |
| Fonts | [OpenDyslexic](https://opendyslexic.org) | SIL Open Font License |
| Icons/Clipart | [Font Awesome](https://fontawesome.com) | CC BY 4.0 |
| Dance Images | Various / Custom | Educational Use |

-----

## Special Thanks

  - Open Source Community
  - Beta Testers
  - Python Software Foundation
  - GitHub

-----


**If you use or adapt this project, please consider sharing improvements or feedback!**