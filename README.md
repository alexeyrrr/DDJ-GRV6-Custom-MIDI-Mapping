# DDJ-GRV6 Custom MIDI Mapping for Rekordbox 7

![Groove Circuit Replacement](Docs/Images/Groove%20Circuit%20Replacement.JPG)

**A performance-oriented custom MIDI mapping suite for the Pioneer DDJ-GRV6 in Rekordbox 7**, designed to streamline live workflows by reducing pad mode switching and expanding control accessibility.

---

## ⚙️ Button Changes (Standard Mapping)

**Major Reassignments:**

*   **Quick Track Pitch Control**:
    *   Switch in Groove Circuit is now → **Semitone Up** and **Semitone Down**
*   **Dedicated Beat Jump controls** :
    *   Now function independently of current pad mode (REV3, FWD3, REV4, FWD4)
    *   Note: Please check that the beat jump section of your pads is set to the correct page to show the +/- 16 beat and 32 beat values
*   **New dedicated Beat Loop buttons**:
    *   Direct buttons for **2-beat**, **4-beat**, **16-beat**, and **32-beat** loops
*   **Active Part / Stem Isolator buttons**:
    *   Direct buttons for muting **Vocal**, **Instruments**, **Bass**, and **Drums**

**Additional Features:**
*   Grid Slide button for quick beatgrid adjustments as shift functionality on the deck select buttons 
*   Headphone Mix / Volume and Master Level controls for compatibilty with soundcards (instead of GRV6 internal output)
*   MFX1 / MFX2 section (volume, on/off, select, assign)

---

## 🎛️ Choose Your Mapping

This repository provides two distinct MIDI mapping configurations. **Immediately determine which one fits your workflow:**

### 1. Standard Custom MIDI Map (Recommended & Default)
*   **Location:** `2 CUSTOM MIDI MAP/DDJ-GRV6 Mapping - Beat Jump, Auto Loop, Stems, Merge FX & Pitch (Non-Destructive).csv`
*   **Purpose:** A non-destructive enhancement of the default layout. Adds dedicated, instantly accessible controls for Beat Jump, Auto Loops, Stems Mute/UnMute, Merge FX, and semitone pitch shifts without sacrificing core functions or requiring constant pad mode switching.
*   **Best for:** Most DJs who want standard, intuitive controls on each deck.

### 2. Lex's Deluxe MIDI Map (Advanced Channel-Swapped Stem Isolation)
*   **Location:** `3 LEXS DELUXE MIDI MAPS/Lex's Deluxe GRV6 - Stable - Stems for 1,2 on ch 3,4.csv`
*   **Purpose:** Swaps the physical channels you use to control stem isolation knobs, allowing you to manipulate stems for Channel 1 & 2 using the physical controls of Channel 3 & 4.
    *   **Channel 1 Stems Control:** Enable stems isolation for Channel 1 by clicking **`SHIFT + CUE (Stem Iso)`** on **Channel 3**. You can then perform all stem adjustments on Channel 3 controls, while still keeping access to the regular Stems pad mode on Channel 1.
    *   **Channel 2 Stems Control:** Enable stems isolation for Channel 2 by clicking **`SHIFT + CUE (Stem Iso)`** on **Channel 4**. All adjustments are done using Channel 4 controls.
    *   **Normal Channel 3/4 Functionality:** Channel 3 & 4 EQs and controls still function normally. The only limitation is that if Stems Isolation mode is actively enabled for a side channel, you temporarily won't be able to use the regular EQs for Channel 3/4. Once you disable Stems Isolation mode, full regular EQ functionality returns immediately.
    *   **Reversible / Symmetrical Control:** You can also reverse this functionality so that the stem isolation buttons for Channel 1 & 2 enable stem isolation mode for Channel 3 & 4, making the entire setup function symmetrically.
*   **Best for:** DJs looking to offload stem adjustments from the active playing deck (Channel 1 & 2) onto the side channels (Channel 3 & 4) to keep physical hands-on control cleaner on the main decks.

---

## 📥 Installation

> [!IMPORTANT]
> This is a two-step process because Rekordbox restricts MIDI reassignment for factory controllers by default. You must replace a system default MIDI file first to unlock custom maps.

### Step 1: Replace the Default Mapping File (Required)

Rekordbox protects configuration files inside its system directory.

#### macOS Instructions:
1. Go to **System Settings → Privacy & Security → Full Disk Access**.
2. Click **+** and add your terminal app (e.g., `Terminal` or `iTerm`).
3. Restart your Terminal window.
4. Run the following commands to backup and replace the default MIDI mapping file:

   ```bash
   cd "/Applications/rekordbox 7/rekordbox.app/Contents/Resources/MidiMappings"
   
   # Backup original
   sudo cp DDJ-GRV6.midi.csv DDJ-GRV6.midi.csv.bak
   
   # Copy the custom default mapping from your cloned repo
   sudo cp ~/path/to/1\ DEFAULT\ MIDI\ MAP\ TO\ COPY\ TO\ REKORDBOX\ SYSTEM/DDJ-GRV6.midi.csv .
   ```
   *(Note: Replace `~/path/to/...` with the actual path to your cloned repository)*

