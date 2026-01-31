# Red Alert 2 EVA Voice Assets

This folder contains extracted EVA (Electronic Video Agent) voice lines from Command & Conquer: Red Alert 2.

## Directory Structure

```
assets/audio/
├── eva_allied/          # Allied EVA voice lines (128 files)
│   ├── ceva*.wav        # Allied EVA announcements
│   ├── cevau*.wav       # Allied unit tutorials
│   ├── transcriptions.json
│   └── TRANSCRIPTIONS.txt
├── eva_soviet/          # Soviet EVA voice lines (130 files)
│   ├── csof*.wav        # Soviet EVA announcements
│   ├── csofu*.wav       # Soviet unit tutorials
│   ├── transcriptions.json
│   └── TRANSCRIPTIONS.txt
└── README.md
```

## Audio Files

### Allied EVA (`eva_allied/`)
- **ceva001-ceva122.wav**: Standard EVA announcements (warnings, status updates, etc.)
- **cevau*.wav**: Unit tutorial voice-overs explaining Allied units

### Soviet EVA (`eva_soviet/`)
- **csof001-csof122.wav**: Standard Soviet EVA announcements
- **csofu*.wav**: Unit tutorial voice-overs explaining Soviet units

## Transcript Mapping

Each folder contains:
- `transcriptions.json` - Machine-readable JSON mapping of filename to transcript
- `TRANSCRIPTIONS.txt` - Human-readable text file with all transcripts

### Usage Example (JavaScript)

```javascript
import alliedEva from './eva_allied/transcriptions.json';
import sovietEva from './eva_soviet/transcriptions.json';

// Get transcript for a specific file
const text = alliedEva['ceva048.wav']; // "Construction complete."

// Find files by keyword
const buildingLines = Object.entries(alliedEva)
  .filter(([file, text]) => text.toLowerCase().includes('building'));
```

## Common EVA Lines

| Event | Allied File | Soviet File | Transcript |
|-------|-------------|-------------|------------|
| Construction complete | ceva048.wav | csof048.wav | "Construction complete." |
| Unit ready | ceva062.wav | csof062.wav | "Unit ready." |
| Insufficient funds | ceva050.wav | csof050.wav | "Insufficient funds." |
| Low power | ceva053.wav | csof053.wav | "Low power." |
| Base under attack | ceva054.wav | csof054.wav | "Our base is under attack." |
| Unit lost | ceva064.wav | csof064.wav | "Unit lost." |
| Building | ceva052.wav | csof052.wav | "Building." |

## Audio Format

- Format: WAV (PCM)
- Sample Rate: 22050 Hz
- Channels: Mono
- Bit Depth: 16-bit

## Source

Extracted from Command & Conquer: Red Alert 2 / Yuri's Revenge using XCC Mixer.
Located in: `language.mix` → `audio.mix`
