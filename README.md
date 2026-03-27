# Jarvis - Voice Assistant

A wake-word-activated voice assistant built in Python. Say **"Jarvis"** to activate it, then give commands to open websites, search Wikipedia, launch apps, and control your system.

---

##  Features

-  **Wake word detection** — activates on "Jarvis"
-  **Text-to-speech** responses via `pyttsx3`
-  **Opens websites** — Google, YouTube, Instagram, LinkedIn, VTOP portals
-  **Plays music** via a custom song library
-  **Wikipedia search** for general knowledge questions
-  **Launches apps** — Calculator, Notepad, Command Prompt
-  **System controls** — Shutdown, Restart, Lock

---

##  Tech Stack

| Library | Purpose |
|---|---|
| `speech_recognition` | Mic input via Google Speech API |
| `pyttsx3` | Offline text-to-speech (SAPI5) |
| `wikipedia` | Fetches article summaries |
| `webbrowser` | Opens URLs |
| `subprocess` | Launches system apps |
| `musiclib` | Custom song name → URL mapping |

---

##  Installation

**Requirements:** Python 3.8+, Windows, working microphone

1. **Clone the repository:**
```bash
git clone https://github.com/Krishh71/Jarvis_voice_assistant.git
cd Jarvis_voice_assistant
```

2. **Install dependencies:**
```bash
pip install speechrecognition pyttsx3 wikipedia pyaudio
```

> If PyAudio fails on Windows:
> ```bash
> pip install pipwin
> pipwin install pyaudio
> ```

The project includes a `musiclib.py` with the following songs:

| Command | Song |
|---|---|
| `play sanam` | Sanam |
| `play ragile` | Ragile |
| `play believer` | Believer |
| `play ayudha pooja` | Ayudha Pooja |
| `play chikri chikri` | Chikri Chikri |
| `play desi kalakaar` | Desi Kalakaar |
| `play phonk` | Phonk (Spotify) |

> To add more songs, edit `musiclib.py` and add entries to the `music` dictionary.

---

##  Usage

```bash
python jarvis.py
```

1. Jarvis starts and says *"Initializing Jarvis..."*
2. Say **"Jarvis"** to wake it up
3. Give a command (see below)
4. Say **"Jarvis off"** to put it back to sleep

---

##  Commands

| Command | Action |
|---|---|
| `open google` | Opens Google |
| `open youtube` | Opens YouTube |
| `open instagram` | Opens Instagram |
| `open linkedin` | Opens LinkedIn |
| `open vtop bhopal` | Opens VIT Bhopal portal |
| `open vtop chennai` | Opens VIT Chennai portal |
| `play <song>` | Plays a song from musiclib |
| `open calculator` | Launches Calculator |
| `open notepad` | Launches Notepad |
| `open cmd` | Opens Command Prompt |
| `shutdown` | Shuts down the PC |
| `restart` | Restarts the PC |
| `lock` | Locks the workstation |
| `who / what / how / why...` | Searches Wikipedia |
| `jarvis off` | Deactivates Jarvis |

---

## 📁 Project Structure

```
jarvis/
├── jarvis.py       # Main assistant script
└── musiclib.py     # Song name to URL dictionary
```

---

##  Notes

- Only works on **Windows** (uses SAPI5 for TTS and `.exe` for apps)
- Requires an active **internet connection** for speech recognition and Wikipedia
- Music playback depends on songs defined in `musiclib.py`

---

