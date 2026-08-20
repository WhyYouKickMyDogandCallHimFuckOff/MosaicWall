A local, browser-based photo and video wall. Point it at a folder and it fills the screen with your images and videos, then keeps adding new ones over time — each shown at its own true aspect ratio, never cropped or stretched — landing wherever there's room until the screen is a slowly evolving collage.

Everything runs entirely in your browser. Your files are read directly from disk and are never uploaded anywhere.

Getting started
Download mosaic-wall.html
Open it in Chrome or Edge (recommended — see Browser support)
Click Choose folder… and select a folder of photos and videos

That's it — no install, no server, no build step.

Features
True aspect ratios, always — every photo and video is sized to exactly match its own shape. Nothing is ever cropped, stretched, or letterboxed.
Fills in over time — a configurable number of tiles appear immediately to fill the screen, then new ones arrive one at a time at a pace you control. Older tiles are simply left in place until something new happens to land on top of them.
No repeats until everything's had a turn — files are shuffled once per pass and drawn in order, so you'll see your whole collection before anything repeats.
Hover to zoom — hover any tile to magnify it in place.
Videos play through — video files autoplay (muted by default) and freeze on their last frame when finished.
Remembers your folder — in Chrome/Edge, the app can reconnect to the same folder next time you open it, with a single click (see below).
Controls

Click the gear icon (top right) to open the settings panel:

Setting	What it does
Initial tiles	How many tiles fill the screen right away
Speed	Seconds between each new tile arriving after the initial fill
Sound	Mute/unmute video playback
Reshuffle	Clear the wall and start over with a fresh shuffle
Fullscreen	Toggle fullscreen mode
Browser support

The app uses the File System Access API where available, which lets it remember your folder between sessions.

Browser	Folder picking	Remembers folder between sessions
Chrome / Edge (desktop)	✅	✅
Firefox / Safari	✅ (fallback picker)	❌ — you'll reselect the folder each time

This is a platform limitation, not a bug: Firefox and Safari don't implement the File System Access API, so the app falls back to a standard folder input, which works fine but can't be reopened without user interaction each time.

Hosting it yourself

This is a single, self-contained HTML file with no build step and no external dependencies other than one Google Font loaded from a CDN. You can:

Open it directly as a local file, or
Host it anywhere that serves static files — GitHub Pages works well and gives you a stable HTTPS URL for free (rename the file to index.html for a clean URL)

Hosting over HTTPS also has a practical benefit: some browsers are more consistent about persisting folder permissions from a real URL than from a file:// link.

Privacy

Nothing about this app phones home. Folder access, file reading, and playback all happen locally in your browser. The only network request it makes is fetching a font from cdnjs.cloudflare.com.

License

MIT — do whatever you'd like with it.