#### Windows Instructions:
1. Navigate to your Rekordbox install directory's MidiMappings folder, typically:
   *   `C:\Program Files\Pioneer\rekordbox 7.x.x\MidiMappings\` or
   *   `C:\Program Files\rekordbox\rekordbox 7.x.x\MidiMappings\`
2. Find `DDJ-GRV6.midi.csv`.
3. Right-click on it → **Properties** → Uncheck **Read-only** → Click **Apply**.
4. Copy `DDJ-GRV6.midi.csv` from folder `1 DEFAULT MIDI MAP TO COPY TO REKORDBOX SYSTEM` in this repo and overwrite the one in the Rekordbox directory.

---

### Step 2: Import the Custom Mapping into Rekordbox

1. Connect your Pioneer DDJ-GRV6 controller and open Rekordbox.
2. Click the **MIDI** button in the top right.
3. In the MIDI settings window, make sure the **DDJ-GRV6** tab is selected.
4. Click **IMPORT** on the right side.
5. Select your chosen custom map:
   *   **For Standard Custom Map (Recommended):** Import `DDJ-GRV6 Mapping - Beat Jump, Auto Loop, Stems, Merge FX & Pitch (Non-Destructive).csv` from folder `2 CUSTOM MIDI MAP`.
   *   **For Deluxe Custom Map:** Import `Lex's Deluxe GRV6 - Stable - Stems for 1,2 on ch 3,4.csv` from folder `3 LEXS DELUXE MIDI MAPS`.
6. Restart Rekordbox to ensure settings initialize properly.

---

## 🎛️ How to Use

*   **Hot Cues**: You can leave your pads in Hot Cue mode for most of your set and perform easily without switching modes.
*   **Beat Jump**: Dedicated controls mapped to physical areas on the controller.
*   **Beat Loops**: Direct 2 / 4 / 16 / 32 beat loop buttons.
*   **Semitone Pitch Shift**: Use the two repurposed Drum Release FX Select buttons to pitch up/down.
*   **Active Parts (Stem Isolation)**: One-press toggle access to Vocal, Instrument, Bass, and Drums.
*   **Deluxe Stem Swap (Deluxe Mapping Only)**:
    *   **Channel 1 stems** are controlled via **Channel 3**: Activate stems control for Ch 1 by clicking **`SHIFT + CUE (Stem Iso)`** on Channel 3. Perform all adjustments using Channel 3 controls while retaining standard stems pad mode.
    *   **Channel 2 stems** are controlled via **Channel 4**: Activate stems control for Ch 2 by clicking **`SHIFT + CUE (Stem Iso)`** on Channel 4. Perform all adjustments using Channel 4 controls.
    *   *Note on Channel EQs:* EQs and controls on Channel 3 & 4 continue to work normally. However, if stem isolation is active on those side channels, the EQs control stems instead of normal EQ bands. Deactivate stem isolation to restore standard EQ functions. You can also reverse this setup so the buttons on Channels 1 & 2 activate stem isolation for Channels 3 & 4 symmetrically.


## 📂 Repository Structure & Files

This repository contains the following files:

| Folder / File | Type | Description |
| :--- | :--- | :--- |
| **`1 DEFAULT MIDI MAP TO COPY TO REKORDBOX SYSTEM/`** | Directory | Contains default controller database mapping. |
| └─ `DDJ-GRV6.midi.csv` | Configuration | Modified default controller configuration to remove read-only limits. **(Required base file replacement)** |
| **`2 CUSTOM MIDI MAP/`** | Directory | **[Recommended]** Contains the main custom performance map. |
| └─ `DDJ-GRV6 Mapping - Beat Jump, Auto Loop, Stems, Merge FX & Pitch (Non-Destructive).csv` | User MIDI Map | Features dedicated pitch shift, auto loops, beat jumps, and stem controls. |
| **`3 LEXS DELUXE MIDI MAPS/`** | Directory | Contains the deluxe channel-swapping stem isolation map. |
| └─ `Lex's Deluxe GRV6 - Stable - Stems for 1,2 on ch 3,4.csv` | User MIDI Map | Stem control mapped to channels 3 and 4 for controlling channels 1 and 2. |
| **`Stickers - New Groove Circuit Functionality/`** | Directory | Artwork vectors and PDFs for custom controller skins/stickers. |
| **`Docs/`** | Directory | Reference manuals for the Pioneer DDJ-GRV6 (including the MIDI message list). |

---