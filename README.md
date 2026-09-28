openpibo-files
==============
- audio : audio files(mp3) for audio, speech examples
- image : image files(jpg,png) for oled vision examples

Rules for adding files
----------------------
The folders are used by the block IDE (openpibo-os.pibo / openpibo-os.pibrain `customblock.js`),
so do not add, rename or remove folders. Files dropped into an existing folder show up in the
block dropdown automatically (`/dir` API).

- file name: lowercase ascii / Korean, `_` instead of spaces.
  Do not use `'` `"` `` ` `` `$` `\` `#` (block code is `'<dir>'+'<file>'`, audio is played with `play "<file>"`).
- audio: `.mp3` or `.wav` only, lowercase extension (`.MP3` is rejected by `audio.play`).
- image (except sample): 128x64 jpg, black background + white line (Pibo OLED converts to 1-bit).
- do not put non-media files (txt, md, etc.) or dot files inside the folders; they show up in the dropdown.
- files reach robots only through a new OS image (`openpibo-files/.git` is removed when the image is built).
