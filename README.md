# Denon LC6000 Prime for Mixxx

Custom Mixxx controller mapping for the Denon LC6000 Prime.

This repository provides:

- four fixed deck presets:
  - `Denon-LC6000-Prime-Deck1.midi.xml`
  - `Denon-LC6000-Prime-Deck2.midi.xml`
  - `Denon-LC6000-Prime-Deck3.midi.xml`
  - `Denon-LC6000-Prime-Deck4.midi.xml`
- one shared script file:
  - `Denon-LC6000-Prime-scripts.js`

Each preset is permanently assigned to one Mixxx deck. This is the recommended setup when using two or more LC6000 units at the same time.

## Features

- Transport, cue, sync, master, key lock, slip
- Jog wheel with touch scratching
- 14-bit tempo fader
- Pitch bend buttons with range switching on `Shift`
- Browse encoder and track loading
- Hold `Select` and turn to zoom the waveform
- Hot Cue mode
- Roll mode
- Auto Loop mode
- Needle search strip
- Button, pad, platter ring, and center display feedback

## Installation

1. Copy these files into your Mixxx controllers directory.

Common locations:

```text
~/.mixxx/controllers/
%LOCALAPPDATA%\Mixxx\controllers\
~/Library/Containers/org.mixxx.mixxx/Data/Library/Application Support/Mixxx/controllers/
```

Copy:

- `Denon-LC6000-Prime-Deck1.midi.xml`
- `Denon-LC6000-Prime-Deck2.midi.xml`
- `Denon-LC6000-Prime-Deck3.midi.xml`
- `Denon-LC6000-Prime-Deck4.midi.xml`
- `Denon-LC6000-Prime-scripts.js`

2. Start Mixxx.

3. Open `Preferences` -> `Controllers`.

4. For each connected LC6000, select the matching preset:

- left unit: `Denon LC6000 Prime Deck 1`
- right unit: `Denon LC6000 Prime Deck 2`
- optional third unit: `Denon LC6000 Prime Deck 3`
- optional fourth unit: `Denon LC6000 Prime Deck 4`

5. Configure the controller settings for each unit if needed:

- `Center display brightness`: `Low`, `Mid`, `High`, `Max`
- `Jog sensitivity`
- `Start in vinyl mode`
- `Enable center display SysEx`

## Multi-Controller Setup

Use one preset per physical LC6000.

Example for a two-deck setup:

- LC6000 #1 -> `Denon LC6000 Prime Deck 1`
- LC6000 #2 -> `Denon LC6000 Prime Deck 2`

Do not assign the same deck preset to two devices.

## Controls

### Transport

- `Play`: play/pause
- `Shift + Play`: stutter from cue
- `Cue`: standard cue behavior
- `Censor/Reverse`: reverse only while held
- `Shift + Censor/Reverse`: momentary censor
- `Sync`: beat sync
- `Shift + Sync`: disable sync
- `Master`: toggle sync leader
- `Key Lock`: toggle key lock
- `Shift + Key Lock`: reset key
- `Slip`: toggle slip mode
- `Pitch Bend - / +`: temporary pitch bend
- `Shift + Pitch Bend - / +`: change tempo range

### Browse and Loading

- `Back / Forward`: move library focus
- `Select turn`: move up/down in the library
- `Select press`: load selected track to the assigned deck
- `Shift + Select press`: load selected track to `PreviewDeck1` and play
- `Hold Select + turn`: waveform zoom
- `Shift + Select turn`: waveform zoom

### Track Navigation

- `Track Skip Prev / Next`: move in the library playlist
- `Shift + Track Skip Prev / Next`: continuous track search backward/forward
- `Beat Jump < / >`: beat jump backward/forward
- `Shift + Beat Jump < / >`: change beat jump size

### Loop Controls

- `Loop In`: set loop in point
- `Loop Out`: set loop out point
- `Auto Loop press`: enable loop or exit reloop
- `Auto Loop encoder`:
  - loop active: halve/double loop size
  - no loop active: change beatloop size
  - `Shift` while loop is active: move the loop
- `Parameter < / >`:
  - in loop modes: change loop size
  - in other modes: change beat jump size

### Performance Modes

- `Hot Cue`: selects Hot Cue pad mode
- `Loop`: selects Auto Loop mode
- `Roll`: selects Roll mode
- `Slicer`: selects Slicer mode
- Pressing an already selected mode button does nothing

### Pads

### Hot Cue Mode

- `Pad 1-8`: trigger Hot Cues 1-8
- `Shift + Pad 1-8`: clear Hot Cues 1-8

### Roll Mode

- `Pad 1`: `1/8`
- `Pad 2`: `1/6`
- `Pad 3`: `1/4`
- `Pad 4`: `1/3`
- `Pad 5`: `1/2`
- `Pad 6`: `2/3`
- `Pad 7`: `1`
- `Pad 8`: `2`

### Auto Loop Mode

- `Pad 1`: `1/8`
- `Pad 2`: `1/4`
- `Pad 3`: `1/2`
- `Pad 4`: `1`
- `Pad 5`: `2`
- `Pad 6`: `4`
- `Pad 7`: `8`
- `Pad 8`: `16`

### Manual Loop and Slicer Modes

- `Slicer` mode can be selected directly.
- Full native pad behavior for Manual Loop and Slicer is not implemented yet.

### Jog Wheel and Needle Strip

- `Platter touch`: enables scratching when vinyl mode is on
- `Jog wheel`: scratch or nudge depending on touch/vinyl state
- `Shift + Jog`: faster seek/nudge
- `Vinyl`: toggle vinyl mode
- `Needle touch + strip`: absolute track position seek

### LEDs and Display

- Main transport and mode LEDs follow Mixxx deck state
- Pad LEDs reflect the current pad mode
- The outer platter ring:
  - off while stopped
  - deck color while playing
  - blinking near the end of the track
- The center display supports:
  - brightness control
  - platter position ring
  - slip position ring
  - loop size text
  - basic deck color integration

## Notes

- Deck assignment is handled by the selected preset file, not by an on-device deck assignment mode.
- The mapping intentionally uses `Censor/Reverse` as `Reverse` on normal press and `Censor` on `Shift`.
- The center display can be disabled per preset with `Enable center display SysEx`.

## Attribution

This mapping was created with AI assistance using OpenAI Codex.
