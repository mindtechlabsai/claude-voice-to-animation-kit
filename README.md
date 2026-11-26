# Voice to Animation for Claude

Turn a messy voice memo into clean narration and an animated scene that moves on the
exact word you say. **Your own voice, no AI voice.** Free. It runs on your own computer,
so your recordings never leave it.

| | You give Claude | You get |
|---|---|---|
| **1. Clean voice** | a phone recording with retakes, wrong words and background noise, plus your script | retakes cut, wrong words swapped, noise removed, pacing fixed, and a report of every edit |
| **2. Timed words** | the clean voice | the time of every word, plus captions (`.srt`) |
| **3. Animated scene** | a question, four options and the phrases to react to | a 1080p quiz video: labels pop in on your words, 3-2-1 countdown, the answer turns green as you say it |
| **Still check** | any video | one sheet of frames, so Claude can catch overlaps and cut-off text before you publish |

## Download

Get the files from **[Releases](../../releases/latest)** (right side of this page).

| File | For |
|---|---|
| `voice-to-animation.mcpb` | Claude Desktop (Windows and macOS) |
| `voice-to-animation-skill.zip` | Claude in the browser (claude.ai) |
| `SHA256SUMS.txt` | fingerprints to check your download is genuine |

## Install (pick one)

### A. Claude Desktop (easiest, recommended)

1. Download **`voice-to-animation.mcpb`**.
2. Double-click it. Claude Desktop opens it. Click **Install**.
   (Or: **Settings → Extensions → Advanced settings → Install Extension…** and pick the file.)
3. In a new chat, say: **"Run the voice-to-animation example."**

No Python, no terminal. On first use it downloads the free speech model (about 480 MB, once).
Your files go in **Documents → Voice to Animation**.

### B. Claude in the browser (claude.ai)

1. Download **`voice-to-animation-skill.zip`**. Don't unzip it.
2. In Claude: **Customize → Skills → + → Upload a skill**, and pick the ZIP.
3. Check **Settings → Capabilities → Code execution and file creation** is on.
4. In a chat, attach your recording and script and say: **"Use voice-to-animation on these."**

This runs in Claude's online sandbox, so it's slower. If your network settings block the
speech-model download there, use option A.

## How to use it

1. **Write your script** with one spoken sentence per line. Ask Claude to write it with you.
2. **Record it in one go** on your phone. If you fluff a line, pause and say the whole line again. Don't stop.
3. **Ask Claude:** "Clean my recording `my-memo.m4a` with my script `my-script.md`."
   Claude shows you every planned cut and word swap first. You approve, it builds.
4. **Ask for the scene:** "Make the quiz scene for this, with a big label every few seconds."
5. **Before you publish:** "Do the still check on the video."

## Check your download is genuine

Compare the fingerprint with the one in `SHA256SUMS.txt` on the release page.

- **Windows (PowerShell):** `Get-FileHash .\voice-to-animation.mcpb -Algorithm SHA256`
- **macOS (Terminal):** `shasum -a 256 voice-to-animation.mcpb`

If they don't match, don't install it. Only download from this page's Releases: we never
send the kit by email or DM.

## Privacy and safety

- Everything runs on your computer (option A). No account, API key or password needed.
- The extension can only read and write inside **Documents → Voice to Animation**.
- The only download it makes is the speech model, from its official release, checked against a fixed SHA-256 fingerprint.

## Credits and licences

- This kit: MIT licence.
- Speech-to-text: NVIDIA Parakeet TDT 0.6B v2 (CC-BY-4.0), run with [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx) (Apache-2.0). Downloaded on first use.
- Noise removal: [RNNoise](https://github.com/xiph/rnnoise) (BSD-3-Clause, notice included in the download) via ffmpeg's `arnndn` filter, with the `std.rnnn` model from [arnndn-models](https://github.com/richardpl/arnndn-models).
- [ffmpeg](https://ffmpeg.org) via [imageio-ffmpeg](https://github.com/imageio/imageio-ffmpeg), [skia-python](https://github.com/kyamagu/skia-python), and the [Poppins](https://github.com/itfoundry/Poppins) font (SIL Open Font Licence, included).

Made for the [MindTechLabs AI](https://www.youtube.com/@mindtechlabsai) YouTube channel.
