# DDJ-GRV6 Custom MIDI Mapping for Rekordbox 7

**A performance-oriented custom MIDI mapping for the Pioneer DDJ-GRV6 in Rekordbox 7**, designed to improve live workflow by reducing pad mode switching.

### Overview & Philosophy

A common point of friction in the stock DDJ-GRV6 mapping is that Hot Cue, Beat Jump, Beat Loop, Sampler, and other performance modes all compete for the same 8 pads. This often forces you to switch modes during a set.

**This custom mapping improves that experience** by adding dedicated controls for frequently used functions.

**Core Objective:**
- Provide direct access to Beat Jump and common Beat Loops without needing to change pad modes.
- Let you stay in Hot Cue mode on the pads for most of your set, while still having instant access to jumps and loops.

**Result:** Faster, more fluid performance — for example, jumping to a cue point and immediately firing a 16-bar loop without multiple mode changes.

### Button Changes & Trade-offs

**Major Reassignments:**

- **Two buttons originally used for Drum Release FX Select**:
  - Now → **Semitone Up** and **Semitone Down** (works across all decks)
  - Lost → Original Drum Release FX type selection

- **Dedicated Beat Jump controls** (repurposed PAD5–PAD8 area):
  - Now function independently of current pad mode (REV3, FWD3, REV4, FWD4)

- **New dedicated Beat Loop buttons**:
  - Direct triggers for **2-beat**, **4-beat**, **16-beat**, and **32-beat** loops

- **Active Part / Stem Isolator buttons**:
  - Direct access for **Vocal**, **Instruments**, **Bass**, and **Drums**

- **Drum Release FX**:
  - Moved to alternative MIDI codes to free up the original buttons for pitch shifting.

**Additional Features:**
- Grid Slide button for quick beatgrid adjustments
- Headphone Mix / Volume and Master Level controls
- MFX1 / MFX2 section (volume, on/off, select, assign)

**What you lose:**
- Some advanced Drum Swap and Drum Release FX workflows (deprioritized in favor of faster performance tools).

### Files Included

| File | Type | Purpose |
|------|------|--------|
| `DDJ-GRV6.midi.csv` | Modified Default Mapping | Required base file replacement |
| `My Custom DDJ-GRV6 with pitch shift.csv` | Custom User Mapping | Main mapping to import |

### Installation

#### Step 1: Replace the Default Mapping File (Required)

Rekordbox protects files inside the app bundle. On macOS you will likely need to grant **Full Disk Access** first.

**macOS Instructions:**

1. Go to **System Settings → Privacy & Security → Full Disk Access**
2. Click the lock at the bottom and authenticate
3. Click **+** and add your terminal app:
   - `Terminal` (located in `/Applications/Utilities/`) or
   - `iTerm` (if you use iTerm — recommended)
4. Restart your Terminal/iTerm window

5. Run the following commands:

```bash
cd "/Applications/rekordbox 7/rekordbox.app/Contents/Resources/MidiMappings"

# Backup original
sudo cp DDJ-GRV6.midi.csv DDJ-GRV6.midi.csv.bak

# Copy the custom default mapping
sudo cp ~/path/to/1\ DEFAULT\ MIDI\ FILE\ TO\ COPY\ TO\ Key\ Mappings/DDJ-GRV6.midi.csv .
```

> **Tip:** Replace `~/path/to/...` with the actual location of the file.

**Windows Instructions:**

1. Go to: `C:\Program Files\Pioneer\rekordbox 7.x.x\MidiMappings\`
2. Find `DDJ-GRV6.midi.csv`
3. Right-click → **Properties** → Uncheck **Read-only** → Apply
4. Copy the version from this repo into the folder (overwrite)

#### Step 2: Import the Custom Mapping

1. Open Rekordbox and connect your DDJ-GRV6
2. Go to **MIDI** tab → Select **DDJ-GRV6**
3. Click **IMPORT**
4. Select `My Custom DDJ-GRV6 with pitch shift.csv`
5. Restart Rekordbox

### How to Use

- **Hot Cues**: You can comfortably leave your pads in Hot Cue mode for most of your set.
- **Beat Jump**: Use the dedicated Beat Jump buttons.
- **Beat Loops**: Use the new direct 2/4/16/32 beat loop buttons.
- **Semitone Pitch Shift**: Use the two repurposed Drum Release FX Select buttons.
- **Active Parts**: One-press access to Vocal / Inst / Bass / Drums isolators.

### Troubleshooting

- Assignment warnings on first import are normal — restart Rekordbox.
- If mappings don’t respond, click **DEFAULT** then re-import the custom file.
- To restore original behavior: Use the **DEFAULT** button in MIDI settings or delete the `MidiMappings` folder and relaunch Rekordbox.

### Compatibility

- Controller: Pioneer DDJ-GRV6
- Software: Rekordbox 7.2.14+ (tested on 7.2.14)
- OS: Windows & macOS